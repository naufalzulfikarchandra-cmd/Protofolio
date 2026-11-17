# AI Project Risk Monitoring

**PMO Risk Dashboard — independent portfolio simulation by Naufal Zulfikar Chandra, developed with AI assistance.**

This project demonstrates how a PMO can plan and govern an AI initiative, evaluate evidence and turn model outputs into a review workflow. The dashboard is an offline HTML application. The prediction engine remains an exploratory synthetic benchmark with operational gate **G01 HOLD**.

## Start here

1. Open `dashboard/Dashboard_PMO_HTML.html` in Chrome, Edge or Firefox. No installation or server is required for the recorded demo.
2. Read [the portfolio case study](portfolio/CASE_STUDY.md) for the problem, PMO decisions and results.
3. Read [the handover guide](handover/HANDOVER.md) and [runbook](handover/RUNBOOK.md) to navigate the package or reproduce a recorded workflow.
4. Review [open items](handover/OPEN_ITEMS.md) before accepting the deliverables.

## Recorded results

| Measure | Recorded value |
|---|---:|
| Synthetic source projects | 4,000 |
| Project month observations | 72,549 |
| Eligible IT project cohort | 1,381 |
| Held out test projects / late cases | 277 / 188 |
| Review capacity | 20% = 56 priorities |
| RF late cases found in top 56 | 44 |
| CPI rule late cases found in top 56 | 39 |
| RF precision / recall at 56 | 78.57% / 23.40% |
| Late cases outside the RF priority list | 144 |

The 95% paired bootstrap interval for the recall difference is −2.05 to +7.49 percentage points. It includes zero. The advantage is inconclusive and does not establish real world impact. Scores are provisional synthetic outputs rather than validated company risk probabilities.

## PMO scope

The eight work stages cover initiation, planning, budgeting, RAID and governance, model evidence, batch and HTML integration, reporting and decisions, and handover and portfolio preparation. The planning baseline has 28 tasks and 93 planned hours. Dates and company cost allocations are simulated. User acceptance remains separately recorded.

The budget snapshot uses IDR and a simulated cutoff of 27 January 2027. BAC is Rp19,739,881.625 and EAC Base is Rp20,140,066.625. The Rp400,185 forecast overrun is 2.03%. The snapshot has not been reforecast after the HTML change or net Option B effort. Source project budgets use USD and are not added to the implementation budget.

## Structure

| Folder | Content |
|---|---|
| `docs` | Prepared project documents and stage outputs, with owner review still pending |
| `governance` | Current RAID, gates, decision and lessons registers, with an original snapshot retained |
| `portfolio` | Case study, CV wording and interview preparation |
| `handover` | Runbook, acceptance checklist, open items and attribution |
| `dashboard` | Standalone HTML, template, embedded PMO snapshot and user guide |
| `code` | Existing training and batch engines and Colab notebooks |
| `data` | Original supplied synthetic data and demo inputs |
| `model` / `results` | Existing model artifact, protocol results, split and execution evidence |
| `artifacts` | Original user supplied Colab result ZIP |

## Status and next decision

Option B means reviewing data provenance and feature availability before deciding whether retraining is necessary. The proposed check is 6 Data hours plus 2 PMO review hours. It has not been executed. Changes to names or dashboard appearance alone do not require a new model. Owner browser UAT and acceptance remain open.

This package is a portfolio handover, not production approval. No company deployment, cash savings or reduction in project delays has been measured. Read [sources and rights](handover/SOURCES_AND_RIGHTS.md) before reuse. No new blanket software license is granted by this README.
