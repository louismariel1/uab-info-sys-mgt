# Updated Chapters 1–2 — Academic Project Report

Chapters 1–2 — Introduction and Data Collection

# 1\. Introduction

## 1.1 Problem Definition

The project addresses the location of a proposed **centralized industrial hospital laundry serving hospitals in Vallès Occidental, Catalonia**.

The laundry would receive soiled hospital linen from participating hospitals, process it in a centralized industrial facility, and return clean linen to the hospitals. The location of the facility is therefore an important operational decision because it affects transportation requirements, facility costs, accessibility, and the overall efficiency of the service.

The assignment requires the selection of a **real existing premise that is available and suitable** for the proposed function. The location decision is therefore approached as a practical facility-location problem rather than as a purely theoretical mathematical exercise.

Because actual hospital laundry-generation data and detailed operational information were not available directly from the hospitals, publicly available information is used together with explicitly documented project assumptions.

## 1.2 Project Objective

The main objective is to identify the **best possible location for a centralized industrial hospital laundry serving the selected hospitals of Vallès Occidental**.

The analysis combines four location methods studied in the course:

1. Center of Gravity Method;
2. Factor Rating Method;
3. Cost Model;
4. Graph-Based Models:
   - Simple Median Model;
   - Coverage Model.

The results of the different methods will subsequently be compared and used to support the selection of a **real available industrial premise**.

The final decision will consider both the quantitative results of the location models and the practical suitability of the selected property.

## 1.3 Study Area

The study focuses on the **Vallès Occidental comarca in Catalonia**, with the hospital network concentrated principally around Sabadell, Terrassa, Sant Cugat del Vallès and the surrounding industrial corridor.

The selected hospital service points are distributed geographically across the main population and industrial centres of the comarca. The resulting network provides a suitable basis for analysing alternative locations for a centralized laundry facility.

The principal demand centres are Sabadell and Terrassa, with additional demand in the Sant Cugat/Rubí area.

## 1.4 Centralized Hospital Laundry Concept

A centralized hospital laundry is considered as a specialized industrial service facility serving several hospitals from a common location.

The proposed operating concept is:

**Hospitals → Collection/transport → Centralized industrial laundry → Processing → Clean-linen delivery → Hospitals**

Centralization can potentially provide operational advantages through economies of scale, specialized equipment, standardized processes, and centralized management.

However, centralization also creates transportation requirements because linen must be collected from and delivered to multiple hospitals. Consequently, the location of the laundry must balance **demand distribution, transportation accessibility, property suitability, and cost**.

For this project, the location decision is therefore treated as a multi-criteria facility-location problem.

---

# 2\. Data Collection and Assumptions

## 2.1 Hospital Network

The hospital network was constructed using publicly available hospital information. The **2025 National Catalogue of Hospitals** published by the Spanish Ministry of Health was used as the principal source for hospital identification and installed-bed information.

A practical inclusion criterion was established: hospitals or hospital service points with at least **50 installed beds** were included in the core network.

Facilities below this threshold were excluded from the main model.

Mútua de Terrassa and Àptima Centre Clínic were combined into a single geographical service point because they are located at the same address.

The resulting network contains **seven hospital service points**.

| ID | Hospital / Service Point | Municipality | Installed Beds |
| --- | --- | --- | --- |
| H01 | Hospital de Sabadell – Parc Taulí | Sabadell | 861 |
| H02 | Hospital de Terrassa | Terrassa | 460 |
| H03 | Mútua de Terrassa + Àptima Centre Clínic | Terrassa | 604 |
| H04 | Hospital Universitari General de Catalunya | Sant Cugat del Vallès | 304 |
| H05 | Centre de Prevenció i Rehabilitació Asepeyo | Sant Cugat del Vallès | 138 |
| H06 | Hospital de Sant Llàtzer | Terrassa | 77 |
| H07 | Hospital Quirónsalud del Vallès – Clínica del Vallès | Sabadell | 71 |
| **Total** |  |  | **2,515** |

The resulting network represents **2,515 installed beds**.

## 2.2 Hospital Locations and Coordinates

Geographical coordinates were assigned to each hospital service point using publicly available mapping and geospatial sources.

The master coordinate representation is **WGS84 latitude and longitude**. Where projected coordinates are required for geographical calculations, the project uses **ETRS89 / UTM Zone 31N**.

The final geographical dataset is:

| ID | Hospital / Service Point | Latitude | Longitude | Demand Weight |
| --- | --- | --- | --- | --- |
| H01 | Hospital de Sabadell – Parc Taulí | 41.55719 | 2.10989 | 861 |
| H02 | Hospital de Terrassa | 41.55679 | 2.05277 | 460 |
| H03 | Mútua de Terrassa + Àptima Centre Clínic | 41.56383 | 2.01718 | 604 |
| H04 | Hospital Universitari General de Catalunya | 41.47491 | 2.04463 | 304 |
| H05 | Centre de Prevenció i Rehabilitació Asepeyo | 41.49010 | 2.07843 | 138 |
| H06 | Hospital de Sant Llàtzer | 41.56261 | 2.01721 | 77 |
| H07 | Hospital Quirónsalud del Vallès – Clínica del Vallès | 41.53233 | 2.11760 | 71 |

These coordinates are used as the hospital locations for the subsequent geographical models.

## 2.3 Demand Estimation

Actual hospital laundry volumes were not publicly available. Therefore, **installed hospital beds are used as the relative demand weight**.

For hospital $i$:

$$
w_i=B_i
$$

where $B_i$ is the number of installed beds.

For estimating the physical scale of the proposed laundry, a planning factor of:

$$
3.0\ kg/bed/day
$$

is adopted.

Estimated daily laundry demand is therefore:

$$
D_i=B_i\times3.0
$$

The resulting total base demand is:

$$
2,515\times3.0=7,545\ kg/day
$$

Therefore, the project uses:

$$
\boxed{7,545\ kg/day}
$$

or approximately:

$$
\boxed{7.55\ tonnes/day}
$$

as the **base demand** for subsequent analysis.

| ID | Beds | Demand Weight | Estimated Laundry Demand |
| --- | --- | --- | --- |
| H01 | 861 | 861 | 2,583 kg/day |
| H02 | 460 | 460 | 1,380 kg/day |
| H03 | 604 | 604 | 1,812 kg/day |
| H04 | 304 | 304 | 912 kg/day |
| H05 | 138 | 138 | 414 kg/day |
| H06 | 77 | 77 | 231 kg/day |
| H07 | 71 | 71 | 213 kg/day |
| **Total** | **2,515** | **2,515** | **7,545 kg/day** |

**Rationale:** Beds are used as the demand proxy because comparable actual laundry-volume data are unavailable.

## 2.4 Candidate Industrial Areas

The industrial-area search identified the principal industrial corridors surrounding the hospital network.

Rather than treating every individual industrial estate as a separate alternative, related industrial estates were grouped into practical geographical candidate areas. This keeps the subsequent property search manageable while preserving the major location alternatives.

Six candidate industrial areas were established:

| ID | Candidate Industrial Area | Main Municipality / Corridor |
| --- | --- | --- |
| IA-T | Els Bellots – Santa Margarida – Can Parellada | Terrassa |
| IA-S1 | Sud-Oest – Sant Pau de Riu-sec | Sabadell |
| IA-S2 | Sabadell Parc Empresarial – Can Roqueta | Sabadell |
| IA-R1 | Can Sant Joan – Can Jardí | Rubí |
| IA-R2 | Rubí Central/South Industrial Corridor | Rubí |
| IA-C | Cerdanyola Industrial Corridor | Cerdanyola del Vallès |

These areas represent the principal industrial alternatives surrounding the hospital demand network.

**Rationale:** The candidate areas were selected to provide broad geographical coverage of the hospital network while keeping the later search for real premises manageable.

## 2.5 Candidate Premises

Individual premises have not yet been selected.

The project will identify and evaluate **real, existing and available premises** after the theoretical and geographical location analysis has been performed.

The premise search will focus primarily on the candidate industrial areas identified above.

Each shortlisted property will subsequently be evaluated according to:

- location;
- industrial classification;
- available floor area;
- suitability for the estimated laundry throughput;
- accessibility;
- vehicle access;
- infrastructure;
- availability;
- purchase or rental cost;
- and compatibility with the proposed industrial laundry operation.

The final selected premise must satisfy the assignment requirement of being a **real and available property**.

## 2.6 Transportation Data

Transportation data have not yet been finalized.

For the subsequent analysis, road distances and travel times will be calculated between the hospitals and the candidate premises.

The transportation analysis will use:

- hospital addresses as origins/destinations;
- candidate property addresses as facility locations;
- road-network distances rather than straight-line distance;
- travel time where relevant.

Transportation data will subsequently support the Cost Model and Graph-Based Models.

## 2.7 Key Assumptions and Limitations

The project is based on publicly available information and therefore includes several necessary assumptions.

The principal assumptions are:

- Actual hospital laundry volumes are unavailable; installed beds are therefore used as the demand proxy.
- A base planning factor of **3.0 kg/bed/day** is used.
- Installed beds are used rather than occupied beds because comparable occupancy data are unavailable for all hospitals.
- Mútua de Terrassa and Àptima Centre Clínic are represented as one geographical service point because they share the same location.
- Hospital coordinates represent the geographical service point rather than a specific loading dock or entrance.
- The analysis uses a **single base-demand scenario**, consistent with the practical scope of the assignment.
- Candidate industrial areas are geographical search zones rather than final location decisions.
- The final recommendation must be based on a real premise that is available and suitable for the proposed operation.

These assumptions are considered acceptable for a practical facility-location study where direct operational data from the hospitals are unavailable.

This gives us a good **stable baseline for the report**. From this point onward, we should avoid repeatedly rewriting Chapters 1–2 unless a later phase discovers a material data error.

The next work can therefore concentrate entirely on **Phase 5 — Center of Gravity**, using the frozen H01–H07 geographic and demand dataset.
