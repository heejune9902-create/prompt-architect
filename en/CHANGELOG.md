# Changelog

## 2026-11-13 · prompt-architect v2

Incorporates material covered in the daily reports from 2026-10-12 through 2026-11-13. The catalog grows from 16 to 19 modules.

### New modules

| Module | Changes | Source reports |
| --- | --- | --- |
| M17 Tool exposure, call format, fallback paths | Narrow tools to 2–3 for a task. Separate the decision from its call expression; correct only the expression on a formatting error. Switch tools or source types after technical failures, but stop for permission issues or blocks. | 10/13 RATED (A), 10/16 Lost in Implicit Routing (P), 10/26 OpenDS-World (P), 11/02 MICA+DART (P), 11/12 SlackBench (A) |
| M18 Adjusting effort levels | Assess difficulty in one line. Revisit earlier judgments only for new information or errors, and start with low reasoning effort and few agents. | 10/12 RACE (P), 10/14 Competence-Aware Orchestration (P), 11/10 Claude Fable and Mythos 5.2 (C) |
| M19 Evidence-linked experience memory | Attach a source and success/failure label to each lesson. Reopen the source only when there is reason for doubt. Count memory-driven improvements and regressions separately. | 10/28 Memory Tax (P), 11/13 WikiTrace (P) |

### Strengthened guidance

- **M01**: An AI stopping on its own is not evidence of correctness. Report in one line what exceeded or fell short of the request. (10/26, 10/29)
- **M03**: Update only changed items, retaining judgments and conclusions. Keep only recent tool results verbatim, and extract what the next action needs. (10/20 CarryOn, 10/22 Cache Engineering, 11/11 Coca-Cola)
- **M04**: Score outcomes and process separately. Do not confuse plans with completed work; check for false premises. (10/19 BizBench, 10/27 TraceTrial, 11/12 SlackBench)
- **M06**: Add ablation tests, fix quality/cost trade-offs before testing, and keep weaker variants that address particular failures on a deferred list. (10/21 HarnessPro, 11/04 R²Orch, 11/06 ParetoSaddler, 11/09 Harness-S)
- **M07**: Add conditional automation, blocking when uncertain, and alternatives when refusing. Define four levels of intervention: observe, notify, suggest, execute. Restate scope at the start and add the previously missing check items. (10/29, 11/03 HALO, 11/05 LeanGuard)
- **Testing procedure**: Include inputs that only sometimes succeed. Count process violations, tool calls, and excessive blocking.
- **Other changes**: Add diagnosis items 16 and 17, five symptom-table rows, quality-gate items 16 and 17, and principle 12, "Start light." Add evidence grade **A** for peer-reviewed conference papers.

## 2026-10 · prompt-architect v1

Includes M01–M16, based on reports from 2026-09-21 through 2026-10-08.
