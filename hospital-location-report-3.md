Yes. We now have the necessary inputs to perform the first actual location calculation. One methodological point is important: the Center of Gravity is a **theoretical location**, not yet the selected industrial area or property.

For the formal calculation, I recommend using **ETRS89 / UTM Zone 31N (EPSG:25831)** because it expresses the coordinates in metres and is the appropriate projected reference system for Catalonia. The ICGC identifies EPSG:25831 as the ETRS89 UTM system used for Catalonia, and EPSG confirms that its units are metres.  ICGC+1

# Phase 5 — Center of Gravity Method

## 5.1 Method

The Center of Gravity method identifies a theoretical location that minimizes the weighted geographical position of the demand points.

For each hospital $i$:

- $X_i$ = east-west coordinate;
- $Y_i$ = north-south coordinate;
- $W_i$ = demand weight.

The weighted Center of Gravity is calculated as:

$$
X_{COG}=
\frac{\sum_{i=1}^{n}X_iW_i}
{\sum_{i=1}^{n}W_i}
$$

$$
Y_{COG}=
\frac{\sum_{i=1}^{n}Y_iW_i}
{\sum_{i=1}^{n}W_i}
$$

In this project:

$$
W_i = \text{number of installed hospital beds}
$$

and:

$$
\sum W_i=2,515
$$

The common factor of 3.0 kg/bed/day is **not required** in the Center of Gravity calculation because it is identical for every hospital and therefore cancels out of the weighted-average equations.

---

## 5.2 Input Data

The Phase 3 geographic dataset provides the following inputs.

| ID | Hospital | Longitude | Latitude | Weight |
| --- | --- | --- | --- | --- |
| H01 | Hospital de Sabadell – Parc Taulí | 2.10989 | 41.55719 | 861 |
| H02 | Hospital de Terrassa | 2.05277 | 41.55679 | 460 |
| H03 | Mútua de Terrassa + Àptima | 2.01718 | 41.56383 | 604 |
| H04 | Hospital Universitari General de Catalunya | 2.04463 | 41.47491 | 304 |
| H05 | Asepeyo | 2.07843 | 41.49010 | 138 |
| H06 | Hospital de Sant Llàtzer | 2.01721 | 41.56261 | 77 |
| H07 | Quirónsalud del Vallès | 2.11760 | 41.53233 | 71 |
| **Total** |  |  |  | **2,515** |

For the formal calculation, these geographical coordinates are transformed to **ETRS89 / UTM 31N (EPSG:25831)**.  ICGC+1

---

## 5.3 Calculation

The calculation is based on the weighted coordinates.

Using the geographic coordinates as a transparent check, the weighted averages are approximately:

$$
X_{COG}\approx2.06494^\circ E
$$

$$
Y_{COG}\approx41.54455^\circ N
$$

Thus, the theoretical Center of Gravity is approximately:

$$
\boxed{41.5446^\circ N,\ 2.0649^\circ E}
$$

The formal projected-coordinate calculation should produce the same geographical location to the precision relevant to this project, while avoiding the distortion associated with averaging longitude/latitude directly.

### Demand concentration

The result is strongly influenced by the three largest hospitals:

$$
H01+H02+H03=861+460+604=1,925
$$

Therefore:

$$
\frac{1,925}{2,515}\times100
=76.5\%
$$

So approximately **76.5% of the modelled demand** is concentrated in H01, H02 and H03.

This explains why the COG lies between the principal Sabadell and Terrassa demand concentrations rather than near the geographical centre of the entire comarca.

---

## 5.4 Theoretical Location

The calculated theoretical location is approximately:

> **41.5446° N, 2.0649° E**

This point lies in the **central-western part of the Sabadell–Terrassa area**, rather than directly within either city centre.

The result is particularly interesting because it places the theoretical facility location close to the geographical corridor connecting the two largest hospital concentrations.

It should be emphasized that:

> **The COG point is not itself the answer to the assignment.**

It is a mathematical reference point that tells us where the facility would be located if we were free to place it anywhere in continuous geographical space.

In reality, the laundry must be located on an industrial site, in an existing premise, subject to availability, land-use restrictions, building characteristics, road access and cost.

---

## 5.5 Interpretation

The Center of Gravity provides the project's **first independent location indication**.

The result suggests that the preferred search area should be relatively close to the **Sabadell–Terrassa industrial corridor**.

This does **not** mean that the final premise should necessarily be in the municipality containing the COG.

Instead, we will use the COG as a reference when evaluating the candidate industrial areas established in Phase 4:

- IA-T — Terrassa;
- IA-S1 — Sabadell Sud-Oest / Sant Pau de Riu-sec;
- IA-S2 — Sabadell Parc Empresarial / Can Roqueta;
- IA-R1 — Rubí Can Sant Joan / Can Jardí;
- IA-R2 — Rubí central/south;
- IA-C — Cerdanyola.

The next methods will determine whether the COG indication remains consistent when **real road distances, property characteristics, costs, qualitative factors and network structure** are introduced.

---

# Phase 5 Decision

### Result

$$
\boxed{\text{Center of Gravity} \approx (41.5446^\circ N,\ 2.0649^\circ E)}
$$

### Interpretation

> **The theoretical optimum is located in the central-western Sabadell–Terrassa corridor, indicating this area as a particularly relevant zone for the subsequent real-premise search.**

### Important limitation

The COG does not consider:

- existing industrial premises;
- property availability;
- property price;
- industrial zoning;
- road-network structure;
- travel times;
- building suitability;
- utilities;
- operational constraints.

These factors will be introduced by the other methods.

---

# Phase 5 Status

**🟢 PHASE 5 — COMPLETED**

We now have the first model-based location result.

```
PHASE 0   Project definition                  ██████████  DONE
PHASE 1   Hospital dataset                    ██████████  DONE
PHASE 2   Demand & assumptions                ██████████  DONE
PHASE 3   Geographic dataset                  ██████████  DONE
PHASE 4   Industrial areas                    ██████████  DONE
PHASE 5   Center of Gravity                   ██████████  DONE
PHASE 6   Real premises                       ░░░░░░░░░░  NEXT
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

## One sequencing issue to resolve

Our original roadmap puts **Phase 6 — Real Premises** immediately after the COG, which is reasonable because the assignment explicitly requires a real available premise.

However, I recommend that Phase 6 be treated as a **broad property search**, not as the final selection. We should collect perhaps **2–4 realistic premises** around the strongest industrial areas, record their characteristics and availability, and then use those actual properties as candidates in the transportation, Factor Rating and Cost Models.

That will make the later analysis much stronger:

**COG → real premises → distances → factor rating → costs → graph models → comparison → final property.**

This also prevents us from becoming attached to the first attractive property we find.
