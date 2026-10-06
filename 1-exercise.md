# Project Management Exercise
Absolutely. This exercise is essentially asking you to **build, schedule, staff, cost, and then control a project in Monday.com**. The key concepts are **precedence, duration, resources, workload/overload, cost, Gantt, and baseline vs. actual performance**.

 ## 1\. What is the project about?

 Andrea and her partners are creating **AldeNat**, a company that distributes dietary and natural products.

 Before the company can start operating, several activities must be completed:

 - Find and prepare an office.
- Buy computers and furniture.
- Buy initial products and office complements.
- Review everything.
- Contact suppliers.
- Prepare marketing.
- Finally, start the business.

 The project begins on **Monday, September 28, 2026**.

 There are three available workers:

 | Person | Role | Cost/hour | Working hours |
| --- | --- | --- | --- |
| Andrea | Owner | €30/h | 09:00–17:00 |
| Anna | Commercial | €15/h | 09:00–17:00 |
| Berta | Administrative | €6/h | 09:00–17:00 |

Everyone works **8 hours per day, Monday–Friday**.

---

 # 2\. Understanding the activity table

 The most important columns are:

 - **Code** → task number.
- **Description** → what needs to be done.
- **Duration** → how many working days the task takes.
- **Prec.** → predecessor: the task(s) that must finish before this task can begin.
- **Owner / Com. / Adm.** → how many hours each employee must work on the task.

 For example:

 ### Task 2 — Prepare budget

 It says:

 > Duration = 3 days\
>  Predecessor = 1\
>  Andrea = 30h

 This means:

 **Task 1 must finish → then Task 2 can start.**

 And Andrea has to work **30 hours** on Task 2.

 Since Andrea works 8 hours/day:

 $$
30h / 8h/day = 3.75\text{ days}
$$

 This is important because the task's **duration is 3 days**, but Andrea's assigned work is **30 hours**.

 In a project-management program such as Monday.com, you need to distinguish between:

 - **Task duration:** 3 days
- **Work/resource effort:** 30 hours

 They are related, but they are not necessarily the same thing.

---

 # 3\. First thing to do: create the project structure

 You would create the following tasks in Monday.com:

 | # | Task | Duration | Predecessor |
| --- | --- | --- | --- |
| 1 | Determine space needs | 2 days | — |
| 2 | Prepare budget | 3 days | 1 |
| 3 | Find location | 7 days | 2 |
| 4 | Sign office contract | 1 day | 3 |
| 5 | Contact computer suppliers | 4 days | 1 |
| 6 | Buy computer equipment | 1 day | 5, 2 |
| 7 | Buy office furniture | 2 days | 2 |
| 8 | Buy complements | 2 days | 2 |
| 9 | Review details | 1 day | 8, 6, 4 |
| 10 | Contact suppliers | 2 days | 9 |
| 11 | Buy products | 6 days | 10 |
| 12 | Marketing campaign | 12 days | 11 |
| 13 | Start of the activity | Milestone | 12 |

Task 13 is not really a normal task. It is a **milestone**, meaning it represents an important event:

 > **AldeNat starts operating.**

---

 # 4\. What does "precedence" mean?

 This is one of the most important parts of the exercise.

 Suppose we have:

 **1 → 2 → 3 → 4**

 That means:

 1. Determine space needs
2. Prepare budget
3. Find location
4. Sign office contract

 You cannot start Task 3 until Task 2 is finished.

 However, tasks can sometimes happen **in parallel**.

 For example:

 - Task 1 → Task 2
- Task 1 → Task 5

 So after Task 1 finishes, both Task 2 and Task 5 can potentially start.

 The project therefore looks approximately like this:

```
                    ┌── Task 3 ── Task 4 ──┐
                    │                       │
Task 1 ── Task 2 ───┼── Task 7 ────────────┤
                    │                       │
                    └── Task 8 ────────────┤
                                            │
Task 1 ── Task 5 ── Task 6 ────────────────┤
                                            ↓
                                      Task 9
                                        ↓
                                      Task 10
                                        ↓
                                      Task 11
                                        ↓
                                      Task 12
                                        ↓
                                  Task 13 (Start)
```

 That's why you shouldn't simply add all durations together. Some activities can occur simultaneously.

---

 # 5\. Overall project planning

 Now you need to determine **when each activity should happen**.

 The project starts:

 **Monday, September 28, 2026**

 Assuming Monday–Friday working days and no holidays, the earliest schedule based purely on the precedence relationships is approximately:

 | Task | Duration | Earliest start | Earliest finish |
| --- | --- | --- | --- |
| 1 | 2d | Sep 28 | Sep 29 |
| 2 | 3d | Sep 30 | Oct 2 |
| 3 | 7d | Oct 5 | Oct 13 |
| 4 | 1d | Oct 14 | Oct 14 |
| 5 | 4d | Sep 30 | Oct 5 |
| 6 | 1d | Oct 6 | Oct 6 |
| 7 | 2d | Oct 5 | Oct 6 |
| 8 | 2d | Oct 5 | Oct 6 |
| 9 | 1d | Oct 15 | Oct 15 |
| 10 | 2d | Oct 16 | Oct 19 |
| 11 | 6d | Oct 20 | Oct 27 |
| 12 | 12d | Oct 28 | Nov 12 |
| 13 | milestone | Nov 12 | Nov 12 |

So, under this basic schedule, the project would finish around:

 **Thursday, November 12, 2026.**

 > The exact date in Monday.com can differ depending on how you configure working hours, weekends, holidays, and whether the end date is interpreted inclusively.

---

 # 6\. Why are tasks 3, 4, 6, 8 and 9 important?

 Look at Task 9:

 > Review details\
>  Predecessors: 8, 6, 4

 This means Task 9 cannot begin until **all three** have finished:

 - Task 4
- Task 6
- Task 8

 This is a classic project-management situation.

 Task 4 takes much longer to reach completion than Tasks 6 and 8, so it effectively controls when Task 9 can start.

 This leads us to the idea of the **critical path**.

---

 # 7\. Critical path

 The critical path is the sequence of activities that determines the minimum project duration.

 For this project, the main controlling sequence is:

 **1 → 2 → 3 → 4 → 9 → 10 → 11 → 12 → 13**

 Let's calculate:

 $$
2+3+7+1+1+2+6+12 = 34\text{ working days}
$$

 So the critical path is approximately **34 working days**.

 The other branches are shorter:

 ### Branch through Task 5

 $$
1+4+1 = 6\text{ days}
$$

 ### Branch through Task 7

 $$
1+3+2 = 6\text{ days}
$$

 ### Branch through Task 8

 $$
1+3+2 = 6\text{ days}
$$

 Therefore, those activities have some **float/slack** because they don't determine the final project completion date.

---

 # 8\. Gantt chart

 The Gantt chart is simply a visual representation of the schedule.

 It should look conceptually like:

```
September                 October                    November
28  30  2  5  7  9  12 14 16 19 21 23 26 28 30 2 4 ... 12

Task 1   ███
Task 2       █████
Task 3             ███████████████
Task 4                            ██
Task 5       ████████
Task 6                 ██
Task 7             ████
Task 8             ████
Task 9                               ██
Task 10                                ████
Task 11                                      ████████████
Task 12                                                     ████████████████████████
Task 13                                                                  ◆
```

 In Monday.com, the Gantt view will automatically make this much clearer.

 The **diamond (◆)** represents the milestone "Start of the activity."

---

 # 9\. Resource allocation

 This is another major part of the exercise.

 You need to assign people to the tasks according to the table.

 For example:

 ### Task 1

 > Andrea = 20h

 So Andrea is assigned 20 hours.

 ### Task 2

 > Andrea = 30h

 Andrea gets another 30 hours.

 ### Task 5

 > Berta = 1h

 Berta works 1 hour.

 And so on.

 Your resource table would look like:

 | Task | Andrea | Anna | Berta |
| --- | --- | --- | --- |
| 1 | 20h | — | — |
| 2 | 30h | — | — |
| 3 | 12h | — | — |
| 4 | 1h | — | — |
| 5 | — | — | 1h |
| 6 | — | — | 3h |
| 7 | 5h | — | — |
| 8 | — | — | 6h |
| 9 | 8h | 10h | 1h |
| 10 | 1h | — | — |
| 11 | — | 6h | 10h |
| 12 | 15h | 10h | 20h |

---

 # 10\. Resource overload

 This is where the exercise becomes more interesting.

 Each employee can work:

 $$
8\text{ hours/day}
$$

 Therefore, if you assign someone more than 8 hours on a particular day, that person is **overloaded**.

 For example, imagine Monday.com shows:

 > Andrea: 10 hours on Monday

 But Andrea can only work:

 > 8 hours

 Therefore:

 $$
10-8=2\text{ hours overload}
$$

 You have to identify these situations.

 ### Important distinction

 A person can have a large total amount of work without being overloaded.

 For example:

 > Andrea has 40 hours of work over 5 days.

 That's fine:

 $$
40/5=8h/day
$$

 But:

 > Andrea has 16 hours assigned to one day.

 That's impossible under the stated working conditions.

---

 # 11\. Resource overload levelling

 Once you identify an overload, you need to **level the resources**.

 Resource leveling means changing the schedule so that nobody exceeds their available capacity.

 For example:

```
BEFORE

Monday:
Andrea = 10h ❌
Capacity = 8h

AFTER

Monday:
Andrea = 8h ✅
Tuesday:
Andrea = 2h
```

 You might therefore delay part of an activity.

 But there is a trade-off:

 > **Fixing a resource overload can make the project longer.**

 This is one of the most important project-management concepts in the exercise.

 You should therefore try to move **non-critical tasks** first.

 For example, if Task 7 has float, you can move it without affecting the final project date.

 But moving a critical-path activity may delay the entire project.

---

 # 12\. Project costs

 You also need to calculate the personnel cost.

 The rates are:

 - Andrea = **€30/hour**
- Anna = **€15/hour**
- Berta = **€6/hour**

 For example, Task 1 costs:

 $$
20h \times €30 = €600
$$

 Task 9 costs:

 Andrea:

 $$
8h \times €30 = €240
$$

 Anna:

 $$
10h \times €15 = €150
$$

 Berta:

 $$
1h \times €6 = €6
$$

 Therefore:

 $$
€240+€150+€6=\boxed{€396}
$$

---

 # 13\. Total planned personnel cost

 Let's calculate the hours first.

 ### Andrea

 $$
20+30+12+1+5+8+1+15
=92h
$$

 Cost:

 $$
92\times €30=\boxed{€2,760}
$$

 ### Anna

 $$
10+6+10=26h
$$

 Cost:

 $$
26\times €15=\boxed{€390}
$$

 ### Berta

 $$
1+3+6+1+10+20=41h
$$

 Cost:

 $$
41\times €6=\boxed{€246}
$$

 Total labor cost:

 $$
€2,760+€390+€246
=\boxed{€3,396}
$$

 Then add the fixed computer-equipment cost:

 $$
€3,396+€3,000
=\boxed{€6,396}
$$

 So the **planned project cost is €6,396**, assuming the hours listed in the table are the complete labor assignments and there are no other fixed costs.

---

 # 14\. What is the Time Baseline?

 This is very important for **Class Practice 2**.

 A baseline is basically a **snapshot of the approved original plan**.

 You save:

 - Original start dates
- Original finish dates
- Original durations
- Original planned costs
- Original resource plan

 Think of it as:

 > **"This is what we originally said would happen."**

 Then, during execution, you can compare reality against that baseline.

 For example:

 | Task | Baseline | Actual |
| --- | --- | --- |
| Find location | 7 days | 10 days |
| Buy computers | 1 day | 3 days |
| Buy complements | 2 days | 1 day |
| Buy products | 6 days | 8 days |
| Marketing | 12 days | 15 days |

This is exactly what Class Practice 2 is testing.

---

 # 15\. Class Practice 2 — what changes?

 Now the project is already underway.

 The instructor gives you **actual results**.

 You must enter those changes into Monday.com and compare them against the baseline.

 Let's examine each one.

---

 ## Task 3 — Find Location

 Original:

 $$
7\text{ days}
$$

 Actual:

 $$
10\text{ days}
$$

 Variance:

 $$
10-7=\boxed{+3\text{ days}}
$$

 So the task is **3 days late**.

 Because Task 3 is on the critical path, this is particularly important.

 It can potentially push the entire project later.

---

 ## Task 6 — Buy Computer Equipment

 Original:

 $$
1\text{ day}
$$

 Actual:

 $$
3\text{ days}
$$

 Variance:

 $$
3-1=\boxed{+2\text{ days}}
$$

 The supplier caused a delay.

 But Task 6 is **not on the critical path**, so its delay may not necessarily delay the entire project.

 That's an important observation to make in your report.

---

 # 16\. Task 8 — Buy Complements

 Original:

 $$
2\text{ days}
$$

 Actual:

 $$
1\text{ day}
$$

 Variance:

 $$
1-2=\boxed{-1\text{ day}}
$$

 This is good news.

 The task finished **one day earlier**.

 However, finishing this task early may not reduce the overall project duration because Task 8 is not controlling the critical path.

 This illustrates why:

 > **Finishing one task early does not automatically mean the whole project finishes early.**

---

 # 17\. Task 11 — Buy Products

 Original:

 $$
6\text{ days}
$$

 Actual:

 $$
8\text{ days}
$$

 Variance:

 $$
8-6=\boxed{+2\text{ days}}
$$

 This is significant because Task 11 is on the critical path.

 Therefore, this delay can directly affect the final project completion date.

---

 # 18\. Task 12 — Marketing Campaign

 Original:

 $$
12\text{ days}
$$

 Actual:

 $$
15\text{ days}
$$

 Variance:

 $$
15-12=\boxed{+3\text{ days}}
$$

 Task 12 is also on the critical path.

 Therefore, the project is likely to finish later than originally planned.

---

 # 19\. Cost variance

 There are two cost changes.

 ### Computer equipment

 Original:

 $$
€3,000
$$

 Actual:

 $$
€3,500
$$

 Variance:

 $$
€3,500-€3,000=\boxed{+€500}
$$

 So computer equipment costs **€500 more than planned**.

---

 ### Marketing campaign

 Additional designer cost:

 $$
\boxed{+€1,000}
$$

 Therefore total additional fixed cost is:

 $$
€500+€1,000
=\boxed{€1,500}
$$

 If labor costs haven't changed, the revised total project cost becomes:

 $$
€6,396+€1,500
=\boxed{€7,896}
$$

 Again, this assumes the exercise intends the additional €1,000 designer cost to be the only additional marketing cost.

---

 # 20\. What should you do in Monday.com?

 For **Class Practice 1**, your workflow should be:

 ### Step 1 — Create the board

 Create an AldeNat project board.

 ### Step 2 — Add the 13 tasks

 Enter all tasks and the milestone.

 ### Step 3 — Enter durations

 Use the durations from the table.

 ### Step 4 — Establish dependencies

 Connect predecessors:

```
1 → 2
2 → 3
3 → 4

1 → 5
5 → 6
2 → 6

2 → 7
2 → 8

8 → 9
6 → 9
4 → 9

9 → 10
10 → 11
11 → 12
12 → 13
```

 ### Step 5 — Assign resources

 Create:

 - Andrea
- Anna
- Berta

 Then assign their hours to each task.

 ### Step 6 — Enter hourly rates

 - Andrea: €30/h
- Anna: €15/h
- Berta: €6/h

 ### Step 7 — Add the €3,000 fixed cost

 Attach it to **Task 6 — Buy computer equipment**.

 ### Step 8 — Create the Gantt

 Use the Gantt view to see:

 - Start dates
- End dates
- Dependencies
- Parallel activities
- Milestone
- Critical path

 ### Step 9 — Check workload

 Look at each employee's workload.

 Identify where:

 $$
\text{Assigned hours} > 8h/day
$$

 ### Step 10 — Level the resources

 Move flexible/non-critical work where necessary.

 ### Step 11 — Save the baseline

 This is essential because Class Practice 2 uses it for comparison.

---

 # 21\. Then Class Practice 2

 You take your original project and **do not simply overwrite the original plan without preserving the baseline**.

 Instead, update the actual situation.

 Change:

 | Task | Original | Actual |
| --- | --- | --- |
| 3 | 7 days | 10 days |
| 6 | 1 day | 3 days |
| 8 | 2 days | 1 day |
| 11 | 6 days | 8 days |
| 12 | 12 days | 15 days |

Then update the costs:

 | Cost | Baseline | Actual | Variance |
| --- | --- | --- | --- |
| Computer equipment | €3,000 | €3,500 | +€500 |
| Marketing designer | €0 | €1,000 | +€1,000 |
| **Total additional** |  |  | **+€1,500** |

Finally, compare:

 **Baseline → Actual**

 for:

 - Schedule
- Duration
- Finish date
- Resources
- Cost
- Delays
- Variances

---

 # 22\. What does the teacher mean by "Project Report"?

 The report should explain what happened, not just show screenshots.

 A good report can have this structure:

 ### 1\. Project objective

 Explain that the objective is to prepare AldeNat for the start of operations.

 ### 2\. Project planning

 Include:

 - Tasks
- Durations
- Dependencies
- Start/finish dates
- Project duration

 ### 3\. Gantt chart

 Include a screenshot of the Gantt.

 ### 4\. Resource allocation

 Show how Andrea, Anna and Berta are assigned.

 ### 5\. Resource overloads

 Explain where someone exceeds their 8-hour daily capacity.

 ### 6\. Resource leveling

 Explain what changes you made to eliminate overloads.

 ### 7\. Project cost

 Show:

 $$
\boxed{€6,396}
$$

 as the original planned cost, based on the information provided.

 ### 8\. Baseline

 Explain that the original schedule and cost were saved as the baseline.

 ### 9\. Follow-up

 Compare the actual results with the baseline.

 ### 10\. Conclusions

 Explain:

 - Which tasks were delayed.
- Which task finished early.
- Whether the final project date changed.
- Whether costs increased.
- Whether resources became overloaded.
- What corrective action should be taken.

---

 ## 23\. The most important concepts to understand

 If this is for an **Information Systems Management / Project Management class**, I would focus on these six concepts:

 **1\. Dependency**

 > Task B cannot start until Task A is finished.

 **2\. Gantt chart**

 > Visual representation of tasks over time.

 **3\. Resource allocation**

 > Assigning Andrea, Anna and Berta to the activities.

 **4\. Resource overload**

 > Assigning more work than an employee can perform in the available time.

 **5\. Resource leveling**

 > Adjusting the schedule to eliminate overloads.

 **6\. Baseline**

 > The original approved plan used later to measure actual performance.

 And Class Practice 2 is essentially asking:

 > **"We made a plan. Reality didn't follow the plan. What changed, how much did it change, and what is the impact on the project?"**

 That is the central idea of the entire exercise.
