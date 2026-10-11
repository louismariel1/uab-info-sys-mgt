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


Agreed. Phase 3 should now focus on **freezing the geographical dataset**, not yet calculating the Center of Gravity. I checked the coordinates against current map/geospatial sources and found a few small corrections to our preliminary values.

# Phase 3 — Geographic Dataset

## 3.1 Objective

The objective of Phase 3 is to establish a consistent geographical dataset for the seven hospital service points defined in Phases 1 and 2.

The dataset will provide the geographical inputs for:

- Center of Gravity;
- industrial-area identification;
- transportation-distance calculations;
- Simple Median Model;
- Coverage Model;
- mapping and visualization.

We will use **WGS84 latitude/longitude** as the master coordinate representation. If projected coordinates are required for a calculation or GIS operation, we can subsequently transform the points to **ETRS89 / UTM Zone 31N (EPSG:25831)**, which is appropriate for the study area.

---

## 3.2 Final Hospital Geographic Dataset

| ID | Hospital / Service Point | Municipality | Latitude | Longitude | Demand Weight |
| --- | --- | --- | --- | --- | --- |
| **H01** | Hospital de Sabadell – Parc Taulí | Sabadell | **41.55719** | **2.10989** | 861 |
| **H02** | Hospital de Terrassa | Terrassa | **41.55679** | **2.05277** | 460 |
| **H03** | Mútua de Terrassa + Àptima Centre Clínic | Terrassa | **41.56383** | **2.01718** | 604 |
| **H04** | Hospital Universitari General de Catalunya | Sant Cugat del Vallès | **41.47491** | **2.04463** | 304 |
| **H05** | Centre de Prevenció i Rehabilitació Asepeyo | Sant Cugat del Vallès | **41.49010** | **2.07843** | 138 |
| **H06** | Hospital de Sant Llàtzer | Terrassa | **41.56261** | **2.01721** | 77 |
| **H07** | Hospital Quirónsalud del Vallès | Sabadell | **41.53233** | **2.11760** | 71 |
|  | **Total** |  |  |  | **2,515** |

The coordinates for H01 are supported by OpenStreetMap-based mapping data; H02 by the mapped Hospital Terrassa location; H03 by the mapped Mútua de Terrassa location; H04 by OpenStreetMap/Wikidata-based data; H05 by OpenStreetMap/Wikidata; H06 by OpenStreetMap; and H07 by OpenStreetMap/Wikidata.  Mapcarta+6

For H01, the hospital's official website confirms the address as Parc del Taulí, 1, Sabadell.  tauli.cat  Asepeyo's official site confirms the H05 address as Av. de l'Alcalde Barnils 54–60, Sant Cugat del Vallès.  Asepeyo

---

## 3.3 Coordinate Validation

There are three points worth documenting.

### H03 — Mútua de Terrassa + Àptima

Mútua de Terrassa and Àptima were aggregated in Phase 2 because they share the same geographical service point. The coordinate used is therefore the Mútua de Terrassa hospital location.

The mapped Mútua de Terrassa location is approximately:

$$
41.56383,\ 2.01718
$$

Mapcarta

The important point for our model is not the exact entrance but the **common hospital-site location**.

### H04 — Hospital Universitari General de Catalunya

Some mapping sources label the physical location as being in/near **Rubí**, while the hospital's institutional address is associated with **Sant Cugat del Vallès**. The geographical model will use the actual hospital coordinates rather than attempting to resolve this municipal-boundary labelling issue.

The coordinate is:

$$
41.47491,\ 2.04463
$$

Wikidata+1

### H06 — Hospital de Sant Llàtzer

The current mapped building location is:

$$
41.56261,\ 2.01721
$$

Mapcarta

This is preferable to the slightly different coordinate used in our preliminary dataset.

---

# 3.4 Geographic Data Convention

From this point forward, we will use the following convention:

| Item | Convention |
| --- | --- |
| Master coordinate system | WGS84 |
| Coordinates | Decimal degrees |
| Latitude | North positive |
| Longitude | East positive |
| Projected GIS system if required | ETRS89 / UTM 31N |
| Hospital location | Hospital/service-point location |
| Transportation origin | Hospital address |
| Demand weight | Hospital beds |
| Hospital IDs | H01–H07 |

This gives us one consistent geographic reference throughout the project.

---

# 3.5 Geographic Distribution

The dataset shows an important characteristic of the problem.

The hospitals are not evenly distributed across Vallès Occidental. There is a clear concentration around:

- **Sabadell**, particularly H01 and H07;
- **Terrassa**, particularly H02, H03 and H06;
- **Sant Cugat/Rubí area**, particularly H04 and H05.

This distribution is precisely why a simple geographical midpoint would not be sufficient. The subsequent **Center of Gravity calculation will weight each location according to its hospital demand**.

In particular:

- H01 carries **861 beds**;
- H03 carries **604 beds**;
- H02 carries **460 beds**.

Together these three service points represent:

$$
861+604+460=1,925\text{ beds}
$$

or approximately:

$$
\frac{1,925}{2,515}\times100
\approx76.5\%
$$

of the modelled demand.

Therefore, the theoretical optimum will be strongly influenced by the Sabadell–Terrassa hospital concentration.

---

# 3.6 Geographic Dataset for the Model

For the next calculations, our input table can be reduced to:

| ID | X = Longitude | Y = Latitude | Weight |
| --- | --- | --- | --- |
| H01 | 2.10989 | 41.55719 | 861 |
| H02 | 2.05277 | 41.55679 | 460 |
| H03 | 2.01718 | 41.56383 | 604 |
| H04 | 2.04463 | 41.47491 | 304 |
| H05 | 2.07843 | 41.49010 | 138 |
| H06 | 2.01721 | 41.56261 | 77 |
| H07 | 2.11760 | 41.53233 | 71 |
| **Total** |  |  | **2,515** |

This is the table we will use for the **Center of Gravity**.

The calculation will be:

$$
X_{COG}=
\frac{\sum X_iW_i}{\sum W_i}
$$

$$
Y_{COG}=
\frac{\sum Y_iW_i}{\sum W_i}
$$

where:

- $X_i$ = longitude of hospital $i$;
- $Y_i$ = latitude of hospital $i$;
- $W_i$ = demand weight of hospital $i$.

For the final geographic calculation, I recommend that we perform the calculation using **projected ETRS89/UTM coordinates**, rather than directly averaging degrees of longitude and latitude. We can still present the resulting point as latitude/longitude for the report.

---

# 3.7 Phase 3 Decision

### Final decision

> **The seven hospital service points H01–H07 and their validated geographical coordinates are adopted as the geographic dataset for the remainder of the project.**

No further hospital-coordinate changes should be made unless a material data error is discovered.

---

# Phase 3 Status

**🟢 PHASE 3 — COMPLETED**

We now have:

- [x]Seven hospital/service points
- [x]Permanent IDs
- [x]Addresses established
- [x]Coordinates established
- [x]Coordinate convention established
- [x]Demand weights connected to coordinates
- [x]Geographic dataset prepared for modelling
- [x]Preliminary geographic distribution understood

### Updated roadmap

```
PHASE 0   Project definition                  ██████████  DONE
PHASE 1   Hospital dataset                    ██████████  DONE
PHASE 2   Demand & assumptions                ██████████  DONE
PHASE 3   Geographic dataset                  ██████████  DONE
PHASE 4   Industrial areas                    ░░░░░░░░░░  NEXT
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

## Next phase

There is a small sequencing point in our roadmap that is now worth addressing.

**Phase 4 — Industrial Areas** should identify the realistic industrial zones around the study network. Then **Phase 5 — Center of Gravity** will calculate the theoretical optimum and allow us to compare that theoretical point with the actual industrial geography.

That gives us the useful progression:

**Hospitals → Demand → Coordinates → Industrial geography → Theoretical COG → Real premises.**

That is the point at which the project starts connecting the mathematical model to the real-world property search.

# Phase 4 — Industrial Areas

## 4.1 Objective

The objective of this phase is to identify industrial areas that could realistically accommodate the proposed centralized hospital laundry.

The industrial-area search should cover the geographical envelope created by the seven hospitals while considering:

- industrial land/buildings;
- road accessibility;
- proximity to the hospital network;
- availability of sufficiently large premises;
- suitability for an industrial laundry;
- potential for heavy/light commercial vehicle access;
- proximity to major roads.

At this stage we are **not selecting a property**.

We are identifying the industrial geography in which the subsequent property search will take place.

---

## 4.2 Why we should not search the entire Vallès Occidental uniformly

Our hospital demand is highly concentrated.

H01, H02 and H03 alone represent:

$$
861+460+604=1,925\text{ beds}
$$

or:

$$
76.5\%
$$

of total modelled demand.

The three main demand centres are therefore:

- Sabadell;
- Terrassa;
- the Sant Cugat/Rubí area.

This suggests that the industrial-area search should concentrate on the **Sabadell–Terrassa–Rubí/Sant Cugat corridor**, while retaining a broader set of industrial areas for comparison.

---

# 4.3 Industrial Geography Identified

## A. Terrassa

Terrassa has a particularly strong industrial base and an extensive network of industrial areas. The municipality maintains an official GIS dataset of its industrial estates, available in SHP and GeoJSON formats.  opendata.terrassa.cat+1

The official municipal sources identify numerous industrial areas, including:

- Can Petit
- Can Parellada
- Els Bellots
- Santa Margarida I
- Santa Margarida II
- Can Palet
- Can Farcan
- Can Guitard
- Colom II
- Palau Nord
- Palau Sud
- Segle XX
- Puigbarral
- La Grípia
- Els Gorgs

Terrassa's own data show approximately **6.13 million m² of industrial-estate surface** across its mapped industrial areas.  Terrassa

The municipality also identifies Els Bellots, Santa Margarida and Can Parellada as a strategically connected industrial cluster.  Terrassa

### Particularly relevant Terrassa cluster

For our project, I propose initially grouping the numerous Terrassa estates into a smaller analytical candidate area:

> **IA-T — Terrassa industrial corridor: Els Bellots / Santa Margarida / Can Parellada**

This is more useful than treating every Terrassa estate as a separate candidate at this stage.

There is also a significant development opportunity at **Els Bellots II**. The municipality describes it as a 95.31-hectare new productive-activity sector between the N-150 and C-58.  Terrassa

However, because our assignment ultimately requires an **existing available premise**, Els Bellots II should not automatically be treated as a property candidate. It is primarily relevant as evidence of the industrial capacity of the area.

---

# 4.4 Sabadell

Sabadell has an extensive industrial network concentrated in several areas.

A recent municipal document identifies seven significant industrial activity zones:

- Can Feu
- Can Roqueta
- Gràcia Nord
- Gràcia Sud
- Parc Industrial Riu Ripoll
- Sabadell Parc Empresarial
- Sud-Oest

The municipality reports approximately **1,855 companies** in these industrial zones.  web.sabadell.cat

Another municipal mobility study groups Sabadell's industrial geography into three broad areas:

1. Riu Ripoll / Can Roqueta;
2. Can Feu / Gràcia / Sud-Oest;
3. Sabadell Parc Empresarial.

It also highlights the strategic relationship of these industrial areas with the **C-58 and AP-7**.  web.sabadell.cat

### Particularly relevant Sabadell areas

For our project, I recommend retaining:

> **IA-S1 — Sabadell Sud-Oest / Sant Pau de Riu-sec**

and

> **IA-S2 — Sabadell Parc Empresarial / Can Roqueta**

as the main Sabadell candidate areas.

The Sud-Oest/Sant Pau de Riu-sec area is particularly interesting because of its location toward the southern part of Sabadell and its relationship with the C-58. The municipality describes Sant Pau de Riu-sec as a major developing industrial area.  web.sabadell.cat

---

# 4.5 Rubí

Rubí is another particularly important candidate because of its position between the Terrassa and Sant Cugat parts of the hospital network.

The municipality currently describes Rubí as having approximately **10 PAE covering almost 400 hectares**, with industrial activity distributed across the municipality.  rubi.cat

The identified areas include:

- Can Jardí
- Can Vallhonrat
- Cova Solera
- Can Rosés
- La Llana
- Carretera de Terrassa
- Molí de la Bastida
- Rubí Sud / Can Pi de Vilaroch
- Sant Genís
- Can Sant Joan

Municipal sources also identify the Rubí industrial network as having strong industrial activity and access to major metropolitan connections.  rubi.cat+1

### Particularly relevant Rubí areas

Rather than analysing all ten areas independently, I recommend initially considering:

> **IA-R1 — Rubí North / Can Sant Joan–Can Jardí**

and

> **IA-R2 — Rubí Central/South industrial corridor**

The Rubí municipality also provides an industrial-property search portal, which will be useful in Phase 6 when we need to identify an **actually available premise**.  rubi.cat

---

# 4.6 Sant Cugat del Vallès

Sant Cugat also contains established industrial areas, including:

- Can Sant Joan
- Can Mamet
- Can Calopa
- Can Graells
- Can Magí
- Turó de Can Mates

Municipal documentation identifies these as the principal concentrations of industrial activity in the municipality.  Oficina Sostenible

However, for our project, Sant Cugat presents an important issue:

> Its industrial geography is relatively close to H04 and H05 but further from the major Sabadell/Terrassa demand concentration.

Therefore, we should **retain Sant Cugat as a candidate area but not assume that it is optimal simply because two hospitals are located there.**

The model will decide.

---

# 4.7 Cerdanyola / Northern Metropolitan Corridor

I recommend retaining one additional geographical control area:

> **IA-C — Cerdanyola industrial corridor**

Cerdanyola has a substantial industrial and economic-activity network. Municipal documentation identifies **11 industrial estates**, covering approximately **2.9 million m²**, with many located close to the C-58 and AP-7/B-30.  Cerdanyola

The areas include:

- Parc de l'Alba
- Parc Tecnològic del Vallès
- La Bòbila
- La Clota
- Riviere–Can Mitjans
- Polizur–Can Mitjans
- Can Fatjó Sud
- Xarau–Santa Anna
- Can Fatjó Nord
- UAB Parc de Recerca Sud
- Carretera de Barcelona

This is a useful **northern/eastern control option**, although some areas are more technology-oriented than traditional industrial estates.

---

# 4.8 Candidate Industrial Areas for the Project

We can now reduce the large number of industrial estates to **six analytical candidate areas**.

| ID | Candidate area | Municipality / corridor | Initial relevance |
| --- | --- | --- | --- |
| **IA-T** | Els Bellots – Santa Margarida – Can Parellada | Terrassa | High |
| **IA-S1** | Sud-Oest – Sant Pau de Riu-sec | Sabadell | High |
| **IA-S2** | Sabadell Parc Empresarial – Can Roqueta | Sabadell | High |
| **IA-R1** | Can Sant Joan – Can Jardí | Rubí | High |
| **IA-R2** | Rubí central/south industrial corridor | Rubí | Medium–High |
| **IA-C** | Cerdanyola industrial corridor | Cerdanyola | Medium |

Sant Cugat industrial areas can remain within the broader Rubí/Sant Cugat candidate geography and can be reconsidered during the property search if suitable premises are found.

---

# 4.9 Why These Six Areas?

The selection is deliberately based on **geographical screening**, not on a premature scoring system.

The six areas provide coverage of the main geographical alternatives:

```
                 Cerdanyola
                    IA-C
                      |
                      |
              Sant Cugat
                 /    |
               /      |
          IA-R1       IA-R2
             RUBÍ
                \
                 \
              IA-S1
             SABadell
                 |
              IA-S2
                 |
                 |
               IA-T
             TERRASSA
```

The actual geometry is more complex than this schematic, but conceptually these candidates cover the major industrial corridors around the hospital network.

---

# 4.10 Screening Criteria for the Next Phase

We should **not yet assign numerical scores** to these areas.

That belongs to the Factor Rating Method.

For Phase 4, we only establish the criteria that will later help us decide whether an area deserves further property investigation:

| Criterion | Purpose |
| --- | --- |
| Industrial land/use | Basic feasibility |
| Road accessibility | Laundry collection/delivery |
| Proximity to hospital network | Transport efficiency |
| Availability of premises | Real-property feasibility |
| Potential premises size | Laundry capacity |
| Utility infrastructure | Industrial operation |
| Heavy/light vehicle access | Logistics |
| Distance from residential concentration | Potential operational compatibility |
| Property cost | Economic feasibility |

These criteria will later be converted into formal **Factor Rating criteria** in Phase 8.

---

# 4.11 Important Methodological Decision

There is a temptation to identify the "best" industrial area now.

We should **not do that**.

At this stage:

> **Industrial areas are candidate geographical zones, not ranked alternatives.**

The Center of Gravity will provide a theoretical location. The transportation model will provide actual distances. The Factor Rating Model will assess qualitative criteria. The Cost Model will assess economic consequences. The Graph Models will provide additional network-based evidence.

Only then should we select the actual premise.

This keeps the four methods independent and avoids **pre-selecting a location before performing the analysis**.

---

# Phase 4 Decision

The project will carry forward the following six candidate industrial areas:

$$
\boxed{
IA\text{-}T,\ IA\text{-}S1,\ IA\text{-}S2,\ IA\text{-}R1,\ IA\text{-}R2,\ IA\text{-}C
}
$$

with the following working labels:

- **IA-T:** Terrassa — Els Bellots/Santa Margarida/Can Parellada
- **IA-S1:** Sabadell — Sud-Oest/Sant Pau de Riu-sec
- **IA-S2:** Sabadell — Parc Empresarial/Can Roqueta
- **IA-R1:** Rubí — Can Sant Joan/Can Jardí
- **IA-R2:** Rubí — central/south industrial corridor
- **IA-C:** Cerdanyola industrial corridor

### Critical rationale

> **The candidate areas were selected to cover the main industrial corridors surrounding the hospital demand network while keeping the subsequent property search manageable.**

---

# Phase 4 Status

**🟢 PHASE 4 — COMPLETED**

We now have:

- [x]Industrial geography identified
- [x]Municipal industrial-area sources identified
- [x]Major industrial corridors screened
- [x]Six candidate areas established
- [x]Candidate IDs assigned
- [x]Preliminary suitability understood
- [x]No premature ranking performed

### Updated roadmap

```
PHASE 0   Project definition                  ██████████  DONE
PHASE 1   Hospital dataset                    ██████████  DONE
PHASE 2   Demand & assumptions                ██████████  DONE
PHASE 3   Geographic dataset                  ██████████  DONE
PHASE 4   Industrial areas                    ██████████  DONE
PHASE 5   Center of Gravity                   ░░░░░░░░░░  NEXT
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

## Next: Phase 5 — Center of Gravity

We now have everything required to calculate the **theoretical Center of Gravity**:

$$
X_{COG}=\frac{\sum X_iW_i}{\sum W_i}
$$

$$
Y_{COG}=\frac{\sum Y_iW_i}{\sum W_i}
$$

The important next step will be to calculate it using the **projected coordinates**, identify the resulting real-world location, and then determine **which of our industrial areas is closest to the theoretical optimum**.

That will give us our first genuine location result before we investigate individual premises.


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
