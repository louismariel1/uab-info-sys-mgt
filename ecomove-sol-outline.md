# EcoMove Solutions — Monday.com Project Management Assignment

## TD1: Excel data preparation phase to accelerate Monday.com data entry

The recommended approach is to prepare and validate all project information in Excel before importing it into Monday.com. This reduces manual data entry, minimizes errors in dependencies and resource assignments, and makes it easier to calculate the schedule and budget.

### 1. Proposed Excel workbook structure

Create one Excel workbook named `EcoMove_Project_Preparation.xlsx`, containing five worksheets.

Sheet 1 — Tasks

Master task register for importing into Monday.com.

Task ID, task name, duration, predecessor IDs, assigned resources, planned start, planned finish, task type, status and notes.

Sheet 2 — Resources

Resource register and hourly rates.

Resource ID, name, role, hourly rate and working calendar.

Sheet 3 — Costs

Labour costs and additional project expenses.

Task ID, resource, planned hours, hourly rate, calculated labour cost, fixed cost and total task cost.

Sheet 4 — Calendar

Scheduling rules and non-working days.

Project start, working days, working hours, public holidays and the August closure.

Sheet 5 — Validation & Summary

Quality checks and management overview.

Missing values, duplicate IDs, invalid predecessors, task totals, labour costs, fixed costs and estimated budget.

### 2. Prepare the task register

The following is the proposed master dataset, based on the assignment. It is suitable for preparing a Monday.com import file.

| ID | Task | Duration (days) | Predecessors | Laura (h) | Marc (h) | Clara (h) |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Define business requirements | 3 | — | 18 | 0 | 0 |
| 2 | Prepare business plan | 4 | 1 | 32 | 0 | 0 |
| 3 | Identify potential locations | 5 | 2 | 10 | 0 | 0 |
| 4 | Sign lease agreement | 1 | 3 | 2 | 0 | 1 |
| 5 | Contact equipment suppliers | 4 | 2 | 0 | 8 | 2 |
| 6 | Purchase charging stations | 2 | 5 | 0 | 6 | 2 |
| 7 | Purchase office equipment | 2 | 4 | 0 | 4 | 3 |
| 8 | Hire installation subcontractor | 3 | 4 | 4 | 0 | 4 |
| 9 | Install office infrastructure | 4 | 6, 7 | 0 | 16 | 0 |
| 10 | Develop marketing materials | 5 | 8 | 5 | 12 | 10 |
| 11 | Sign municipal agreements | 3 | 9 | 8 | 0 | 2 |
| 12 | Launch promotional campaign | 8 | 10, 11 | 4 | 20 | 4 |
| 13 | Operational launch | Milestone | 12 | 0 | 0 | 0 |

Important data-preparation rule: the duration is expressed in working days, whereas resource assignments are expressed in hours. Keep these as separate fields. The sum of resource hours does not necessarily equal the task duration multiplied by the daily working hours, because the hours in the assignment represent planned effort rather than necessarily full-time allocation.

### 3. Prepare the resource and cost registers

| Resource | Role | Hourly rate |
| --- | --- | --- |
| Laura | Project Manager | €35 |
| Marc | Technical Specialist | €22 |
| Clara | Administrative Assistant | €12 |

Use Excel formulas to calculate labour costs.

For example, if the columns contain Laura's hours, Marc's hours and Clara's hours, the labour-cost formula for a task is:

excel
```
=Laura_Hours*35+Marc_Hours*22+Clara_Hours*12
```

Calculate the project labour budget from the supplied effort data:

| Resource | Total hours | Labour cost |
| --- | --- | --- |
| Laura | 93 | €3,255 |
| Marc | 66 | €1,452 |
| Clara | 30 | €360 |
| Total | 189 | €5,067 |

Add the fixed costs separately:

| Fixed-cost item | Amount |
| --- | --- |
| Charging stations (Task 6) | €8,000 |
| Advertising campaign (Task 12) | €4,500 |
| Total fixed costs | €12,500 |

The preliminary total project budget is therefore:

$$
€5,067+€12,500=\boxed{€17,567}
$$

This is the budget calculated from the supplied labour hours and fixed costs, before any additional costs or changes resulting from resource leveling.

### 4. Validate the Excel dataset before importing

Use data validation, conditional formatting and formulas to detect errors before moving the data to Monday.com.

- Unique task IDs: every task must have a unique identifier.
- Valid predecessors: predecessor IDs must exist and must not refer to the same task or create circular dependencies.
- Valid resource names: use consistent names such as Laura, Marc and Clara.
- Numeric fields: durations, hours and costs must be stored as numbers, not text.
- Cost checks: the resource-hour totals should match the original assignment.
- Milestone check: Task 13 should have zero duration.
- Calendar check: exclude weekends and account for the August holiday closure if the schedule reaches that period.
- Dependency check: Task 9 must wait for both Tasks 6 and 7, while Task 12 must wait for both Tasks 10 and 11.

### 5. Import into Monday.com efficiently

1. Export the validated task worksheet to CSV or use Monday.com's supported Excel import workflow.
2. Create the project board and map Excel columns to Monday.com columns: task name, task ID, duration, dates, owner, status, cost and other relevant fields.
3. Import the task list first. Create or confirm the resource directory and assign the people to tasks.
4. Configure dependencies after the tasks have been imported, using task IDs to identify predecessors.
5. Enter the hourly rates and fixed costs in appropriate columns, formulas or connected cost-tracking tools.
6. Verify a sample of imported tasks and compare the resulting task count, hours and budget with Excel before continuing.

Recommendation: treat Excel as the preparation and validation layer, and Monday.com as the project execution and monitoring platform. Do not assume that importing a CSV automatically creates all dependencies, resource-rate settings, formulas or a project baseline; verify these features in the Monday.com plan and import workflow being used.

## TD2: Comprehensive solution outline and project roadmap

The second objective is to transform the prepared data into a complete project plan in Monday.com, from project setup through scheduling, cost control, resource leveling and baseline monitoring.

## 1. End-to-end implementation roadmap

Phase 1 — Prepare the data

TD1

- Create the Excel workbook and validate all 13 tasks.
- Verify the resource hours, hourly rates, predecessor IDs and fixed costs.
- Approve the initial scope and budget assumptions.

Deliverable: validated import-ready dataset.

Phase 2 — Create the Monday.com workspace

- Create an EcoMove Solutions workspace and project board.
- Import the tasks and configure task ID, duration, dates, owner, status, effort and cost columns.
- Create or invite Laura, Marc and Clara as appropriate.

Deliverable: structured project board.

Phase 3 — Configure scheduling logic

- Enter the project start date: 5 October 2026.
- Configure the Monday–Friday working calendar and 7-hour workday.
- Link predecessors and successors.
- Define the operational launch as a milestone.

Deliverable: dependency-driven project schedule.

Phase 4 — Resource and budget setup

- Record the three hourly rates.
- Assign the specified hours to each resource.
- Enter the €8,000 charging-station cost and €4,500 advertising cost.
- Check concurrent assignments and calculate the project budget.

Deliverable: resource and cost plan.

Phase 5 — Analyze and optimize the schedule

- Generate the Gantt chart.
- Identify the critical path and project completion date.
- Review workload conflicts.
- Apply resource leveling and recalculate dates.

Deliverable: feasible, optimized schedule.

Phase 6 — Reporting and baseline

- Review the schedule, cost and resource reports.
- Obtain approval of the final plan.
- Save the approved baseline or an equivalent frozen reference plan.
- Monitor actual progress against the approved plan.

Deliverable: approved project plan and monitoring framework.

## 2. Recommended Monday.com board structure

Use a main project board with one item per task. Suggested groups are:

- Business planning: Tasks 1–3.
- Premises and procurement: Tasks 4–9.
- Marketing and agreements: Tasks 10–11.
- Launch: Tasks 12–13.

Recommended columns:

| Column | Monday.com purpose |
| --- | --- |
| Task ID | Unique task reference |
| Task name | Activity description |
| Duration | Planned working days |
| Start date | Planned start |
| Due date | Planned finish |
| Dependency | Predecessor tasks |
| People | Responsible team member(s) |
| Status | Not started, Working on it, Done, Blocked |
| Planned effort | Hours assigned to each resource |
| Labour cost | Calculated personnel cost |
| Fixed cost | Additional non-labour cost |
| Total cost | Labour cost + fixed cost |
| Notes | Assumptions, risks and deliverables |

For tasks involving multiple employees, either use a People column plus a separate effort/cost breakdown, or maintain a connected resource-allocation board. A single People column alone does not necessarily capture individual hours or costs.

## 3. Build the dependency network

The dependency structure must be completed before trusting the Gantt chart or completion date.

Business planning

1 → 2 → 3

Premises and procurement

3 → 4 → 7 → 9

2 → 5 → 6 → 9

4 → 8 → 10

Agreements and promotion

9 → 11

10 and 11 → 12

Task 13 — Operational launch milestone

The important logic is that:

- Task 9 cannot start until Tasks 6 and 7 are both complete.
- Task 12 cannot start until Tasks 10 and 11 are both complete.
- Task 13 occurs when Task 12 is complete.

In Monday.com, verify that each dependency represents the intended finish-to-start relationship. The board should not merely contain predecessor numbers as text; the dependencies must be configured as actual links if they are to drive scheduling.

## 4. Calculate the initial schedule and critical path

Assuming the durations are working days, the project starts on Monday, 5 October 2026, and no public holidays are excluded beyond weekends, the initial schedule can be calculated as follows.

| Task | Planned start | Planned finish |
| --- | --- | --- |
| 1 | 5 Oct 2026 | 7 Oct 2026 |
| 2 | 8 Oct 2026 | 13 Oct 2026 |
| 3 | 14 Oct 2026 | 20 Oct 2026 |
| 4 | 21 Oct 2026 | 21 Oct 2026 |
| 5 | 14 Oct 2026 | 19 Oct 2026 |
| 6 | 20 Oct 2026 | 21 Oct 2026 |
| 7 | 22 Oct 2026 | 23 Oct 2026 |
| 8 | 22 Oct 2026 | 26 Oct 2026 |
| 9 | 26 Oct 2026 | 29 Oct 2026 |
| 10 | 27 Oct 2026 | 2 Nov 2026 |
| 11 | 30 Oct 2026 | 3 Nov 2026 |
| 12 | 4 Nov 2026 | 13 Nov 2026 |
| 13 | 13 Nov 2026 | 13 Nov 2026 |

These are the initial earliest-start dates, before resource leveling. Dates should be recalculated if public holidays are included in the project calendar.

### Critical path

The initial critical path is:

1 → 2 → 3 → 4 → 7 → 9 → 11 → 12 → 13

Initial project duration

# 30 working days

Initial completion date

# 13 Nov 2026

The critical path has zero total float under the initial dependency-driven schedule. Any delay to a critical activity can delay the operational launch unless the schedule is recovered.

For the assignment, use Monday.com's Gantt view and critical-path functionality if supported by your plan. Otherwise, calculate the critical path using the forward-pass and backward-pass method in Excel and identify the corresponding tasks on the Gantt chart.

## 5. Review resource allocation and apply resource leveling

Resource leveling is an important step because a dependency-feasible schedule is not necessarily a resource-feasible schedule.

Potential conflicts in the initial schedule include:

| Period | Overlapping tasks | Resources potentially affected |
| --- | --- | --- |
| 22–23 Oct | Tasks 7 and 8 | Clara |
| 27 Oct–2 Nov | Task 10 overlaps Task 11 from 30 Oct | Laura and Clara |

These are potential conflicts, not proof of over-allocation. The assignment gives total hours per task, but not the daily distribution of those hours. Since each employee has a 7-hour working day, daily allocations must be checked before confirming whether capacity is exceeded.

### Recommended leveling procedure

1. Open the workload or resource-management view.
2. Review Laura's, Marc's and Clara's assignments across the overlapping periods.
3. Compare daily allocated hours with the 7-hour daily capacity.
4. Move flexible work, redistribute work where appropriate, or split work across available days.
5. Preserve all predecessor relationships and task durations.
6. Recalculate the schedule, critical path, project finish date and resource costs.
7. Record the revised completion date and explain any delay introduced by leveling.

Example: Tasks 10 and 11 overlap for two working days, 30 October and 2 November. If Laura or Clara cannot complete their assigned effort within their daily capacity, some of Task 10's work could be moved to later days. However, because Task 12 depends on both tasks, any delay to Task 10 beyond Task 11's completion could delay the launch.

Do not automatically shift an entire task merely because two tasks overlap. First determine whether the assigned hours can be completed within the available capacity. The best leveling solution is the one that resolves actual capacity conflicts while minimizing the impact on the critical path.

## 6. Calculate the budget and configure cost tracking

The initial project budget is calculated as follows.

Personnel costs

## €5,067

Fixed costs

## €12,500

Total initial budget

# €17,567

Based on the supplied resource hours and fixed costs, excluding any unspecified expenses.

Configure the following calculations:

- Labour cost = sum of each resource's assigned hours multiplied by their hourly rate.
- Task total cost = labour cost + fixed cost.
- Project budget = sum of all task total costs.

Use separate cost fields for charging stations and advertising so that these costs are not accidentally included twice.

After resource leveling, compare the initial and revised budgets. If the same work and assigned hours are retained, the labour budget should remain €5,067. If extra effort or external costs are introduced, update the estimate accordingly.

## 7. Generate the Gantt chart and project reports

The Gantt chart should display:

- All 13 tasks, including the launch milestone.
- Start and finish dates.
- Task durations.
- Predecessor links.
- Parallel activities.
- The critical path, where available.
- Baseline dates and current forecast dates, where supported.

Recommended reports and dashboards:

| Report | Main purpose |
| --- | --- |
| Project timeline | Review sequence, duration and launch date |
| Critical-path report | Identify activities that control completion |
| Resource workload report | Identify over-allocation and unused capacity |
| Cost report | Compare planned, actual and forecast costs |
| Task-status report | Track completed, ongoing and blocked activities |
| Milestone report | Monitor key approvals and operational launch |

Monday.com's available formulas, workload features, Gantt options and baseline capabilities depend on the product plan and configuration. If a required feature is unavailable, use a connected board, dashboard or Excel calculation rather than assuming the feature is included.

## 8. Save the project baseline

A baseline is the approved reference plan against which actual performance will be measured.

Before saving it:

1. Validate the dependency network.
2. Approve the resource assignments and hourly rates.
3. Confirm the project calendar and planned dates.
4. Review the critical path and the effect of resource leveling.
5. Approve the final budget and completion date.
6. Save or freeze the approved schedule and budget using the baseline capability available in Monday.com, or preserve an equivalent reference snapshot.

During execution, update actual start and finish dates, task status, actual effort and costs. Compare these against the baseline to identify schedule delays and budget variances.

Useful indicators include:

- Schedule variance: actual or forecast progress compared with the baseline.
- Cost variance: budgeted cost compared with actual cost.
- Resource variance: actual assigned workload compared with capacity.
- Milestone variance: difference between the baseline launch date and current forecast launch date.

A baseline should not be overwritten every time the plan changes. Approved changes should be documented so that the original plan remains available for comparison.

## 9. Final deliverables checklist

## Submission checklist

0 of 12

[ ]Excel workbook with validated task, resource and cost data

[ ]Monday.com project board containing all 13 tasks

[ ]Three resource profiles and hourly rates

[ ]Configured task dependencies and working calendar

[ ]Resource assignments and fixed costs

[ ]Initial Gantt chart and project schedule

[ ]Critical-path analysis

[ ]Resource-overallocation assessment

[ ]Resource-leveling changes and revised schedule

[ ]Project duration and budget calculation

[ ]Project reports and dashboard

[ ]Approved project baseline or frozen reference plan

## Conclusion

The most efficient solution is to use Excel for structured data preparation, validation and preliminary calculations, and Monday.com for dependency-driven scheduling, resource coordination, reporting and project monitoring.

The initial schedule indicates a 30-working-day project, with an expected operational launch on 13 November 2026, and a preliminary budget of €17,567. These figures should be treated as the initial planning estimates. The final approved dates and budget must be confirmed after validating the calendar, reviewing daily resource capacity, applying any necessary resource leveling and saving the baseline.
