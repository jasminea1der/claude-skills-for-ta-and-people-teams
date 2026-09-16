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
| `Application: Recruited On` | `hire_date` (provisional) | Total hires and time to hire, only after confirming this is the date the application entered the hired/recruited outcome |
| `Offer Letter: Created Date` | `offer_date` | Offer volume and offer timing |
| `Offer Detail: Start Date` | `start_date` | Optional start-date validation; not the default hire date |
| `Offer Letter: Candidate Offer Response Date` | `offer_acceptance_date` (provisional) | Time to fill and offer-decision timing; confirm it is populated for both accepted and declined responses |
| `Offer Letter: Offer Status` | `offer_status` | Accepted, declined, pending, withdrawn or expired outcome |

This export is not sufficient by itself for:

- **Time to hire**, because it still needs `application_received_date` from an application
  received/applied date field.
- **Time to fill**, because it still needs `requisition_open_date`.
- **Source of hire**, unless a source field is added.
- **Hires by department, location or TA partner**, unless those requisition fields are
  added or joined from a requisition export.
- **The full recruitment funnel**, unless status history with status dates is added.

Before using `Recruited On` as `hire_date`, confirm whether “Recruited” is the final hired
outcome in this SuccessFactors instance or an earlier recruiting status. Before using
Candidate Offer Response Date for `offer_acceptance_date`, confirm that the same field
records the response date for declined offers; the acceptance rate denominator requires
all decided offers, not only accepted ones.
