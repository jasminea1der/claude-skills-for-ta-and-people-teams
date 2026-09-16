# SuccessFactors TA report definitions

Use these definitions unless the user confirms a different local definition. Record any
change in the delivery note and in the assumptions columns of the relevant report.

## Scope and dates

| Measure | Definition |
|---|---|
| Reporting period | Inclusive `report_period_start` through inclusive `report_period_end` in the agreed business timezone |
| Applications received | Unique applications whose `application_received_date` falls in the period |
| Total hires | Unique applications with a valid hire event in the period |
| Open positions | Unique requisitions whose status is open as of `as_of_date`; this is a snapshot, not a flow |
| Time to hire | Calendar days from `application_received_date` to `hire_date` |
| Time to fill | Calendar days from `requisition_open_date` to `offer_acceptance_date`; use `hire_date` only if acceptance is unavailable, and label the substitution |

Do not mix application-to-hire and requisition-open-to-acceptance in one metric. The
definitions are intentionally separate: one describes the candidate journey and the other
describes how long a vacancy remains open.

## Measures and formulas

| Report | Measure | Formula |
|---|---|---|
| KPI summary | Average time to hire | `sum(time_to_hire_days) / count(valid time_to_hire_days)` |
| KPI summary | Offer acceptance rate | `offers_accepted / offers_decided`, where decided is accepted + declined + withdrawn + expired if those outcomes are confirmed as decisions |
| Trend | Median time to hire | Median of valid application-to-hire calendar-day values in each period |
| Department | Hire share | `department_hires / total_hires` |
| Source | Hire conversion | `source_hires / source_applications` |
| Source | Hire share | `source_hires / total_hires` |
| Funnel | Conversion from previous stage | `current_stage_count / previous_stage_count` |
| Funnel | Conversion from applications | `current_stage_count / applications_count` |
| Role type | Average time to fill | `sum(valid time_to_fill_days) / count(valid time_to_fill_days)` |

Percentages are numeric fractions between 0 and 1. Keep the numerator and denominator in
the output so a reader can distinguish a real rate from a small sample.

## Canonical role types

Normalise local level values to these exact labels:

1. `Waged`
2. `Salaried L16 and below`
3. `Salaried L17 - L19`
4. `Salaried L20 and above`

If a role is salaried but has no level, use `Unassigned` and report the missing mapping.
Do not infer a level from job title alone.

## Funnel rules

The funnel is application-based and uses each application at most once. A record can count
in every stage it reached, so the stage counts should be non-increasing:

`Applications >= Screened >= Interviewed >= Offered >= Hired`

Use the first timestamp at which the application reached each mapped stage. If a local
workflow skips a stage, leave the mapping documented and do not manufacture a stage event.

## Missing and invalid data

- Missing dimensions are grouped as `Unassigned` or `Unknown`, not dropped.
- A missing date excludes the record from a duration denominator only.
- A zero denominator produces a blank rate, not zero.
- Negative durations are invalid and excluded after being counted in the data-quality note.
- Duplicate source records are de-duplicated by source identifier and latest valid event.
