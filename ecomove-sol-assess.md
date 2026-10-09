# Assessment of the Monday.com-generated EcoMove Solutions project

Based on the report you provided, the Monday.com AI has created a substantial part of the project solution, but the report does not demonstrate that the assignment is fully complete.

The strongest parts are the task structure, resource-rate model, fixed costs and dependency network. The main concerns are the unresolved resource-leveling issue, the inconsistent completion and milestone dates, and the absence of evidence that the required reports and baseline have actually been generated and saved.

One important limitation: I can assess the report against the assignment requirements, but I cannot directly inspect your Monday.com board from this report alone. A feature described in the summary is not necessarily configured correctly in the board.

## 1. Assessment against all 14 assignment requirements

Assessment based on the generated summary, rather than independent inspection of the live board.

| # | Assignment requirement | Assessment | Reason |
| --- | --- | --- | --- |
| 1 | Enter all project information and activities | Likely met | All 13 activities are listed across three phases. Verify their descriptions, durations and assignments in the board. |
| 2 | Define predecessors and dependencies | Likely met | The report states that dependencies are linked. Verify every predecessor, particularly Tasks 9 and 12, which each have two predecessors. |
| 3 | Create three resources and assign hourly rates | Partially evidenced | The rates and hours are reported, but it does not confirm that Laura, Marc and Clara are configured as actual Monday.com users or resources with usable cost rates. |
| 4 | Assign resources to activities | Partially evidenced | Resource totals are provided, but the report does not show all task-level assignments or prove that the People and hours columns are configured correctly. |
| 5 | Enter fixed costs | Likely met | Both fixed costs are identified, but verify that €8,000 is assigned to Task 6 and €4,500 to Task 12 in the actual board. |
| 6 | Obtain the overall project schedule | Needs verification | A schedule is reported, but the 13 November campaign completion and 16 November launch milestone need to be reconciled. |
| 7 | Generate the Gantt chart | Likely met | The report states that the Gantt view is active. Confirm that bars, dates and dependency links are visible. |
| 8 | Identify the critical path | Needs verification | A critical-path chain is reported, but there is no evidence that the Gantt critical-path feature is enabled or that the chain remains critical after leveling. |
| 9 | Review resource allocation | Partially evidenced | The report identifies a capacity issue in Task 2, but does not show a complete workload review for all three employees. |
| 10 | Detect resource overallocations | Partially met | One conflict is identified. The report does not establish that every task and every employee has been checked. |
| 11 | Apply resource leveling | Not demonstrated | Extending Task 2 is proposed as an option; the report does not confirm that the change has actually been applied. |
| 12 | Calculate project duration and budget | Partially met | The budget is internally consistent, but the final duration is not reconciled with the milestone date or resource leveling. |
| 13 | Generate a project report | Not demonstrated | A solution summary is not proof that a formal project report or dashboard has been generated. |
| 14 | Save a baseline for future monitoring | Not demonstrated | The report says a baseline can be saved anytime. That does not mean a baseline snapshot already exists. |

Overall verdict: the board appears substantially configured, but I would not yet submit it as a fully completed assignment. Requirements 11, 13 and 14 are the clearest outstanding items; several others need direct verification.

## 2. The three most important issues to fix

### Issue 1 — Resource leveling has been proposed, not completed

The report explicitly says:

> “Leveling Strategy: Extend Task 2 by +1 day … or shift non-critical parallel tasks…”

This is a recommendation, not evidence of an implemented change.

Task 2 requires 32 hours from Laura over four working days. At a maximum capacity of 7 hours per day, Laura can supply only 28 hours during that period.

If you extend Task 2 to five working days, her average allocation becomes:

$$
32/5=6.4\text{ hours/day}
$$

That resolves the average-capacity problem for Task 2, assuming an even workload distribution. But it also changes the schedule and may affect the critical path.

The report must therefore be updated to show:

- Task 2's revised duration and dates.
- Recalculated dates for Tasks 3 and 4 and their successors.
- The revised critical path and completion date.
- A fresh workload check for Laura, Marc and Clara.

Simply stating that leveling is possible does not satisfy requirement 11.

### Issue 2 — The project finish date is inconsistent

The report states:

- Overall project duration: 30 working days.
- Final campaign completion: Friday, 13 November 2026.
- Operational launch milestone: Monday, 16 November 2026.

The milestone occurs one working day after the campaign completion, with the weekend in between. This may be intentional if the operational launch is scheduled for the next working day, but it needs to be reflected consistently in the project plan.

Under the conventional scheduling interpretation where the zero-duration milestone occurs immediately upon completion of Task 12, the milestone would normally be on 13 November. If Monday.com is deliberately scheduling it for 16 November, verify the dependency configuration and the date shown on the actual milestone item.

There is also a resource-leveling implication: if Task 2 is extended by one day, the project schedule must be recalculated. The report cannot simply retain the original critical-path dates without showing that the revised plan has been checked.

### Issue 3 — The baseline has not necessarily been saved

The report says:

> “You can snapshot the baseline anytime…”

That describes a capability, not a completed action.

Requirement 14 asks you to save a baseline for future monitoring. You should verify that a named baseline snapshot exists in the Gantt view.

If no baseline exists, save one only after approving the revised schedule and budget. A baseline captured before resolving the resource conflict would preserve an initial plan that is already known to have a capacity issue.

The same principle applies to requirement 13: a dashboard or report should actually exist, rather than merely being described as a possible next step.

## 3. Check the financial figures

The reported financial calculations are correct based on the original assignment.

| Budget component | Reported amount | Assessment |
| --- | --- | --- |
| Laura's labour | €2,905 | Correct |
| Marc's labour | €1,452 | Correct |
| Clara's labour | €336 | Correct |
| Total labour | €4,693 | Correct |
| Charging stations | €8,000 | Correct |
| Advertising | €4,500 | Correct |
| Total project budget | €17,193 | Correct |

The three resource totals also reconcile to 177 hours.

One additional check is needed: the phase costs add up to €17,193, so they are consistent with the overall budget. However, the report does not show how those phase costs are calculated or whether they are automatically linked to task-level cost formulas. Verify that the costs are calculated rather than manually entered summary figures.

## 4. What to do directly in Monday.com

Follow this checklist to finish the assignment.

## Final completion checklist

0/10

A. Verify project setup

[ ]Confirm all 13 tasks and their durations are present.

[ ]Check the three resource profiles, hourly rates and task-level hours.

[ ]Verify both fixed costs are assigned to the correct tasks.

[ ]Confirm the dependency links for Tasks 9, 12 and 13.

B. Correct the schedule

[ ]Extend Task 2 to five working days, or implement another justified capacity solution.

[ ]Recalculate dependent task dates and the critical path.

[ ]Resolve whether the operational launch is 13 November or 16 November.

[ ]Recheck all three employees' daily workloads after leveling.

C. Complete the deliverables

[ ]Verify the Gantt chart and critical-path visualization.

[ ]Create a project dashboard or formal report with schedule, budget and progress.

[ ]Save a named baseline snapshot after approving the final plan.

[ ]Verify that the baseline exists and can be used for future comparisons.

## 5. What I would request from Monday.com AI next

Rather than asking it to create more features immediately, ask it to audit and complete the existing board, preserving the work already done.

Writing

Please audit the existing “EcoMove Solutions - Project Launch” board against all 14 requirements of the project management assignment.

Do not create a duplicate board or duplicate tasks.

1. Verify that all 13 tasks, durations, predecessor links, resource assignments, hourly rates and fixed costs match the original assignment.
2. Confirm that total resource effort is 177 hours, labour cost is €4,693, fixed costs are €12,500 and total budget is €17,193.
3. Resolve the Task 2 capacity conflict by implementing an appropriate leveling solution, not merely recommending one.
4. Recalculate the schedule, critical path and milestone date after leveling. Explain any difference from the initial schedule.
5. Check daily workload for Laura, Marc and Clara against the 7-hour daily capacity.
6. Verify that the Gantt chart displays the dependency links and critical path.
7. Create a project dashboard or formal report covering schedule, progress, resources and costs.
8. Save an actual baseline snapshot named “EcoMove_Approved_Baseline” after the schedule has been validated.
9. Report which of the 14 requirements are completed, which are incomplete, and which could not be verified.

Do not claim that an action has been completed unless it has actually been performed. Clearly identify any feature that is unavailable under the current Monday.com plan.

## Final conclusion

The generated solution is a good starting point, and its resource totals and preliminary budget are correct. But the summary alone does not prove that every assignment requirement has been fulfilled.

The most important remaining work is to implement resource leveling, reconcile the launch milestone date, generate the actual report and save the baseline. Once those actions are completed and verified on the board, the solution will be much closer to a defensible, submission-ready project management assignment.
