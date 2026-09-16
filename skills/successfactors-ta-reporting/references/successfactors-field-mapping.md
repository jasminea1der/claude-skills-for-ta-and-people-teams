# SuccessFactors field mapping

SuccessFactors Recruiting configurations differ. Treat these as canonical output fields
and map the local export to them; confirm the mapping before publishing metrics.

## Canonical fields

| Canonical field | Used by | Likely source labels or objects |
|---|---|---|
| `requisition_id` | All reports | Job requisition ID / Requisition ID |
| `application_id` | Applications, funnel, hires | Application ID |
| `candidate_id` | De-duplication only | Candidate ID |
| `requisition_title` | Open positions | Job title / Requisition title |
| `requisition_status` | Open positions | Status / Requisition status |
| `requisition_open_date` | Open positions, time to fill | Open date / Job requisition opened |
| `application_received_date` | Applications, time to hire | Application date / Applied date |
| `status_name` | Funnel | Application status / Candidate status |
| `status_date` | Funnel | Status change date / Application history date |
| `hire_date` | Hires, time to hire | ATS hired-status date / employee hire date only if confirmed |
| `start_date` | Optional validation | Employee start date; do not substitute without confirmation |
| `offer_status` | Offer acceptance | Offer status / Offer outcome |
| `offer_date` | Offer acceptance | Offer date |
| `offer_acceptance_date` | Time to fill | Offer accepted date |
| `ta_partner` | All reports | Recruiter / Talent Acquisition Partner |
| `department` | All reports | Department / Business unit |
| `location` | All reports | Location / Job location |
| `source` | Source of hire | Source / Candidate source / Application source |
| `role_type` | Role-type time to fill | Waged/Salaried classification |
| `level` | Role-type mapping | Job level / Pay grade / Career level |

## Mapping checks

1. Confirm whether the export is application-level, requisition-level, or status-history
   level. A status-history export will have repeated application IDs by design.
2. Confirm that the recruiter field is the TA partner, not the hiring manager or the person
   who last edited the requisition.
3. Confirm whether `hire_date` means the ATS hired-status date, employee hire transaction
   date, or actual start date. Do not assume it means offer acceptance.
4. Confirm whether `offer_acceptance_date` is available separately. Use it for time to
   fill; only use it as a documented fallback for `hire_date` when no hire event exists.
5. Confirm whether source is first-touch, last-touch, or a single SuccessFactors source
   value. Do not call a last-touch value “source of hire” without labelling the attribution.
6. Confirm that level values are current and map cleanly to the four required role types.

Keep a mapping table in the delivery note with `source_field`, `canonical_field`,
`transformation`, and `confirmed_by`. Unmapped required fields should be listed as gaps,
not silently omitted.

## Arnott's hires/offers export

For the reported SuccessFactors fields, use this initial mapping:

| SuccessFactors field | Canonical field | Use |
|---|---|---|
| `Application: Application ID` | `application_id` | Join key and unique application count |
| `Application: Job Req ID` | `requisition_id` | Join key to requisition data |
| `Application: Recruited On` | `hire_date` | Confirmed by the user as the date the application entered the final hired/recruited outcome |
| `Offer Letter: Created Date` | `offer_date` | Offer volume and offer timing |
| `Offer Detail: Start Date` | `start_date` | Optional start-date validation; not the default hire date |
| `Offer Letter: Candidate Offer Response Date` | `offer_acceptance_date` | Confirmed by the user as populated for both accepted and declined responses; use with `offer_status` for decided offers |
| `Offer Letter: Offer Status` | `offer_status` | Accepted, declined, pending, withdrawn or expired outcome |

This export is not sufficient by itself for:

- **Time to hire**, because it still needs `application_received_date` from an application
  received/applied date field.
- **Time to fill**, because it still needs `requisition_open_date`.
- **Source of hire**, unless a source field is added.
- **Hires by department, location or TA partner**, unless those requisition fields are
  added or joined from a requisition export.
- **The full recruitment funnel**, unless status history with status dates is added.

The user confirmed that “Recruited” is the final hired outcome in this SuccessFactors
instance and that Candidate Offer Response Date is populated for both accepted and
declined offers. Use these mappings unless the SuccessFactors configuration changes.

## Recruitment funnel source report

Create a separate **application status history** report in SuccessFactors. Do not build the
funnel from the hires/offers report: that report contains outcomes, but not every stage an
application passed through or the date it reached each stage.

Select the report object or columns that expose one row per application-status event, with
at least:

| Required field | Why it is needed |
|---|---|
| `Application: Application ID` | Unique funnel unit and join key |
| `Application: Job Req ID` | Requisition join key and filtering |
| `Application: Application Status` or status label | Map local statuses to Applications, Screened, Interviewed, Offered and Hired |
| `Application: Status Change Date` or event date | Identify when each stage was first reached |
| `Application: Application Received/Applied Date` | Period scope and Applications stage |
| TA Partner/recruiter | TA Partner filter |
| Department | Department filter and breakdown |
| Location | Location filter and breakdown |

If the SuccessFactors report builder cannot expose status history as multiple rows per
application, export the application audit trail/status audit report instead. The critical
requirement is repeated rows for the same Application ID, one for each status transition,
not just the current status. Also export the local status labels exactly as configured so
they can be mapped in `StatusMapping`.

Map the local statuses to the canonical funnel:

`Applications > Screened > Interviewed > Offered > Hired`

Count an application once at each stage it reached, using the first status-change date for
that stage. The hires/offers report can validate the `Hired` stage and offer outcomes, but
the status-history report is the source of truth for the full funnel.
