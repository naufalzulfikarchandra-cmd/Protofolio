# AI Project Risk Monitoring

## Project profile

Independent PMO portfolio simulation by Naufal Zulfikar Chandra, prepared with AI assistance for document preparation, coding and analysis. The project studies how an internal PMO could prioritise project reviews using early project measurements. It does not represent employment at a real client or an implemented company system.

## Business problem and intended decision

A PMO with limited review capacity needs a consistent way to identify projects that deserve earlier attention. A risk score is only useful if its inputs would have been known when the review decision was made, and if the review queue fits available capacity. The simulated objective is to support review prioritisation, not to automate project decisions or guarantee delivery outcomes.

## My role and use of AI

I initiated and directed the project, chose the portfolio objective, constrained spending, selected the 20% demo review capacity, corrected stage boundaries and changed the dashboard delivery from Power BI to HTML when the original approach did not meet my needs. AI assisted with the preparation of project documents, pipeline code, analysis and dashboard. Formal acceptance of the resulting package and user testing are still separate tasks.

The PMO skills demonstrated are scope definition, work breakdown, budget assumptions, change control, evidence review, risk governance, status reporting and decision preparation. The technical artifacts support those skills; they are not presented as software I personally wrote without assistance.

## Delivery approach

| Stage | Main artifact |
|---|---|
| Initiation | Business case, charter, stakeholder and governance documents |
| Planning | 28 task WBS, simulated schedule, RACI and Jira backlog |
| Budget | Baseline allocation, simulated cost ledger, forecast and cost definitions |
| Governance | RAID snapshot, control gates and mitigation plan |
| Data and model | Source audit, month 2 snapshot, split, rule and ML evaluation |
| Integration | Validated batch output, offline HTML dashboard and manual review queue |
| Reporting | Project status report, options brief, steering slides and lessons |
| Handover | Source package, runbook, case study, acceptance checklist and CV material |

## Data and modelling choices

The supplied synthetic benchmark contains 4,000 projects and 72,549 project month observations. The IT cohort has 1,381 projects. A month 2 snapshot uses seven features from planned duration, budget, EV and AC. The fixed project split is 828 training, 276 validation and 277 test projects.

The comparison included Logistic Regression and Random Forest alongside a CPI rule. Validation average precision selected calibrated Random Forest depth 4. XGBoost was not a project requirement. Final outcomes and project identifiers were excluded as predictors. PV, SPI and SV were excluded after data concerns were identified. Baseline freeze and semantic feature availability remain unproven, so G01 remains HOLD.

## Results at the chosen capacity

At 20% review capacity, 56 of the 277 test projects enter the priority list. Random Forest finds 44 late cases compared with 39 from the CPI rule. Precision is 78.57% and recall is 23.40%. There are 188 late cases in the test set, so 144 remain outside the RF queue.

The five additional cases are an internal synthetic test result. The bootstrap interval for the recall difference spans zero. I therefore retain an inconclusive comparison rather than claiming the AI is operationally superior. Diagnostic recall at a 0.5 threshold is 93.09%, but it requires 253 alerts and does not describe the selected capacity of 56.

## PMO decisions and control of change

The dashboard output changed to HTML by user direction. The earlier Power BI package is superseded, and the original baseline remains part of the history. The current package does not claim an agreed revised effort or cost baseline for that change.

The budget uses simulated company allocations. At the original simulated cutoff, EAC exceeds BAC by Rp400,185, or 2.03%. Those numbers are not personal expenditure or an updated forecast after every later change. Option B proposes a bounded data review first. Its gross effort estimate is not automatically added to EAC because the old Base scenario already contains rework allowances.

## What is available and what remains open

The HTML supports filtering, search, ranking, project details, scenario comparison, CSV import and export, and a review queue requiring manual evidence. The existing evidence records 21 DOM interaction checks and full notebook execution with simulated Colab upload and download. These checks do not constitute owner UAT in Windows.

Open items include feature availability evidence, owner UAT, the net cost and schedule effect of scope changes, and formal package acceptance. Lessons and current RAID are in the governance folder. No operational cost saving, reduction in delays, production rollout or real company stakeholder approval is claimed.

## Why this is relevant to a PMO role

This case demonstrates a PMO decision to keep an attractive AI demo within its evidence limits, compare options at the same review workload, preserve the baseline when tools change, and produce a traceable handover. The main outcome is a usable management and demonstration package with explicit unresolved decisions.
