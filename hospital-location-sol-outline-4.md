Yes. I would do all three now. One small structural improvement: **Data Collection should remain a consolidated section**, while the detailed modelling phases follow it. Also, the current roadmap should reflect that Phase 3 is now the active phase.

## TD1 — Updated Project Status

```
CURRENT PROJECT STATUS

PHASE 0   Project definition                  ██████████  DONE
PHASE 1   Hospital dataset                    ██████████  DONE
PHASE 2   Demand & assumptions                ██████████  DONE
PHASE 3   Geographic dataset                  ░░░░░░░░░░  NEXT
PHASE 4   Industrial areas                    ░░░░░░░░░░
PHASE 5   Center of Gravity                   ░░░░░░░░░░
PHASE 6   Real premises                       ░░░░░░░░░░
PHASE 7   Transportation matrix               ░░░░░░░░░░
PHASE 8   Factor Rating                       ░░░░░░░░░░
PHASE 9   Cost Model                          ░░░░░░░░░░
PHASE 10  Graph Models                        ░░░░░░░░░░
PHASE 11  Method comparison                   ░░░░░░░░░░
PHASE 12  Sensitivity analysis                ░░░░░░░░░░
PHASE 13  Final property validation           ░░░░░░░░░░
PHASE 14  Final recommendation                ░░░░░░░░░░
PHASE 15  Report completion                   ░░░░░░░░░░
PHASE 16  Quality/reproducibility check      ░░░░░░░░░░
```

### Current position

**Phases 0–2 are complete.**

We are now entering:

> **Phase 3 — Geographic Dataset**

The immediate objective is to finalize the geographical inputs required for the location analysis, before calculating the Center of Gravity.

---

# TD2 — Updated Data Collection Status

| Dataset | Status | Next action |
| --- | --- | --- |
| Hospital list | 🟢 **Final** | Use H01–H07 |
| Hospital addresses | 🟢 **Final** | Use verified addresses |
| Coordinates | 🟡 **In progress** | Finalize/geocode and validate |
| Bed numbers | 🟢 **Final** | Use 2025 catalogue values |
| Demand weights | 🟢 **Final** | Beds = relative demand |
| Base laundry demand | 🟢 **Final** | 3.0 kg/bed/day |
| Industrial areas | ⬜ Not started | Identify candidate areas |
| Available premises | ⬜ Not started | Search and verify |
| Property characteristics | ⬜ Not started | Collect for shortlisted properties |
| Road distances | ⬜ Not started | Calculate after candidate properties |
| Travel times | ⬜ Not started | Calculate after candidate properties |
| Cost parameters | ⬜ Not started | Establish during Cost Model |
| Coverage threshold | ⬜ Not started | Define during Graph Model |
| Final dataset | ⬜ Not started | Freeze after all data collection |

### Important distinction

We should now stop calling the hospital information "preliminary." **Phase 1 is frozen.**

The only remaining hospital-related activity is **coordinate validation**, which belongs to Phase 3.

---

# TD3 — Updated Report Structure

I recommend keeping the overall structure but making one important change: **the report should follow the actual analytical sequence**, not necessarily the chronological sequence in which we happened to collect the data.

The revised structure is:

```
1. Introduction
   1.1 Problem definition
   1.2 Project objective
   1.3 Study area
   1.4 Centralized hospital laundry concept

2. Data Collection and Assumptions
   2.1 Hospital network
   2.2 Hospital locations and coordinates
   2.3 Demand estimation
   2.4 Candidate industrial areas
   2.5 Candidate premises
   2.6 Transportation data
   2.7 Key assumptions and limitations

3. Center of Gravity Method
   3.1 Method
   3.2 Input data
   3.3 Calculation
   3.4 Theoretical location
   3.5 Interpretation

4. Factor Rating Method
   4.1 Selection of criteria
   4.2 Criteria weights
   4.3 Candidate scores
   4.4 Weighted results
   4.5 Ranking

5. Cost Model
   5.1 Cost assumptions
   5.2 Facility costs
   5.3 Transportation costs
   5.4 Operating costs
   5.5 Total cost by candidate
   5.6 Cost ranking

6. Graph-Based Models
   6.1 Simple Median Model
       6.1.1 Network
       6.1.2 Distances
       6.1.3 Weighted distances
       6.1.4 Result

   6.2 Coverage Model
       6.2.1 Coverage threshold
       6.2.2 Hospital-candidate matrix
       6.2.3 Coverage results
       6.2.4 Result

7. Comparison of Results
   7.1 Comparison of the four methods
   7.2 Agreement and disagreement
   7.3 Interpretation of differences
   7.4 Sensitivity analysis

8. Selection and Validation of Real Premise
   8.1 Selected property
   8.2 Exact location
   8.3 Property characteristics
   8.4 Size and capacity
   8.5 Price/cost
   8.6 Availability evidence
   8.7 Industrial classification
   8.8 Infrastructure
   8.9 Accessibility
   8.10 Suitability for hospital laundry

9. Final Recommendation
   9.1 Selected premise
   9.2 Reasons for selection
   9.3 Expected advantages
   9.4 Risks and limitations

10. Conclusion
    10.1 Summary of methodology
    10.2 Main findings
    10.3 Final location
```

## Why I would make this change

The original structure placed **Sensitivity Analysis inside Section 7**, which is fine, but we should treat it as a **cross-check after all four models**, rather than as a separate fifth location method.

More importantly, Section 8 should be called **"Selection and Validation of Real Premise"** rather than simply "Selection of Real Premise."

That's because the assignment has a very specific practical requirement:

> The answer must be a **real premise that exists, is available, and is suitable**.

Therefore, the mathematical models identify and rank candidates, but the final stage must validate that the winning candidate actually exists and is practically suitable.

---

# How the roadmap and report now connect

We now have a clean relationship between the **working project roadmap** and the **final report**:

| Project Phase | Final Report |
| --- | --- |
| Phase 0 | Section 1 |
| Phase 1 | Section 2.1–2.2 |
| Phase 2 | Section 2.3 + assumptions |
| Phase 3 | Section 2.2 + Section 3 inputs |
| Phase 4 | Section 2.4 |
| Phase 5 | Section 3 |
| Phase 6 | Section 2.5 + Section 8 |
| Phase 7 | Section 2.6 + Sections 5–6 |
| Phase 8 | Section 4 |
| Phase 9 | Section 5 |
| Phase 10 | Section 6 |
| Phase 11 | Section 7 |
| Phase 12 | Section 7.4 |
| Phase 13 | Section 8 |
| Phase 14 | Section 9 |
| Phase 15 | Sections 1–10 |
| Phase 16 | Final quality check |

This is useful because **we don't have to write the report twice**. We develop the solution first, keep the underlying data and calculations organized, and then progressively populate the corresponding report sections.

## Next step

We should now proceed with **Phase 3 — Geographic Dataset**.

The concrete task is:

> **Finalize the latitude/longitude coordinates for H01–H07, validate them, establish the coordinate system, and prepare the exact input table for the Center of Gravity calculation.**

Once that is done, we can immediately calculate the **theoretical Center of Gravity** and move into the industrial-area search.
