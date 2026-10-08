# Hospital Laundry Location Problem
## Suggested step-by-step outline

### 1\. Define the problem and objective

Start by clearly defining:

- **Facility:** Industrial hospital laundry.
- **Service area:** Hospitals in **Vallès Occidental**.
- **Objective:** Select the location that minimizes the overall logistics/operational burden while satisfying practical requirements.
- **Final requirement:** The selected location must correspond to a **real industrial premise that exists and is available for rent/purchase**, and must be suitable for conversion into a hospital laundry.

Define what "best" means. For example:

> The optimal location should provide good accessibility to the hospitals, minimize transportation costs and distance, have sufficient industrial infrastructure, and comply with the requirements of an industrial laundry.

---

# 2\. Identify the hospitals to be served

Create the dataset that will be used throughout the four methods.

For example, identify the main hospitals in Vallès Occidental, such as hospitals in:

- Sabadell
- Terrassa
- Sant Cugat del Vallès
- Rubí
- Cerdanyola del Vallès
- Other municipalities if their hospitals are considered part of the service area

For each hospital, collect:

| Hospital | Municipality | Address | X coordinate | Y coordinate | Beds / activity | Estimated laundry demand |
| --- | --- | --- | --- | --- | --- | --- |
| Hospital A | Sabadell | ... | ... | ... | ... | ... kg/day |
| Hospital B | Terrassa | ... | ... | ... | ... | ... |
| Hospital C | Sant Cugat | ... | ... | ... | ... | ... |

### Important

You need a **measure of demand** for each hospital because a large hospital should have more influence on the location than a small one.

Possible demand proxy:

- Number of beds
- Number of patients
- Surgical activity
- Estimated kg of laundry/day

If actual laundry-volume data isn't available, state an assumption such as:

> Estimated laundry demand is proportional to the number of hospital beds.

That assumption then needs to be applied consistently throughout the calculations.

---

# 3\. Establish the candidate locations

Don't immediately choose a premise.

First identify perhaps **5–10 candidate industrial areas/premises** distributed around Vallès Occidental.

For example:

- Sabadell
- Terrassa
- Barberà del Vallès
- Santa Perpètua de Mogoda
- Cerdanyola del Vallès
- Rubí
- Sant Quirze del Vallès
- Montcada i Reixac

At this stage, you're looking for **candidate industrial zones**, not necessarily the final building.

Then investigate actual premises available for:

- rent, or
- purchase.

For every candidate, collect:

| Candidate | Municipality | Size m² | Price | Industrial zoning | Access | Availability | Other characteristics |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A | Sabadell | 2,000 | €... | Yes | Excellent | Available | ... |
| B | Barberà | 3,000 | €... | Yes | Excellent | Available | ... |
| C | Terrassa | 2,500 | €... | Yes | Good | Available | ... |

This information becomes particularly important in the **factor-rating and cost models**.

---

# 4\. Method 1 — Center of Gravity

This gives you a **mathematical indication of where the facility should ideally be located**.

Assign coordinates to every hospital.

Use:

$$
X^*=\frac{\sum x_iw_i}{\sum w_i}
$$

$$
Y^*=\frac{\sum y_iw_i}{\sum w_i}
$$

where:

- $x_i,y_i$ = coordinates of hospital $i$
- $w_i$ = demand/weight of hospital $i$

For example, if Hospital A has twice the laundry demand of Hospital B, Hospital A receives twice the weight.

### Output

You should obtain something like:

> **Center of gravity = approximately \[X,Y\], corresponding to an area between Barberà del Vallès and Sabadell.**

Then plot the hospitals and calculated center.

**Important:** The center of gravity is **not necessarily your final location**. It is a theoretical optimum. There may be no suitable industrial building exactly there.

---

# 5\. Method 2 — Factor Rating Method

Now evaluate the **real-world characteristics** of the candidate locations.

Create criteria relevant to a hospital laundry.

For example:

| Factor | Weight |
| --- | --- |
| Distance/access to hospitals | 25% |
| Road accessibility | 20% |
| Industrial zoning/suitability | 15% |
| Property cost | 15% |
| Availability of water/electricity/gas | 10% |
| Premise size/expansion possibilities | 5% |
| Environmental/regulatory suitability | 5% |
| Labour availability | 5% |
| **Total** | **100%** |

Then score each candidate from **1 to 10**.

Example:

| Factor | Weight | A | B | C |
| --- | --- | --- | --- | --- |
| Hospital accessibility | 25% | 8 | 9 | 7 |
| Road access | 20% | 9 | 8 | 7 |
| Industrial suitability | 15% | 8 | 9 | 9 |
| Cost | 15% | 7 | 6 | 9 |
| Utilities | 10% | 9 | 8 | 7 |
| ... | ... | ... | ... | ... |
| **Weighted score** |  | **8.1** | **8.2** | **7.8** |

Calculate:

$$
Score_j=\sum_i w_i r_{ij}
$$

where:

- $w_i$ = weight of factor
- $r_{ij}$ = rating of location $j$

This produces a ranking of your candidate locations.

---

# 6\. Method 3 — Cost Model

This should translate the location decision into **money**.

Estimate the annual cost of operating from each candidate.

A simplified model could be:

$$
TC_j = FC_j + TC_{transport,j} + OC_j
$$

where:

- $FC$ = fixed facility cost
- $TC_{transport}$ = transportation cost
- $OC$ = other operating costs

### Fixed costs

Consider:

- Rent/purchase cost
- Property taxes
- Maintenance
- Utilities
- Adaptation/renovation
- Equipment installation

### Transportation costs

For each hospital:

$$
TransportCost_i = Distance_{ij}\times Trips_i\times Cost/km
$$

Then:

$$
TC_{transport,j}=
\sum_i Distance_{ij}\times Trips_i\times Cost/km
$$

You could improve the model by incorporating laundry volume:

$$
TC_{transport,j}
=
\sum_i Distance_{ij}
\times Demand_i
\times Cost/kg/km
$$

depending on the data available.

### Output

Produce something like:

| Candidate | Facility cost/year | Transport cost/year | Other costs | Total annual cost |
| --- | --- | --- | --- | --- |
| A | €250k | €180k | €80k | **€510k** |
| B | €280k | €140k | €75k | **€495k** |
| C | €220k | €210k | €85k | **€515k** |

Candidate B would therefore be the cheapest according to the model.

---

# 7\. Method 4 — Graph-Based Model

This is particularly useful because your problem can be represented as a **network**.

Think of:

- **Nodes** = hospitals + candidate facilities
- **Edges** = roads/connections
- **Edge weight** = distance or travel time

You have two models to apply.

## 7A. Simple Median Model

The objective is to select the facility location that minimizes the weighted distance to all hospitals:

$$
\min \sum_i w_i d_{ij}
$$

where:

- $w_i$ = hospital demand
- $d_{ij}$ = road distance between hospital $i$ and candidate location $j$

Calculate this for every candidate.

| Candidate | Weighted distance |
| --- | --- |
| A | 1,250 |
| B | **1,080** |
| C | 1,340 |
| D | 1,190 |

The lowest value is the best location under the **simple median model**.

### Important distinction

Center of gravity uses **geographical coordinates**.

Simple median uses the **network/graph**, so it can account for the actual road structure.

That distinction is worth explicitly explaining in your report.

---

# 8\. Coverage Model

Now introduce a service-level requirement.

For example:

> Every hospital should be reachable from the laundry within 30 minutes.

You can define a maximum acceptable travel distance/time:

$$
d_{ij}\leq D_{max}
$$

For example:

$$
D_{max}=30\text{ minutes}
$$

Then determine which candidate locations can cover which hospitals.

Example:

| Candidate | Hospital A | Hospital B | Hospital C | Hospital D | Hospitals covered |
| --- | --- | --- | --- | --- | --- |
| A | ✓ | ✓ | ✗ | ✓ | 3 |
| B | ✓ | ✓ | ✓ | ✓ | **4** |
| C | ✓ | ✗ | ✓ | ✓ | 3 |

Candidate B provides complete coverage.

If your course uses a **weighted coverage model**, incorporate hospital demand into the objective:

$$
\max \sum_i w_i z_i
$$

where $z_i=1$ if hospital $i$ is covered.

---

# 9\. Compare the four methods

This is an important section of the assignment.

Don't simply perform four calculations and stop.

Create a final comparison:

| Location | Center of Gravity | Factor Rating | Cost Model | Simple Median | Coverage |
| --- | --- | --- | --- | --- | --- |
| A | ✓ | 2nd | 2nd | 2nd | Partial |
| B | **Closest** | **1st** | **1st** | **1st** | **Full** |
| C | 3rd | 3rd | 3rd | 3rd | Full |

Then discuss whether the methods converge on the same area.

---

# 10\. Select the final real premise

This is the crucial final step because your assignment specifically says:

> **The solution must be a real premise existing in reality that is available and suitable.**

So you should not finish with:

> "The optimal location is Barberà del Vallès."

You need to finish with something more concrete:

> **Recommended premise:** \[specific industrial warehouse/address\], \[municipality\].

Then demonstrate that it is actually available.

For the final premise, verify:

### Physical suitability

- Floor area
- Ceiling height
- Loading/unloading area
- Vehicle access
- Possibility of separating clean/dirty laundry flows
- Expansion possibilities

### Infrastructure

- Water supply
- Drainage
- Electricity capacity
- Gas, if required
- Ventilation
- Wastewater management

### Legal/planning suitability

- Industrial zoning
- Permitted activity
- Environmental requirements
- Fire-safety requirements
- Possibility of obtaining the necessary operating permits

### Logistics

- Distance/time to each hospital
- Access to major roads
- Truck accessibility
- Traffic restrictions

### Commercial availability

- Current rental/sale status
- Asking price
- Availability date
- Property owner/agent
- Source proving the property is actually on the market

---

# 11\. Validate the final premise against the theoretical optimum

This is where you bring everything together.

Suppose your mathematical analyses identify an optimal area around **Barberà del Vallès**, but the actual available warehouse is 4 km away.

That's perfectly acceptable.

You can explain:

> The center-of-gravity calculation identifies the theoretical optimal point. However, no suitable industrial premise is available at that exact location. The selected warehouse is the closest available premise satisfying the operational, infrastructure and regulatory requirements.

Then recalculate the actual distances from the **selected premise** to all hospitals.

This makes the analysis much more realistic.

---

# 12\. Perform a sensitivity analysis

This would make the project considerably stronger.

Test what happens if your assumptions change.

For example:

### Scenario A — Equal hospital weights

Every hospital has equal importance.

### Scenario B — Bed-based weights

Larger hospitals have greater demand.

### Scenario C — Higher fuel/transport costs

Increase transport cost by 20%.

### Scenario D — Maximum 30-minute delivery

Apply the coverage constraint.

### Scenario E — Higher rent

Increase property cost by 20%.

Then see whether the recommended location changes.

If the same location remains attractive under several scenarios, you have a much stronger conclusion.

---

# 13\. Final recommendation

Your final section could follow this structure:

### Recommended location

**\[Real industrial premise\]**

### Why?

1. It is close to the calculated center of gravity.
2. It obtains a high factor-rating score.
3. It has competitive total annual cost.
4. It minimizes weighted road distance.
5. It provides the required coverage of the hospitals.
6. It is a real industrial property currently available.
7. It has the physical/infrastructural characteristics required for a hospital laundry.

Then clearly state the limitations and assumptions.

---

# Suggested report structure

I would organize the actual assignment like this:

## 1\. Introduction

- Problem definition
- Objective
- Study area
- Why centralized hospital laundry?

## 2\. Data Collection

- Hospitals
- Coordinates
- Number of beds/demand
- Candidate industrial areas
- Transport distances/times
- Property information

## 3\. Center of Gravity Method

- Formula
- Input data
- Calculation
- Map
- Result

## 4\. Factor Rating Method

- Selection of criteria
- Weights
- Scores
- Weighted results
- Ranking

## 5\. Cost Model

- Assumptions
- Facility costs
- Transportation costs
- Operating costs
- Total cost by location

## 6\. Graph-Based Model

### 6.1 Simple Median

- Network
- Distances
- Weighted distances
- Result

### 6.2 Coverage Model

- Coverage threshold
- Hospital-candidate matrix
- Coverage results
- Result

## 7\. Comparison of Results

- Comparison table
- Agreement/disagreement between methods
- Sensitivity analysis

## 8\. Selection of Real Premise

- Exact property
- Photos/map
- Size
- Price
- Availability evidence
- Industrial classification
- Infrastructure
- Accessibility

## 9\. Final Recommendation

- Selected premise
- Why it is preferable
- Expected advantages
- Risks/limitations

## 10\. Conclusion

- Summarize the four methods
- State the final location clearly

---

### One important strategic point

**Don't search for the real warehouse first and then try to make the calculations justify it.** Do the analysis first, identify the most promising geographical area/candidates, and **then search for an actual available premise that fits the result**.

For this assignment, I'd use approximately **6–8 candidate locations**, the major hospitals in Vallès Occidental, and then narrow the search down to **2–3 serious premises before selecting the final one**.

If you want, I can next help you turn this into the **actual project**, including identifying the Vallès Occidental hospitals, collecting their coordinates/demand data, selecting candidate industrial areas, and ultimately finding a **real available warehouse** to use as the final answer.
