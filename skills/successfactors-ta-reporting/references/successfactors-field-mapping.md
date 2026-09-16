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
| `hire_date` | Hires, time to hire | Hire date / Start date only if confirmed |
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
3. Confirm whether `hire_date` means hire transaction date, accepted start date, or actual
   start date. Use only the confirmed event for time to hire.
4. Confirm whether source is first-touch, last-touch, or a single SuccessFactors source
   value. Do not call a last-touch value “source of hire” without labelling the attribution.
5. Confirm that level values are current and map cleanly to the four required role types.

Keep a mapping table in the delivery note with `source_field`, `canonical_field`,
`transformation`, and `confirmed_by`. Unmapped required fields should be listed as gaps,
not silently omitted.
