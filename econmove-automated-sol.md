# EcoMove Solutions: Automation strategy to speed up the assignment

Yes. A substantial part of this assignment can be automated, particularly the repetitive work involved in preparing data, validating task dependencies, calculating costs, creating tasks in Monday.com, checking resource allocations and generating reports.

My recommendation is to build a semi-automated workflow using Excel + Monday.com + Power Automate or Make, with human approval at the key decision points. This avoids manually entering the same information multiple times and reduces the risk of incorrect dates, missing dependencies and inconsistent cost calculations.

## 1. Which parts of the assignment can be automated?

### 01

Excel data preparation and validation

High

Automatically validate task IDs, predecessors, durations, resource hours, hourly rates and fixed costs before import.

### 02

Task creation and data import

High

Create Monday.com items from a validated spreadsheet using supported imports, an integration platform or the API.

### 03

Resource and cost calculations

High

Calculate labour costs, fixed costs, task totals and the project budget from a single source of truth.

### 04

Dependency and schedule validation

High

Detect missing predecessors, circular dependencies, invalid dates and tasks scheduled before their prerequisites.

### 05

Resource-overallocation alerts

Medium–High

Compare planned daily hours against the 7-hour capacity and flag possible conflicts for review.

### 06

Progress tracking and notifications

High

Notify owners about overdue tasks, blocked activities, approaching deadlines and milestone changes.

### 07

Reporting and baseline comparisons

Medium–High

Generate regular status summaries and compare current dates and costs with approved baseline values.

### 08

Critical-path analysis and resource leveling

Medium

Calculate the critical path and propose scheduling changes, subject to validation of calendars, task durations and resource constraints.

The key distinction is between automating calculations and repetitive actions, which is usually straightforward, and automating project-management decisions, which needs more care. For example, a script can identify an overloaded resource, but automatically moving tasks can create new dependency conflicts or delay the launch.

## 2. Recommended automation architecture

Step 1 — Excel preparation template

Master task data, resources, hours, costs and project calendar

Step 2 — Automated validation

Check missing fields, IDs, dependencies, hours, costs and schedule logic

Step 3 — Human approval

Approve the data and initial schedule before creating or updating records

Step 4 — Automation connector

Power Automate, Make, or a small API integration

Step 5 — Monday.com project board

Tasks, owners, dates, dependencies, status and cost fields

Step 6 — Monitoring and reporting

Alerts, workload checks, schedule changes and baseline comparisons

This architecture uses Excel as the preparation layer, Monday.com as the operational project platform and the connector as the bridge between them. The connector should transfer validated data rather than independently calculate competing versions of the schedule or budget.

## 3. The highest-value automation: one-click project setup

For this assignment, I would implement the following process first. It automates the data-heavy parts without trying to automate every project-management decision.

### Workflow A — Validate, calculate and import

Trigger: Laura clicks “Validate and prepare project” in the Excel template.

1. Read the Excel tables

Read the 13 tasks, resource assignments, rates and fixed costs.

2. Run automated validation

Reject duplicate task IDs, unknown predecessor IDs, missing fields, negative durations, invalid resource names and circular dependencies.

3. Calculate the project plan

Calculate labour costs, fixed costs, earliest start/finish dates, total duration, critical path and estimated budget.

4. Display a validation report

Show all errors and warnings, including potential resource conflicts. Require approval before import.

5. Create or update Monday.com items

Transfer the approved task data, map task IDs to Monday.com item IDs, and configure the dependencies.

6. Reconcile the result

Confirm all 13 tasks exist, dependencies are linked, and cost totals agree with the approved Excel data.

Monday.com supports creating items and updating dependency columns through its API. The dependency API uses the actual Monday.com item IDs, so the integration must first create the tasks, store the mapping between your Excel task IDs and Monday.com item IDs, and then link the dependencies. monday.com Developer Platform

+1

This is the key technical detail that prevents one of the most common import errors: treating a predecessor code such as `6` as if it were already the Monday.com item ID.

### Workflow B — Automatic progress monitoring

Once the board is configured, use Monday.com automations or a connector to monitor changes.

| Trigger | Automated action |
| --- | --- |
| Task is marked complete | Notify the next task owner that a prerequisite is complete |
| Due date approaches | Notify the assigned owner |
| Due date passes and task is incomplete | Alert Laura |
| Status changes to Blocked | Notify Laura and the relevant owner |
| Actual cost exceeds budget | Flag the task for review |
| Forecast launch date changes | Notify the project team and record the change |
| Weekly reporting time arrives | Generate a project status summary |

For dependencies, use the platform's native dependency features wherever possible rather than rebuilding dependency logic in a separate automation. Monday.com documents that dependencies can be visualized in Gantt views and used in timeline and date-based automations. Availability of particular features depends on the plan. monday.com Developer Platform

+1

## 4. Which tools should you use?

Microsoft sharepoint 2025 Icone, loghi, simboli – Download gratuito PNG, SVG

Option 1 — Excel + Monday.com native features

Best starting point

Prepare the dataset with Excel formulas, validation rules and conditional formatting. Import the tasks, then configure dependencies, resource assignments and reporting in Monday.com.

- Lowest technical complexity.
- Ideal for a 13-task academic assignment.
- Some dependency setup and resource analysis may remain manual.

File:Microsoft Power Automate.svg - Wikimedia Commons

Option 2 — Excel + Power Automate + Monday.com

Best for a Microsoft-based workflow.

Trigger a flow from an approved Excel dataset, validate records, and create or update Monday.com items through a suitable connector or HTTP/API integration.

- Useful for repeatable imports and notifications.
- Requires configuration, authentication and possibly a premium connector or API access.
- Excel connector limitations and retry behaviour must be considered to prevent duplicate records. Microsoft Learn
  +1

Logo Make – Logos PNG

Option 3 — Excel + Make + Monday.com API

Best for a visual integration workflow.

Use a scenario to read approved task rows, create items, save their IDs, link dependencies, and send error notifications.

- Easier to visualize a multistep integration.
- Useful when importing or updating data repeatedly.
- Requires scenario configuration, testing and appropriate access to both platforms.

GitHub - thevkrant/morse\_code: Morse code is a method of transmitting text information as a series of on-off tones lights or clicks that can be directly understood by a skilled listener or observer without special equipment. It is named for Samuel F. B. Morse. Every character in the English language is substituted by a series of dots and dashes or something just singular dot or dash. · GitHub

Option 4 — Python + Monday.com API

Best for custom scheduling logic.

Build a script that validates the project network, calculates earliest and latest dates, identifies the critical path, flags capacity conflicts, and sends approved data to Monday.com.

- Greater control over scheduling calculations.
- Suitable for repeatable project-planning assignments.
- Requires coding, API credentials and maintenance.

For this assignment, I would start with Option 1 if the objective is to complete the coursework quickly. If the objective is to demonstrate a more sophisticated automation solution, Option 2 or Option 3 is a better project to present. Choose one integration route rather than implementing several overlapping workflows.

## 5. Important safeguards to prevent automation errors

Automation only reduces errors when the process is designed to detect and handle them. I recommend implementing these controls from the beginning.

| Risk | Recommended control |
| --- | --- |
| Duplicate task creation | Use the Excel task ID as a unique external key and update existing items instead of blindly creating new ones. |
| Broken dependencies | Create all tasks first, map IDs, then link predecessors and verify the links. |
| Incorrect costs | Calculate against a single resource-rate table and reconcile the total with €17,567. |
| Incorrect dates | Use one defined working calendar, with weekends and applicable holidays excluded. |
| Resource over-allocation | Validate daily hours against each employee's 7-hour capacity. |
| Unintended rescheduling | Require approval before applying resource-leveling changes. |
| API or connector failure | Log failed records, retry safely and reconcile the final task count. |
| Baseline overwritten | Preserve a read-only approved baseline and record subsequent changes separately. |

One further technical safeguard is important: make the integration idempotent. This means running the workflow twice should not create 26 tasks instead of 13. Before creating a task, the automation should check whether its external task ID is already mapped to an existing Monday.com item. Excel connector documentation also warns about delayed updates and duplicate insertions under certain retry conditions. Microsoft Learn

+1

## 6. A practical implementation plan for the assignment

Step 1

Build the Excel template

Create task, resource, cost and calendar tables; add formulas and validation rules.

Step 2

Automate the checks

Validate IDs and dependencies, calculate the budget and initial schedule, and flag possible resource conflicts.

Step 3

Configure Monday.com

Create the board, columns, groups, resource assignments, dependencies and Gantt view.

Step 4

Automate data transfer

Use a supported import or connector/API to create and update tasks, then reconcile all records.

Step 5

Add monitoring and reporting

Configure deadline alerts, blocked-task notifications, weekly reporting and baseline comparisons.

Step 6

Test and document

Run a test import, simulate a failure, check duplicate prevention, verify totals and save the approved baseline.

## 7. How to demonstrate the automation in your submission

To make the assignment more convincing, demonstrate a small, working proof of concept rather than simply describing automation.

I would demonstrate three scenarios:

1. Successful import: the 13 tasks are created, the dependencies are linked and the total budget reconciles to €17,567.
2. Error detection: deliberately enter a nonexistent predecessor ID and show that the validation process blocks the import.
3. Monitoring: mark a task as blocked or overdue and show that the responsible person receives a notification.

Measure the results using:

- Time required to prepare and enter the project.
- Number of manual data-entry steps eliminated.
- Number of validation errors caught before import.
- Number of duplicate or incorrectly linked tasks.
- Agreement between the Excel budget and Monday.com budget.

These measures allow you to explain the actual benefits of automation without claiming unmeasured time savings.

## Final recommendation

For EcoMove Solutions, the best balance of speed, reliability and complexity is:

Excel validation template → approval gate → automated Monday.com import → native dependency and status automations → automated reporting → approved baseline.

Automate repetitive data handling, calculations, validation and notifications first. Keep resource leveling, schedule changes and baseline approval under human control until the workflow has been thoroughly tested.

That approach will speed up the assignment while making the resulting project plan easier to verify, explain and maintain.
