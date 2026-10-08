Yes. Since we are working iteratively, I would make the roadmap a **living project plan** rather than a fixed table of contents. The important change from our original outline is that we now have a **data/evidence phase before writing the report**, and we explicitly separate **facts, assumptions, calculations, and decisions**.

# Updated Project Roadmap

## Phase 0 — Project Definition and Working Rules

**Status: 🟢 Completed**

Establish the project boundaries before collecting data.

### 0.1 Define the decision problem

> Select the best real, available industrial premise for a centralized hospital laundry serving the hospitals of Vallès Occidental.

### 0.2 Define the required methods

The project must use:

1. Center of Gravity
2. Factor Rating
3. Cost Model
4. Graph-Based Models
   - Simple Median
   - Coverage Model

### 0.3 Establish practical constraints

- No time to contact hospitals directly.
- Use publicly available online information.
- Use number of beds as the primary demand proxy.
- Document assumptions explicitly.
- Final solution must be a **real available premise**.
- Use consistent data across all models.

### 0.4 Establish project identifiers

- `Hxx` → hospitals
- `Axx` → industrial areas
- `Pxx` → properties
- `ASxx` → assumptions
- `Fxx` → important factual data, if useful
- `Cxx` → calculated outputs, if useful

---

# Phase 1 — Build the Hospital Dataset

**Status: 🔵 Next step**

This is our immediate task.

### 1.1 Determine the final hospital population

Identify which hospitals should be included in the service network.

We should establish a clear inclusion rule, for example:

> Include hospitals in Vallès Occidental with significant inpatient activity that could reasonably generate demand for an industrial hospital laundry.

### 1.2 Assign hospital IDs

For example:

```
H01
H02
H03
...
```

### 1.3 Collect factual information

For every hospital:

- Official name
- Municipality
- Address
- Latitude
- Longitude
- Number of beds
- Source
- Date accessed
- Notes

### 1.4 Verify the data

Prefer:

1. Government sources
2. Official hospital sources
3. Other reliable secondary sources

### Deliverable

A definitive:

**`hospitals.csv`**

and a human-readable hospital table.

---

# Phase 2 — Define Demand and Modelling Assumptions

**Status: 🔵 After Phase 1**

Once we know the hospitals, we establish how their demand will be represented.

### 2.1 Primary assumption

Use:

$$
w_i = Beds_i
$$

as the relative demand weight.

### 2.2 Investigate laundry-demand information

We will check whether credible public information exists regarding:

- kg laundry/bed/day;
- kg laundry/patient/day;
- healthcare textile consumption.

If good data exist, we can improve the model.

If not, we retain beds as the proxy.

### 2.3 Decide whether actual kg/day is required

For the location models, relative weights may be sufficient.

For the cost model, we may need an additional assumption such as:

$$
LaundryDemand_i =
Beds_i \times LaundryFactor
$$

The factor will only be introduced if necessary.

### 2.4 Create the assumptions register

For example:

| ID | Assumption | Status |
| --- | --- | --- |
| AS01 | Beds represent relative laundry demand | Confirmed |
| AS02 | One centralized laundry serves all selected hospitals | Confirmed |
| AS03 | ... | To determine |

### Deliverable

**`assumptions.csv`**

and finalized demand weights.

---

# Phase 3 — Geographical Dataset

**Status: 🔵 After Phase 2**

Now prepare the geographic information needed by the location models.

### 3.1 Verify hospital coordinates

Obtain latitude/longitude for each `Hxx`.

### 3.2 Establish coordinate system

Use a consistent system throughout the project.

For example:

- Latitude/longitude for mapping
- Projected coordinates where required for distance calculations

### 3.3 Prepare hospital map

Plot:

- hospitals;
- relative demand/weights;
- Vallès Occidental boundary.

### Deliverable

A geographical hospital dataset suitable for the **Center of Gravity** calculation.

---

# Phase 4 — Candidate Industrial Areas

**Status: ⬜ Not started**

Only now do we systematically identify potential locations.

### 4.1 Identify industrial clusters

Investigate areas around:

- Barberà del Vallès
- Cerdanyola del Vallès
- Sabadell
- Terrassa
- Santa Perpètua de Mogoda
- Sant Quirze del Vallès
- Rubí
- Other areas indicated by the analysis

### 4.2 Don't assume our preliminary candidates are final

Our earlier findings are **provisional**.

The Center of Gravity and hospital distribution may suggest additional areas.

### 4.3 Assign area IDs

```
A01
A02
A03
...
```

### Deliverable

**`industrial_areas.csv`**

---

# Phase 5 — Center of Gravity Analysis

**Status: ⬜ Not started**

This is the first actual location model.

Calculate:

$$
X^*=
\frac{\sum_i x_iw_i}
{\sum_iw_i}
$$

$$
Y^*=
\frac{\sum_i y_iw_i}
{\sum_iw_i}
$$

### Outputs

- X coordinate
- Y coordinate
- Map
- Nearest municipality/industrial areas
- Interpretation

### Critical distinction

The result is a **theoretical location**, not yet the final property.

It tells us:

> "Where would the facility ideally be located geographically, given the distribution of demand?"

---

# Phase 6 — Search for Real Available Premises

**Status: ⬜ Not started**

This phase connects the mathematical model to reality.

### 6.1 Search around promising areas

Prioritize locations close to:

- Center of Gravity
- major hospitals
- major road connections

### 6.2 Identify actual available properties

For every property:

- `P01`
- `P02`
- `P03`
- etc.

Collect:

- address;
- municipality;
- industrial estate;
- floor area;
- plot area;
- rent/purchase price;
- €/m²;
- ceiling height;
- loading docks;
- truck access;
- utilities;
- fire protection;
- offices;
- patio;
- availability;
- listing date;
- source.

### 6.3 Check suitability

A property being advertised as an industrial warehouse does **not automatically mean it is suitable for a hospital laundry**.

We therefore need to evaluate:

- water;
- drainage;
- electrical capacity;
- wastewater;
- ventilation;
- access;
- space;
- industrial activity compatibility;
- possibility of adaptation.

### Deliverable

**`properties.csv`**

and a shortlist of perhaps **5–8 serious candidates**.

---

# Phase 7 — Transportation Dataset

**Status: ⬜ Not started**

For every:

$$
Hospital \times Candidate
$$

combination, collect:

- road distance;
- travel time.

This produces the core transportation matrix:

|  | P01 | P02 | P03 | P04 |
| --- | --- | --- | --- | --- |
| H01 | km/min | km/min | km/min | km/min |
| H02 | km/min | km/min | km/min | km/min |
| H03 | km/min | km/min | km/min | km/min |
| H04 | km/min | km/min | km/min | km/min |
| H05 | km/min | km/min | km/min | km/min |

### Deliverable

**`transport_matrix.csv`**

This dataset will later be reused by **three different models**, which is why it needs to be carefully constructed.

---

# Phase 8 — Factor Rating Model

**Status: ⬜ Not started**

Define and justify the factors.

Initial proposal:

| Factor | Weight |
| --- | --- |
| Accessibility to hospitals | 25% |
| Road accessibility | 20% |
| Premise suitability | 15% |
| Property cost | 15% |
| Utilities/infrastructure | 10% |
| Size/expansion | 5% |
| Regulatory/environmental suitability | 5% |
| Labour accessibility | 5% |
| **Total** | **100%** |

Then:

$$
Score_j=\sum_i w_i r_{ij}
$$

### Deliverable

Ranked candidate properties.

---

# Phase 9 — Cost Model

**Status: ⬜ Not started**

Construct the economic model.

### Facility costs

- Rent
- Utilities
- Maintenance
- Property-related costs
- Adaptation

### Transportation

For example:

$$
TransportCost =
\sum_i Demand_i
\times Distance_{ij}
\times CostFactor
$$

The exact formulation will depend on the information we can reasonably obtain.

### Total

$$
TC_j =
FacilityCost_j+
TransportCost_j+
OtherCost_j
$$

### Deliverable

Annual estimated cost for every candidate.

---

# Phase 10 — Graph-Based Models

**Status: ⬜ Not started**

## 10.1 Simple Median

Calculate:

$$
\min_j
\sum_i w_i d_{ij}
$$

where $d_{ij}$ is road distance between hospital $i$ and property $j$.

### Output

Candidate ranking by weighted road distance.

---

## 10.2 Coverage Model

Define a service threshold.

For example:

> Every hospital should be reachable within 30 minutes.

Then calculate:

$$
Coverage_{ij} =
\begin{cases}
1 & d_{ij}\leq D_{max}\\
0 & d_{ij}>D_{max}
\end{cases}
$$

We can then determine:

- which hospitals each candidate covers;
- whether all hospitals are covered;
- total weighted demand covered.

### Deliverable

Coverage matrix and candidate ranking.

---

# Phase 11 — Integrate and Compare the Four Methods

**Status: ⬜ Not started**

This is where the project becomes a decision analysis rather than four unrelated calculations.

Create a master comparison:

| Candidate | COG proximity | Factor Rating | Cost | Simple Median | Coverage |
| --- | --- | --- | --- | --- | --- |
| P01 | Excellent | 1st | 2nd | 1st | Full |
| P02 | Good | 2nd | 1st | 2nd | Full |
| P03 | ... | ... | ... | ... | ... |

Then answer:

- Do the methods agree?
- Which candidate consistently performs well?
- Why do methods disagree?
- Which factors explain the differences?

---

# Phase 12 — Sensitivity Analysis

**Status: ⬜ Not started**

Test whether the conclusion is robust.

Possible scenarios:

### Scenario 1

Beds used as demand weights.

### Scenario 2

Different demand assumptions.

### Scenario 3

Transport costs +20%.

### Scenario 4

Property costs +20%.

### Scenario 5

30-minute coverage requirement.

### Scenario 6

Alternative factor-rating weights.

The key question:

> **Does the recommended property remain attractive when reasonable assumptions change?**

---

# Phase 13 — Final Real-Premise Validation

**Status: ⬜ Not started**

Before declaring the winner, perform a final due-diligence check.

For the selected `Pxx` verify:

- Is it still advertised?
- Is the address correct?
- Is the area correct?
- Is the property actually industrial?
- Is the stated price current?
- Is the property physically suitable?
- Can a hospital laundry plausibly operate there?
- Are there obvious regulatory/infrastructure problems?
- Does it provide adequate vehicle access?

We should explicitly distinguish:

> **"Available according to the listing"**

from:

> **"Confirmed available directly by the owner."**

Since we won't contact the owner, the first formulation is the appropriate one.

---

# Phase 14 — Final Recommendation

**Status: ⬜ Not started**

Select the final property.

The conclusion should answer:

> **Why this property rather than the alternatives?**

Ideally:

> Candidate Pxx is recommended because it provides the best overall balance between geographical position, weighted transportation distance, total cost, service coverage, facility characteristics and real-world availability.

---

# Phase 15 — Write the Report

**Status: ⬜ Not started**

Only after the analysis is complete do we finalize the report.

The report structure becomes:

```
1. Introduction
2. Data Collection and Assumptions
3. Center of Gravity Method
4. Factor Rating Method
5. Cost Model
6. Graph-Based Models
   6.1 Simple Median
   6.2 Coverage Model
7. Comparison of Results
8. Sensitivity Analysis
9. Selection and Validation of Real Premise
10. Final Recommendation
11. Conclusion
12. References
13. Appendices
```

For **each section**, we will produce:

```
Academic Version
        +
Practical Project Version
```

---

# Phase 16 — Final Quality Check

Before submission, check:

### Data consistency

- Same hospital IDs everywhere.
- Same bed weights everywhere.
- Same candidate IDs everywhere.
- Same distances everywhere.

### Traceability

Every important external number has a source.

### Assumptions

Every estimated value is explicitly identified as an assumption.

### Methodology

All four required methods have actually been applied.

### Practical requirement

The final answer is a **real available premise**, not merely a municipality or theoretical coordinate.

### Reproducibility

Another student should be able to follow our data, assumptions and calculations and approximately reproduce the result.

---

# Current Project Status

Our roadmap now looks like this:

```
PHASE 0  Project definition                 ██████████  DONE
PHASE 1  Hospital dataset                   ░░░░░░░░░░  NEXT
PHASE 2  Demand & assumptions               ░░░░░░░░░░
PHASE 3  Geographic dataset                 ░░░░░░░░░░
PHASE 4  Industrial areas                   ░░░░░░░░░░
PHASE 5  Center of Gravity                  ░░░░░░░░░░
PHASE 6  Real premises                      ░░░░░░░░░░
PHASE 7  Transportation matrix              ░░░░░░░░░░
PHASE 8  Factor Rating                      ░░░░░░░░░░
PHASE 9  Cost Model                         ░░░░░░░░░░
PHASE 10 Graph Models                       ░░░░░░░░░░
PHASE 11 Method comparison                  ░░░░░░░░░░
PHASE 12 Sensitivity analysis               ░░░░░░░░░░
PHASE 13 Final property validation          ░░░░░░░░░░
PHASE 14 Final recommendation               ░░░░░░░░░░
PHASE 15 Report completion                  ░░░░░░░░░░
PHASE 16 Quality/reproducibility check     ░░░░░░░░░░
```

### The immediate next action

**Phase 1: build the definitive hospital dataset.**

We should now stop discussing the report temporarily and do the actual research for `H01, H02, ...`: **hospital name → address → municipality → current beds → source → coordinates → identifier**.

Once that dataset is solid, we move to Phase 2 and don't proceed to the Center of Gravity until the hospital data and assumptions are frozen. This sequential approach should prevent errors from propagating through all four location models.
