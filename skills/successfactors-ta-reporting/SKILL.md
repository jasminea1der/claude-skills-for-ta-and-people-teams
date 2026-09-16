---
name: successfactors-ta-reporting
description: Turns SAP SuccessFactors Recruiting exports into downloadable CSV reports for talent acquisition leadership — hiring KPIs, applications, time to hire, offer acceptance, open positions, trends, department and source analysis, funnel conversion, and time to fill by Waged, Salaried L16 and below, Salaried L17–L19, and Salaried L20 and above. Use when someone asks for SuccessFactors reports, TA dashboards, recruiting metrics, CSV exports, hiring funnel data, or reporting filtered by Talent Acquisition Partner, department, or location.
---

# SuccessFactors TA reporting

Builds a consistent CSV report pack from SAP SuccessFactors Recruiting data. The pack is
designed for Arnott's talent acquisition reporting: it answers the operational questions
leaders ask without pretending that SuccessFactors field names, stage history, or date
semantics are consistent until they have been checked.

This skill creates **CSV files, not a dashboard mock-up**. Each file is rectangular,
machine-readable, UTF-8 encoded, and safe to open in Excel. It includes the filter context
and reporting period so a downloaded file is still interpretable after it leaves the ATS.

## What you need to start

Minimum viable input:

1. A SuccessFactors Recruiting export or API extract containing requisitions, applications,
   candidate status history, offers and hires; and
2. The reporting period and whether dates should be interpreted in the business's local
   timezone.

Ask for the export if it is available. If the user does not have one, do not stall: create
the complete CSV pack with headers, a field-mapping request, and clearly labelled empty
outputs. Never fill a report with invented counts.

Ask only the highest-value questions first:

- What is the reporting period, and is it based on application, status-change, offer, hire
  or requisition dates?
- Which SuccessFactors status values mean screened, interviewed, offered and hired in this
  instance?
- Is “time to hire” application-to-hire or requisition-approved-to-hire, and is “time to
  fill” requisition-open-to-accepted-offer?

If these answers are unavailable, use the definitions in `references/metric-definitions.md`,
mark them as assumptions in the output, and list the exact fields that need confirmation.

## Process

### 1. Inspect and map the source

Read `references/successfactors-field-mapping.md` before transforming data. Map the user's
actual column names to the canonical fields there; do not assume a standard SuccessFactors
label. Preserve the original export untouched and work from a copy or an in-memory
transformation.

Require a stable identifier for each requisition and application. Candidate names, email
addresses, phone numbers, CV text and free-text notes are not needed for these aggregates.
Drop them before creating report files.

Check these data-quality conditions before calculating metrics:

- dates parse as dates and are in one timezone or explicitly normalised;
- each application has one requisition identifier;
- status history has event dates, not only the current status;
- requisitions have a consistent department, location, TA partner and role type;
- offer records distinguish accepted, declined, withdrawn, expired and pending;
- duplicate exports are removed using the source record identifier and event timestamp.

Report missingness rather than silently treating missing values as zero. A missing
department is `Unassigned`, a missing source is `Unknown`, and an unparseable date is
excluded only from the metric that requires it and counted in the data-quality note.

### 2. Apply the reporting scope and filters

Filter records by the requested reporting period and these optional dimensions:

- **Talent Acquisition Partner**
- **Department**
- **Location**

Apply filters consistently to every report. Include the selected value in the output's
filter columns; use `All` when a dimension was not restricted. Do not filter a funnel stage
independently: a funnel must use the same in-scope applications throughout.

For open positions, use the requisition's current state as of the extract date. If a
point-in-time snapshot is not available, label the output as “current as of extract date”
rather than presenting it as a historical period-end position count.

### 3. Derive the canonical stages and dates

Map local SuccessFactors statuses to the canonical funnel stages:

`Applications > Screened > Interviewed > Offered > Hired`

Count an application in a stage if it reached that stage at least once during the scope.
Use the first date it reached each stage. A later rejection does not erase a stage already
reached. Keep the stage mapping in the assumptions/data-quality section.

Use one explicit hire event per application. If an application has more than one hire-like
event, retain the earliest valid hire event and report the duplicate for review.

### 4. Calculate the measures

Use `references/metric-definitions.md` for the authoritative formulas. In particular:

- **Total hires** is a count of unique applications with a valid hire event.
- **Applications received** is a count of unique applications received in the period.
- **Average time to hire** is the arithmetic mean in calendar days for hired applications
  with both required dates; include the denominator.
- **Offer acceptance rate** is accepted offers divided by decided offers, not accepted
  offers divided by all offers. Show pending/withdrawn/expired separately where available.
- **Open positions** is a count of requisitions currently open at the extract date.
- **Time to hire trend** is grouped by the selected grain (month by default) using the same
  date definition as the headline time-to-hire metric.
- **Time to fill by role type** uses exactly four labels: `Waged`, `Salaried L16 and below`,
  `Salaried L17 - L19`, and `Salaried L20 and above`.

Do not substitute time to fill for time to hire. If the source cannot support the requested
measure, output the column with blank values and state the missing source field.

### 5. Produce the CSV pack

Create these files using `assets/csv-templates/`:

| File | Grain | Purpose |
|---|---|---|
| `ta_kpi_summary.csv` | One row per filter/period | Total hires, applications, average time to hire, offer acceptance and open positions |
| `time_to_hire_trend.csv` | One row per period | Hire volume, average and median time to hire, and denominator |
| `hires_by_department.csv` | One row per department | Hires and share of all in-scope hires |
| `source_of_hire.csv` | One row per source | Applications, hires, hire share and conversion |
| `recruitment_funnel.csv` | One row per funnel stage | Counts, conversion from previous stage and conversion from applications |
| `time_to_fill_by_role_type.csv` | One row per role type | Requisition count, hires, average and median time to fill |
| `open_positions.csv` | One row per open requisition | Requisition detail for action and export |

Every aggregate file contains `report_period_start`, `report_period_end`,
`ta_partner_filter`, `department_filter`, `location_filter`, and `as_of_date`. Detail files
also contain the source record identifier needed to reconcile back to SuccessFactors.

Use ISO dates (`YYYY-MM-DD`), decimal days to two places, percentages as numeric values
between 0 and 1, and UTF-8 with a header row. Quote fields that contain commas, line breaks
or double quotes according to RFC 4180. Use an empty field for not-applicable rather than
`0`, `N/A`, or a fabricated estimate.

### 6. Reconcile and package

Before delivering the files, run these checks:

- total hires in `ta_kpi_summary.csv` equals the hired count in
  `recruitment_funnel.csv`;
- department hire counts sum to total hires, allowing for an explicit `Unassigned` row;
- source hire counts sum to total hires, allowing for `Unknown`;
- funnel counts are non-increasing from applications to hired;
- offer acceptance numerator is not greater than its decided-offer denominator;
- role-type counts reconcile to the source population, with an explicit `Unassigned` row
  if role type is missing;
- every open requisition has a requisition identifier, status, title, department, location,
  TA partner, role type and as-of date where the source provides them.

Include a short `README` or delivery note beside the CSVs stating the source extract,
period, filters, timezone, metric definitions, status mapping, excluded records and
reconciliation exceptions. Keep it factual and concise. The CSVs are the deliverable;
the note prevents them being misread later.

## Output

Deliver a folder or archive containing the seven CSV files and the delivery note. The
headline KPI file should have these columns:

`report_period_start,report_period_end,as_of_date,ta_partner_filter,department_filter,location_filter,total_hires,applications_received,average_time_to_hire_days,time_to_hire_denominator,offers_accepted,offers_decided,offer_acceptance_rate,open_positions`

Use the exact headers in `assets/csv-templates/` for the other six files. Do not add
personal data to any output. If the user asked for a dashboard import, preserve these CSVs
as the source artefacts and offer a dashboard-ready variant only after the CSVs reconcile.

## Data, privacy and reporting guardrails

SuccessFactors exports can contain personal and sensitive information. Request identifiers
instead of names, remove candidate contact details and free text, and do not export
protected characteristics for these reports. Aggregate results can still expose small
groups: flag low-count slices for the user's privacy review rather than suppressing them
silently.

These are operational reporting definitions, not audit or legal conclusions. Keep the
source extract, status mapping and assumptions available for review, especially where
time-to-hire or funnel numbers may be used to compare teams or locations.

## Reference files

- `references/metric-definitions.md` — formulas, date rules, denominators and reconciliation
  rules for every requested report.
- `references/successfactors-field-mapping.md` — canonical fields and likely
  SuccessFactors source objects/labels to map against the local configuration.
- `assets/csv-templates/` — exact output headers for the seven downloadable CSVs.

---

*Part of the [Claude Skills for TA and People Teams](https://github.com/we-are-move/claude-skills-for-ta-and-people-teams) collection — open-source skills
for in-house talent and people teams. Built and maintained by the team at MOVE.*
