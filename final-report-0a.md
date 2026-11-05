# Centralized Hospital Laundry Location Study

## Location Analysis for a Centralized Hospital Laundry in Vallès Occidental, Catalonia

**Group Members:** Meabh Geary – 1829913; Thea Isberg – 1822816; Annemyn Ooschoeu – 1829120; Louis-Marie Loe – 1833548

**Report status:** Final analytical location study completed; preferred location selected.

**Study area:** Vallès Occidental, Barcelona, Catalonia, Spain.

**Selected location:** **Industrial warehouse in Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain).**

---

# Executive Summary

This study evaluates six candidate industrial areas for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental, Catalonia.

The healthcare network comprises 2,515 beds. Using an assumed laundry-generation factor of 3.0 kg per bed per day, the estimated processing demand is:

- **Daily demand:** 7,545 kg/day.
- **Annual demand:** 2,753,925 kg/year.

Four complementary location-analysis methods are applied:

1. Centre of Gravity Method.
2. Factor-Rating Method.
3. Cost Model.
4. Geographic Coverage Method.

Each method evaluates a different aspect of the location decision.

| Method | Preferred result | Main finding |
| --- | --- | --- |
| Centre of Gravity | Camí de Can Coniller, Terrassa | Demand-weighted geographical balance |
| Factor-Rating | IA-S2 — Can Roqueta | Highest qualitative score: 4.20/5 |
| Cost Model | IA-R2 — Cova Solera | Lowest estimated annual equivalent cost |
| Geographic Coverage | IA-T — Els Bellots | Highest baseline coverage: 87.9% |

The project owner's principal priority is to compare transport-supply, transport-distribution and operating costs, including fixed, variable and establishment costs. This priority align with the Cost Model. Consequently, **the Cost Model is the controlling method for the final selection**.

The Cost Model identifies **Cova Solera, Rubí**, as the lowest-cost candidate: **Estimated annual equivalent cost: €1,821,014.**

**Final Selection:** An industrial warehouse in **Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain)** as the preferred location under the adopted assumptions. A publicly available property listing provides indicative evidence of a warehouse of approximately 1,500 m² in Cova Solera, with an asking rent of approximately €6,000/month.

---

# 1\. Introduction

## 1.1 Project Background

This study evaluates potential locations for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental.

The proposed facility will collect soiled textiles, process them centrally and distribute clean textiles to the healthcare facilities.

Location affects transport requirements, delivery distances, property costs and operating expenditure. The study therefore compares candidate industrial areas using geographical, qualitative and economic criteria.

## 1.2 Objective of the Location Study

The objective is to identify the most appropriate industrial location by applying four complementary methods:

- Centre of Gravity Method.
- Factor-Rating Method.
- Cost Model.
- Geographic Coverage Method.

## 1.3 Study Methodology and Scope

The study is geographically limited to Vallès Occidental, Catalonia, which defines the regional scope for both healthcare demand and potential locations for the centralized laundry facility.

Seven healthcare facilities within this region were identified as demand points, and six existing industrial areas were shortlisted as potential locations.

The shortlist was based on their geographical position, their identification as established industrial areas or corridors, and the availability of relevant public geographical and industrial information.

---

# 2\. Data Collection and Assumptions

## 2.1 Healthcare Facilities

The proposed laundry will serve seven healthcare facilities.

| ID | Hospital / Service Point | Municipality | Beds |
| --- | --- | --- | --- |
| H01 | Hospital de Sabadell – Parc Taulí | Sabadell | 861 |
| H02 | Hospital de Terrassa | Terrassa | 460 |
| H03 | Mútua de Terrassa + Àptima Centre Clínic | Terrassa | 604 |
| H04 | Hospital Universitari General de Catalunya | Sant Cugat del Vallès | 304 |
| H05 | Centre de Prevenció i Rehabilitació Asepeyo | Sant Cugat del Vallès | 138 |
| H06 | Hospital de Sant Llàtzer | Terrassa | 77 |
| H07 | Hospital Quirónsalud del Vallès | Sabadell | 71 |
|  | **Total** |  | **2,515** |

The three largest service points (H01, H02 and H03) account for 1,925 beds.

Their share of total demand weight is:

$$
\frac{861+460+604}{2515}\times100
=76.54\%
$$

Approximately 76.5% of the demand weight is concentrated in these three facilities.

## 2.2 Laundry Demand Estimation

An average laundry-generation rate of 3.0 kg per bed per day is assumed.

The estimated daily demand is:

$$
Q_{\text{daily}}=N\times L
$$

Where:

- $N$ = Total number of beds.
- $L$ = Laundry-generation factor.

Substituting the project values:

$$
Q_{\text{daily}}=2515\times3.0
$$

$$
\boxed{Q_{\text{daily}}=7,545\text{ kg/day}}
$$

Assuming 365 operating days per year:

$$
Q_{\text{annual}}=Q_{\text{daily}}\times365
$$

$$
Q_{\text{annual}}=7545\times365
$$

$$
\boxed{Q_{\text{annual}}=2,753,925\text{ kg/year}}
$$

The 3.0 kg/bed/day factor is a planning assumption, not measured consumption data from the individual hospitals.

## 2.3 Geographical Data

Hospital and candidate-area coordinates are expressed in WGS84 (EPSG:4326).

For the Centre of Gravity calculation, the latitude and longitude values are weighted directly using hospital bed capacity.

This produces an approximate geographical centre expressed in latitude and longitude.

### 2.3.1 Hospital Coordinates

| ID | Latitude | Longitude |
| --- | --- | --- |
| H01 | 41.55719 | 2.10989 |
| H02 | 41.55679 | 2.05277 |
| H03 | 41.56383 | 2.01718 |
| H04 | 41.47491 | 2.04463 |
| H05 | 41.49010 | 2.07843 |
| H06 | 41.56261 | 2.01721 |
| H07 | 41.53233 | 2.11760 |

### 2.3.2 Candidate Industrial Areas

The following table presents the six candidate industrial areas, their respective municipalities and geographical coordinates in WGS84 (EPSG:4326).

| ID | Candidate Industrial Area | Municipality | Latitude | Longitude |
| --- | --- | --- | --- | --- |
| IA-T | Els Bellots / Santa Margarida / Can Parellada | Terrassa | 41.549829 | 2.041354 |
| IA-S1 | Sud-Oest / Sant Pau de Riu-sec | Sabadell | 41.513398 | 2.099462 |
| IA-S2 | Sabadell Parc Empresarial / Can Roqueta | Sabadell | 41.540064 | 2.133064 |
| IA-R1 | Can Sant Joan / Can Jardí | Rubí | 41.473458 | 2.020948 |
| IA-R2 | Central/southern industrial corridor / Cova Solera | Rubí | 41.482667 | 2.026944 |
| IA-C | Cerdanyola industrial corridor / Parc de l'Alba | Cerdanyola del Vallès | 41.486013 | 2.106586 |

Methodological note: The coordinates represent reference points within the respective industrial areas and are used consistently to calculate straight-line geographical distances between each candidate and the seven healthcare facilities. 

The six candidate areas were identified within the defined regional study scope. Each candidate is evaluated against the complete network of seven healthcare facilities, irrespective of the municipality in which the candidate area is located.

## 2.4 General Modelling Assumptions

| Parameter | Adopted assumption |
| --- | --- |
| Healthcare facilities | 7 |
| Total demand weight | 2,515 beds |
| Laundry-generation factor | 3.0 kg/bed/day |
| Daily demand | 7,545 kg/day |
| Annual demand | 2,753,925 kg/year |
| Candidate industrial areas | 6 |
| Reference warehouse area | 1,500 m² |
| Factor-Rating scale | 1–5 |
| Baseline coverage radius | 7.5 km |
| Road-distance conversion factor | 1.30 |
| Transport cost benchmark | €1.424/km |
| Annual operating days | 365 |

## 2.5 Data Limitations

The study uses:

- Bed capacity as a proxy for laundry demand.
- Representative industrial-area coordinates.
- Indicative asking rents rather than agreed lease prices.
- Straight-line geographical distances for geographical analysis.
- Estimated transport distances and frequencies rather than verified vehicle routes.
- Planning assumptions for fixed, variable and establishment costs.

These assumptions provide a consistent basis for comparing the six candidates. They are not verified operational or commercial quotations.

---

# 3\. Centre of Gravity Method

## 3.1 Methodology

The Centre of Gravity Method identifies a geographical location using the coordinates and demand weights of the healthcare facilities.

In this study, the geographical centre is calculated by weighting the latitude and longitude of each hospital according to its number of beds.

The weighted latitude is:

$$
Latitude^*=
\frac{\sum_{i=1}^{n}W_iLatitude_i}
{\sum_{i=1}^{n}W_i}
$$

The weighted longitude is:

$$
Longitude^*=
\frac{\sum_{i=1}^{n}W_iLongitude_i}
{\sum_{i=1}^{n}W_i}
$$

Where:

- $Latitude_i$ = Latitude of hospital $i$.
- $Longitude_i$ = Longitude of hospital $i$.
- $W_i$ = Number of beds at hospital $i$.
- $n$ = Number of healthcare facilities.

The total demand weight is the total number of beds:

$$
\sum_{i=1}^{7}W_i=2515
$$

## 3.2 Coordinate Reference and Calculation Approach

The original hospital coordinates are expressed in WGS84 (EPSG:4326).

For this study, the weighted average is calculated directly using the latitude and longitude values.

This approach provides an approximate geographical centre suitable as center of gravity.

The resulting latitude and longitude are subsequently used to identify a nearby postal address through a reverse-geocoding service.

## 3.3 Weighted Coordinate Calculations

### 3.3.1 Weighted Latitude Calculation

The general formula is:

$$
Latitude^*=
\frac{\sum_{i=1}^{7}W_iLatitude_i}
{\sum_{i=1}^{7}W_i}
$$

Expanding the formula for all seven healthcare facilities:

$$
Latitude^*=
\frac{
W_1Latitude_1+
W_2Latitude_2+
\cdots+
W_7Latitude_7
}{2515}
$$

Substituting the actual bed capacities and latitude values from Section 2.3.1:

$$
\begin{aligned}
Latitude^*=\frac{1}{2515}[&
861(41.55719)\\
&+460(41.55679)\\
&+604(41.56383)\\
&+304(41.47491)\\
&+138(41.49010)\\
&+77(41.56261)\\
&+71(41.53233)]
\end{aligned}
$$

Calculating the individual weighted values:

$$
\begin{aligned}
Latitude^*=\frac{1}{2515}[&
35,780.73859\\
&+19,117.12340\\
&+25,184.95332\\
&+12,608.57264\\
&+6,896.23380\\
&+3,840.92197\\
&+2,565.99643]
\end{aligned}
$$

Adding the weighted values gives the numerator:

$$
\sum W_iLatitude_i=104,484.54015
$$

The complete calculation is therefore:

$$
Latitude^*=
\frac{104,484.54015}{2515}
$$

$$
\boxed{Latitude^*=41.5445487674^\circ}
$$

Rounded to four decimal places:

$$
\boxed{Latitude^*=41.5445^\circ}
$$

### 3.3.2 Weighted Longitude Calculation

The general formula is:

$$
Longitude^*=
\frac{\sum_{i=1}^{7}W_iLongitude_i}
{\sum_{i=1}^{7}W_i}
$$

Expanding the formula for all seven healthcare facilities:

$$
Longitude^*=
\frac{
W_1Longitude_1+
W_2Longitude_2+
\cdots+
W_7Longitude_7
}{2515}
$$

Substituting the actual bed capacities and longitude values from Section 2.3.1:

$$
\begin{aligned}
Longitude^*=\frac{1}{2515}[&
861(2.10989)\\
&+460(2.05277)\\
&+604(2.01718)\\
&+304(2.04463)\\
&+138(2.07843)\\
&+77(2.01721)\\
&+71(2.11760)]
\end{aligned}
$$

Calculating the individual weighted values:

$$
\begin{aligned}
Longitude^*=\frac{1}{2515}[&
1,816.61529\\
&+944.27420\\
&+1,218.37872\\
&+621.16752\\
&+286.82334\\
&+155.32517\\
&+150.74760]
\end{aligned}
$$

Adding the weighted values gives the numerator:

$$
\sum W_iLongitude_i=5193.33184
$$

The complete calculation is therefore:

$$
Longitude^*=
\frac{5193.33184}{2515}
$$

$$
\boxed{Longitude^*=2.0649430775^\circ}
$$

Rounded to four decimal places:

$$
\boxed{Longitude^*=2.0649^\circ}
$$

### 3.3.3 Final Centre of Gravity Coordinates

Combining the two calculated coordinates gives:

| Coordinate | Calculated result |
| --- | --- |
| Weighted latitude | 41.5445487674° |
| Weighted longitude | 2.0649430775° |

Therefore, the approximate weighted geographical centre is:

$$
\boxed{41.5445^\circ\text{ N},\quad2.0649^\circ\text{ E}}
$$

## 3.4 Reverse Geocoding and Address Identification

The calculated coordinates were independently checked using the GPS-Coordinates.net reverse-geocoding service.

The service returned the following nearby postal address: **Camí de Can Coniller, 08220 Terrassa, Spain.**

The corresponding coordinates are: 

- Latitude: 41.5448
- Longitude: 2.0649

The postal address is a geographical identification of the calculated centre.

## 3.5 Interpretation

The Centre of Gravity Method identifies  **Camí de Can Coniller, 08220 Terrassa, Barcelona, Spain**.

The result represents the geographical balance of the seven healthcare facilities, weighted by their respective bed capacities.

However, the business owner's strategy being the Cost Model, the Center of Gravity will not determine the final Laundry location.

---

# 4\. Factor-Rating Method

## 4.1 Methodology

The Factor-Rating Method compares candidate locations using weighted qualitative criteria.

Each criterion receives a weight, and each candidate receives a score from 1 (least favourable) to 5 (most favourable).

The weighted score is:

$$
S_j=\sum_{k=1}^{m}w_kr_{jk}
$$

Where:

- $S_j$ = Weighted score of candidate $j$.
- $w_k$ = Weight of criterion $k$.
- $r_{jk}$ = Candidate score for criterion $k$.
- $m$ = Number of criteria.

The maximum possible score is 5.

## 4.2 Evaluation Criteria

| Criterion | Weight |
| --- | --- |
| Proximity to healthcare facilities | 25% |
| Road accessibility | 20% |
| Evidence of suitable premises | 20% |
| Industrial compatibility | 15% |
| Utilities and infrastructure | 10% |
| Environmental and residential compatibility | 10% |
| **Total** | **100%** |

## 4.3 Candidate Scores

| Candidate | Proximity | Roads | Premises | Industrial | Utilities | Environment |
| --- | --- | --- | --- | --- | --- | --- |
| IA-T | 5 | 4 | 3 | 5 | 3 | 3 |
| IA-S1 | 4 | 4 | 2 | 5 | 3 | 3 |
| IA-S2 | 3 | 5 | 5 | 5 | 4 | 3 |
| IA-R1 | 2 | 4 | 4 | 5 | 4 | 3 |
| IA-R2 | 2 | 4 | 4 | 5 | 4 | 3 |
| IA-C | 2 | 5 | 2 | 3 | 4 | 3 |

The scores are indicative comparative assessments based on available geographical and industrial evidence. They are not the result of formal site inspections or technical audits.

## 4.4 Weighted Results

For IA-S2 — Can Roqueta:

$$
\begin{aligned}
S_{\text{IA-S2}}={}&0.25(3)+0.20(5)+0.20(5)\\
&+0.15(5)+0.10(4)+0.10(3)
\end{aligned}
$$

$$
S_{\text{IA-S2}}=
0.75+1.00+1.00+0.75+0.40+0.30
$$

$$
\boxed{S_{\text{IA-S2}}=4.20/5}
$$

The weighted results for all candidates are:

| Candidate | Weighted Score | Rank |
| --- | --- | --- |
| **IA-S2 — Can Roqueta** | **4.20** | **1** |
| IA-T — Els Bellots | 4.00 | 2 |
| IA-S1 — Sant Pau de Riu-sec | 3.55 | 3 |
| IA-R1 — Can Jardí | 3.55 | 3 |
| IA-R2 — Cova Solera | 3.55 | 3 |
| IA-C — Cerdanyola | 3.05 | 6 |

**IA-S2 — Can Roqueta** achieves the highest weighted score of 4.20/5, followed by IA-T — Els Bellots with 4.00/5.

## 4.5 Interpretation

The Factor-Rating Method identifies IA-S2 — Can Roqueta as the highest-scoring candidate.

Its result is supported by its favourable assessment of road accessibility, evidence of suitable industrial premises and industrial compatibility.

The Factor-Rating Method is a qualitative assessment. Its result depends on the selected criteria, weights and assigned scores.

It complements, but does not replace the Cost Model which has priority in the current study. 

---

# 5\. Cost Model

## 5.1 Methodology

The Cost Model compares the estimated annual costs of operating the centralized laundry at each candidate location.

The model includes:

- Property rental.
- Transport-supply.
- Transport-distribution.
- Fixed operating costs.
- Variable processing costs.
- Establishment costs.

The objective is to identify the candidate with the lowest estimated annual equivalent cost.

## 5.2 Transport Cost Estimation

The model converts geographical distance into estimated road distance:

$$
d_{\text{road}}=d_{\text{map}}\times f
$$

Transport cost is estimated using:

$$
C_{\text{transport}}=
d_{\text{map}}\times f\times q\times c\times n
$$

Where:

- $d_{\text{map}}$ = Geographical distance.
- $f$ = Road-distance conversion factor.
- $q$ = Number of journeys per operating period.
- $c$ = Transport cost per kilometre.
- $n$ = Number of operating periods per year.

The adopted assumptions are:

| Parameter | Assumption |
| --- | --- |
| Road-distance conversion factor | 1.30 |
| Transport cost benchmark | €1.424/km |
| Distribution tours | 2 complete multi-stop tours/day |
| Distribution operating days | 365 days/year |
| Supply journeys | 2 round trips/week |
| Supply operating weeks | 52 weeks/year |

The €1.424/km benchmark is based on an indicative Spanish articulated-vehicle operating-cost reference. It is a comparative cost proxy, not a quotation from a laundry transport provider.

### Distribution Transport

Two complete multi-stop tours per day are assumed:

1. Clean-linen delivery to the seven healthcare facilities.
2. Soiled-linen collection from the seven healthcare facilities.

A nearest-neighbour sequence based on representative geographical coordinates is used to estimate the tours.

### Supply Transport

Two weekly round trips are assumed between each candidate laundry location and a representative supplier hub in the Barcelona area.

The resulting estimates are based on converted geographical distances and assumed operating frequencies, not verified vehicle routes or transport-provider quotations.

## 5.3 Annual Transport Costs

| Candidate | Distribution/year | Supply/year | Combined/year |
| --- | --- | --- | --- |
| IA-T — Els Bellots | €43,544 | €9,213 | €52,757 |
| IA-S1 — Sant Pau de Riu-sec | €43,854 | €7,161 | €51,015 |
| IA-S2 — Can Roqueta | €47,740 | €8,028 | €55,768 |
| IA-R1 — Can Jardí | €42,838 | €6,698 | €49,536 |
| IA-R2 — Cova Solera | €41,392 | €6,837 | €48,229 |
| IA-C — Cerdanyola | €49,670 | €5,940 | €55,610 |

Combined transport cost is:

$$
C_{\text{transport}}=
C_{\text{distribution}}+C_{\text{supply}}
$$

For Cova Solera:

$$
C_{\text{transport,IA-R2}}=
41,392+6,837
$$

$$
\boxed{C_{\text{transport,IA-R2}}=€48,229/year}
$$

Cova Solera has both the lowest estimated distribution transport cost (€41,392/year) and the lowest combined supply and distribution transport cost (€48,229/year) among the six candidate locations.

## 5.4 Property Rental Costs

A common reference warehouse area of 1,500 m² is used for all candidates.

The annual rental cost is:

$$
C_{\text{rent}}=R\times A\times12
$$

Where:

- $R$ = Monthly rental rate (€ / m²).
- $A$ = Reference warehouse area (m²).
- $12$ = Months per year.

For Cova Solera:

$$
C_{\text{rent}}=4.00\times1,500\times12
$$

$$
\boxed{C_{\text{rent}}=€72,000/year}
$$

The comparative rental estimates are:

| Candidate | Indicative rent €/m²/month | Annual rent |
| --- | --- | --- |
| IA-R2 — Cova Solera | €4.00 | €72,000 |
| IA-R1 — Can Jardí | €4.80 | €86,400 |
| IA-S2 — Can Roqueta | €5.00 | €90,000 |
| IA-S1 — Sant Pau de Riu-sec | €5.50 | €99,000 |
| IA-C — Cerdanyola | €5.45 | €98,100 |
| IA-T — Els Bellots | €5.95 | €107,100 |

These are indicative rental estimates, not confirmed contractual prices.

## 5.5 Fixed, Variable and Establishment Costs

The common operating-cost assumptions are:

| Cost component | Calculation | Annual cost |
| --- | --- | --- |
| Fixed operating costs | Planning estimate | €1,000,000 |
| Variable processing costs | €0.20 × 2,753,925 kg | €550,785 |
| Establishment costs | €1,500,000 / 10 years | €150,000 |
| **Total common annual cost** |  | **€1,700,785** |

### Variable Processing Costs

$$
C_{\text{variable}}=
Q_{\text{annual}}\times c_{\text{variable}}
$$

$$
C_{\text{variable}}=
2,753,925\times0.20
$$

$$
\boxed{C_{\text{variable}}=€550,785/year}
$$

### Annual Establishment Cost

The €1,500,000 establishment investment is allocated over ten years using a simple straight-line method:

$$
C_{\text{establishment,annual}}=
\frac{1,500,000}{10}
$$

$$
\boxed{C_{\text{establishment,annual}}=€150,000}
$$

### Total Common Annual Cost

$$
C_{\text{common}}=
C_{\text{fixed}}+
C_{\text{variable}}+
C_{\text{establishment,annual}}
$$

$$
C_{\text{common}}=
1,000,000+550,785+150,000
$$

$$
\boxed{C_{\text{common}}=€1,700,785/year}
$$

These figures are planning assumptions, not supplier quotations or a detailed financial feasibility estimate.

The establishment cost uses a simple straight-line annual allocation, without a financing rate or discounted cash-flow calculation.

Because these costs are held constant across all candidates, they do not affect the relative ranking.

## 5.6 Total Annual Equivalent Cost

The total annual equivalent cost is:

$$
\begin{aligned}
C_{\text{total},j}={}&C_{\text{rent},j}\\
&+C_{\text{supply},j}\\
&+C_{\text{distribution},j}\\
&+C_{\text{fixed}}\\
&+C_{\text{variable}}\\
&+\frac{C_{\text{establishment}}}{10}
\end{aligned}
$$

For Cova Solera:

$$
\begin{aligned}
C_{\text{total,IA-R2}}={}&72,000+6,837+41,392\\
&+1,000,000+550,785+150,000
\end{aligned}
$$

$$
\boxed{C_{\text{total,IA-R2}}=€1,821,014/year}
$$

### Cost Comparison

| Rank | Candidate | Rent | Transport | Common costs | Annual total |
| --- | --- | --- | --- | --- | --- |
| **1** | **IA-R2 — Cova Solera** | **€72,000** | **€48,229** | **€1,700,785** | **€1,821,014** |
| 2 | IA-R1 — Can Jardí | €86,400 | €49,536 | €1,700,785 | €1,836,721 |
| 3 | IA-S2 — Can Roqueta | €90,000 | €55,768 | €1,700,785 | €1,846,553 |
| 4 | IA-S1 — Sant Pau de Riu-sec | €99,000 | €51,015 | €1,700,785 | €1,850,800 |
| 5 | IA-C — Cerdanyola | €98,100 | €55,610 | €1,700,785 | €1,854,495 |
| 6 | IA-T — Els Bellots | €107,100 | €52,757 | €1,700,785 | €1,860,642 |

## 5.7 Cost Model Result

Cova Solera achieves the lowest estimated annual equivalent cost:

**€1,821,014/year.**

The second-ranked candidate, Can Jardí, has an estimated annual cost of €1,836,721.

The difference is:

$$
1,836,721-1,821,014
$$

$$
\boxed{€15,707/year}
$$

The economic advantage is relatively modest and depends on the adopted rental and transport assumptions.

Nevertheless, Cova Solera ranks first under the stated Cost Model and the project owner's priorities.

---

# 6. Geographic Coverage Method

## 6.1 Methodology and Objective

The Geographic Coverage Method evaluates how effectively each of the six candidate industrial areas serves the seven healthcare facilities within Vallès Occidental.

The method considers two geographical performance measures:

1. Weighted mean distance: Measures the average distance between a candidate location and the healthcare network, giving greater importance to hospitals with more beds.
2. Geographical coverage: Measures the proportion of total hospital-bed demand located within a specified distance of each candidate.

## 6.2 Straight-Line Distance Matrix

The first step is to calculate the distance between each of the seven healthcare facilities and each of the six candidate industrial areas.

This produces 42 individual distance measurements.

Table 6.1 – Straight-line distances between hospitals and candidate industrial areas (km)

| Hospital | IA-T | IA-S1 | IA-S2 | IA-R1 | IA-R2 | IA-C |
| --- | --- | --- | --- | --- | --- | --- |
| H01 | 5.76 | 4.95 | 2.71 | 11.90 | 10.79 | 7.92 |
| H02 | 1.23 | 6.20 | 6.94 | 9.64 | 8.52 | 9.06 |
| H03 | 2.54 | 8.85 | 10.00 | 10.05 | 9.06 | 11.41 |
| H04 | 8.34 | 6.26 | 10.33 | 1.98 | 1.71 | 5.31 |
| H05 | 7.32 | 3.13 | 7.18 | 5.13 | 4.37 | 2.39 |
| H06 | 2.46 | 8.76 | 9.96 | 9.92 | 8.93 | 11.31 |
| H07 | 6.64 | 2.59 | 1.55 | 10.37 | 9.35 | 5.23 |

All distances are expressed in kilometres and rounded to two decimal places.

The candidate industrial areas are:

- IA-T: Els Bellots, Terrassa.
- IA-S1: Sant Pau de Riu-sec, Sabadell.
- IA-S2: Can Roqueta, Sabadell.
- IA-R1: Can Jardí, Rubí.
- IA-R2: Cova Solera, Rubí.
- IA-C: Parc de l'Alba, Cerdanyola.

### Example of distance calculation

To demonstrate how the distances were obtained, consider Hospital H01 and candidate IA-T (Els Bellots).

Hospital H01:

- Latitude: 41.55719°
- Longitude: 2.10989°

IA-T:

- Latitude: 41.54983°
- Longitude: 2.04135°

The Haversine formula is used:

$$
a=\sin^2\left(\frac{\Delta\phi}{2}\right)
+\cos(\phi_1)\cos(\phi_2)
\sin^2\left(\frac{\Delta\lambda}{2}\right)
$$

$$
d=2R\arcsin(\sqrt a)
$$

Where:

- $\phi$ = Latitude in radians.
- $\lambda$ = Longitude in radians.
- $R=6371$ km = Approximate Earth radius.
- $d$ = Straight-line distance.

Substituting the geographical coordinates gives:

$$
\boxed{d_{\text{H01,IA-T}}=5.76\text{ km}}
$$

The same calculation is repeated for all 42 combinations.

## 6.3 Weighted Mean Distance

The weighted mean distance measures the average geographical distance between each candidate industrial area and the seven healthcare facilities.

Unlike a simple average, this method gives greater importance to hospitals with higher bed capacities.

The formula is:

$$
D_j=\frac{\sum_{i=1}^{7}W_i d_{ij}}
{\sum_{i=1}^{7}W_i}
$$

Where:

- $D_j$ = Weighted mean distance for candidate $j$.
- $W_i$ = Number of beds at hospital $i$.
- $d_{ij}$ = Distance between hospital $i$ and candidate $j$.
- $\sum W_i=2515$ = Total hospital-bed demand.

### Step 1: Establish the demand weights

| Hospital | Beds (weight) |
| --- | --- |
| H01 | 861 |
| H02 | 460 |
| H03 | 604 |
| H04 | 304 |
| H05 | 138 |
| H06 | 77 |
| H07 | 71 |
| Total | 2,515 |

### Step 2: Calculate the weighted mean distance for the Industrial Area. For example for Els Bellots

Using the distances from Table 6.1:

$$
\begin{aligned}
D_{\text{IA-T}}=\frac{1}{2515}[&
861(5.76)+460(1.23)\\
&+604(2.54)+304(8.34)\\
&+138(7.32)+77(2.46)\\
&+71(6.64)]
\end{aligned}
$$

The weighted distance numerator is:

$$
\begin{aligned}
={}&4959.36+565.80+1534.16\\
&+2535.36+1010.16+189.42+471.44
\end{aligned}
$$

$$
=\ 11265.70
$$

Therefore:

$$
D_{\text{IA-T}}=\frac{11265.70}{2515}
$$

$$
\boxed{D_{\text{IA-T}}=4.48\text{ km}}
$$

### Step 3: Compare all six candidates

The same calculation is applied to the remaining five candidates.

Table 6.2 – Weighted mean distance results

| Candidate | Weighted mean distance |
| --- | --- |
| IA-T — Els Bellots | 4.48 km |
| IA-S1 — Sant Pau de Riu-sec | 6.22 km |
| IA-S2 — Can Roqueta | 6.59 km |
| IA-C — Parc de l'Alba | 8.38 km |
| IA-R2 — Cova Solera | 8.41 km |
| IA-R1 — Can Jardí | 9.37 km |

Best geographical proximity: Els Bellots achieves the lowest weighted mean distance, indicating that it provides the closest overall geographical position relative to the demand-weighted hospital network.

## 6.4 Geographic Coverage Methodology

The second part of the analysis determines how many hospital beds are located within a defined geographical radius of each candidate.

A hospital is classified as covered when its straight-line distance from the candidate industrial area is equal to or less than the selected radius.

The baseline coverage radius is:

$$
\boxed{R=7.5\text{ km}}
$$

This is a project modelling assumption, not a statutory requirement or an established healthcare delivery standard.

### Step 1: Calculate covered demand

The covered demand formula is:

$$
C_j(R)=\sum_{i=1}^{7}W_i I(d_{ij}\leq R)
$$

Where:

- $C_j(R)$ = Total covered hospital beds.
- $W_i$ = Bed capacity of hospital $i$.
- $d_{ij}$ = Straight-line distance.
- $R$ = Coverage radius.
- $I$ = Indicator equal to 1 if the hospital is within the radius and 0 otherwise.

### Step 2: Convert covered demand into a percentage

$$
Coverage_j(R)=\frac{C_j(R)}{2515}\times100
$$

For Els Bellots, the hospitals within 7.5 km are H01, H02, H03, H05, H06 and H07.

Their combined bed capacity is:

$$
\begin{aligned}
C_{\text{IA-T}}(7.5)=
&861+460+604\\
&+138+77+71
\end{aligned}
$$

$$
\boxed{C_{\text{IA-T}}(7.5)=2211\text{ beds}}
$$

Hospital H04 is excluded because its distance from Els Bellots is 8.34 km.

The coverage percentage is:

$$
Coverage_{\text{IA-T}}=
\frac{2211}{2515}\times100 = 87.9
$$

This means that 87.9% of the total hospital-bed demand is located within 7.5 km of Els Bellots.

## 6.5 Baseline Geographic Coverage Results

The baseline comparison applies the 7.5 km coverage radius to all six candidates.

Table 6.3 – Geographic coverage at 7.5 km

| Candidate | Covered beds | Coverage |
| --- | --- | --- |
| IA-T — Els Bellots | 2,211 | 87.9% |
| IA-S1 — Sant Pau de Riu-sec | 1,834 | 72.9% |
| IA-S2 — Can Roqueta | 1,530 | 60.8% |
| IA-C — Parc de l'Alba | 513 | 20.4% |
| IA-R1 — Can Jardí | 442 | 17.6% |
| IA-R2 — Cova Solera | 442 | 17.6% |
| Total network demand | 2,515 | 100% |

Els Bellots achieves the highest geographical coverage, with 2,211 hospital beds within the baseline radius.

This represents a substantial geographical advantage over the other five candidates.

## 6.6 Sensitivity Analysis: Different Coverage Radii

To examine whether the results depend on the selected coverage radius, the calculations are repeated using three different geographical thresholds:

- 5 km: Relatively restrictive coverage.
- 7.5 km: Baseline coverage.
- 10 km: Wider geographical coverage.

The same coverage formula is applied:

$$
Coverage_j(R)=
\frac{C_j(R)}{2515}\times100
$$

Table 6.4 – Sensitivity analysis of geographic coverage

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| IA-T — Els Bellots | 45.4% | 87.9% | 100% |
| IA-S1 — Sant Pau de Riu-sec | 42.5% | 72.9% | 100% |
| IA-S2 — Can Roqueta | 37.1% | 60.8% | 87.9% |
| IA-R1 — Can Jardí | 12.1% | 17.6% | 38.9% |
| IA-R2 — Cova Solera | 17.6% | 17.6% | 65.8% |
| IA-C — Parc de l'Alba | 5.5% | 20.4% | 72.9% |

Coverage percentages calculated using the Table 6.1 distances rounded to two decimal places.### Interpretation of the Sensitivity Analysis

The results demonstrate that Els Bellots maintains the strongest geographical performance across all three coverage thresholds.

At 5 km, Els Bellots covers 45.4% of total hospital-bed demand, compared with 42.5% for Sant Pau de Riu-sec.

At 7.5 km, its coverage increases to 87.9%, maintaining its first position.

At 10 km, Els Bellots and Sant Pau de Riu-sec both achieve complete coverage of the healthcare network.

The sensitivity analysis therefore confirms that Els Bellots remains the strongest geographical candidate under the three tested distance assumptions.

## 6.7 Interpretation and Geographical Preference

The Geographic Coverage Method identifies IA-T — Els Bellots, Terrassa, as the strongest candidate from a geographical perspective.

This conclusion is supported by two results:

1. It achieves the lowest weighted mean distance of 4.48 km.
2. It achieves the highest baseline geographical coverage of 87.9% within the 7.5 km radius.

Furthermore, the sensitivity analysis demonstrates that Els Bellots maintains its geographical advantage when the coverage radius changes to 5 km or 10 km.

It is important to understand that the Geographic Coverage Method does not automatically select a final warehouse location. Instead, it identifies the candidate that provides the strongest geographical proximity and coverage of the hospital network.

The method does not account directly for property rental, establishment costs, fixed operating expenses or transport-provider costs.

Consequently, its result is complementary to the Cost Model.

Geographical preference: IA-T — Els Bellots.

However, the final project recommendation remains IA-R2 — Cova Solera, Rubí, because the project owner's principal decision criterion is the minimisation of total annual operating costs. Cova Solera achieves the lowest estimated annual equivalent cost in the Cost Model.

My recommendation is to retain this complete seven-part structure. It demonstrates the geographical method clearly, includes the necessary calculations and avoids unnecessary repetition.

The key distinction is now clear: Els Bellots wins the geographical analysis; Cova Solera wins the cost analysis and therefore remains the final selected location.

---

# 7\. Summary Results and Final Selection

## 7.1 Comparison of the Four Methods

| Method | Preferred result | Main result |
| --- | --- | --- |
| Centre of Gravity | Theoretical point near Terrassa | Demand-weighted geographical balance |
| Factor-Rating | IA-S2 — Can Roqueta | Highest score: 4.20/5 |
| Cost Model | IA-R2 — Cova Solera | Lowest annual cost: €1,821,014 |
| Geographic Coverage | IA-T — Els Bellots | 87.9% baseline coverage |

The methods produce different results because they evaluate different location criteria.

- **Centre of Gravity:** Identifies a theoretical demand-weighted geographical balance point.
- **Factor-Rating:** Favours Can Roqueta based on the weighted qualitative criteria.
- **Geographic Coverage:** Favours Els Bellots based on geographical coverage.
- **Cost Model:** Favours Cova Solera based on the lowest estimated annual equivalent cost.

The results are not contradictory. Each method answers a different decision question.

## 7.2 Controlling Decision Criterion

The project owner's priority is to compare transport-supply, transport-distribution and operating costs, including fixed, variable and establishment costs.

The Cost Model directly evaluates these priorities.

Consequently, the Cost Model is the controlling method for the final selection. The other methods provide supporting geographical and qualitative assessments.

## 7.3 Selected Location

**Final selected location: Industrial warehouse in Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain).**

This corresponds to candidate IA-R2.

An identifiable public property listing provides a reference for an industrial warehouse of approximately 1,500 m² in Cova Solera, advertised at approximately €6,000 per month.

The implied rental rate is:

$$
R=\frac{6000}{1500}
$$

$$
\boxed{R=€4.00/\text{m}^2/\text{month}}
$$

The annual rental cost is:

$$
C_{\text{annual}}=6000\times12
$$

$$
\boxed{C_{\text{annual}}=€72,000/year}
$$

The property listing provides indicative market evidence only. Availability, contractual conditions and technical suitability must be confirmed before an actual lease decision.

## 7.4 Selection Rationale

Cova Solera is selected because:

1. It achieves the lowest estimated annual equivalent cost.
2. It has the lowest indicative rental cost among the six candidates.
3. It has the lowest estimated distribution transport cost.
4. Its combined supply and distribution transport cost is competitive.
5. An identifiable warehouse listing supports the rental assumption.
6. Its selection directly reflects the project owner's cost-based priorities.

Although Cova Solera does not achieve the best geographical coverage or the highest Factor-Rating score, its economic performance makes it the preferred candidate under the project's stated priorities.

---

# 8\. Conclusion

This study compared six candidate industrial areas for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental.

The estimated demand is **7,545 kg/day**, equivalent to **2,753,925 kg/year**, based on the assumed generation rate of 3.0 kg per bed per day.

Four complementary location-analysis methods were applied:

- Centre of Gravity Method.
- Factor-Rating Method.
- Cost Model.
- Geographic Coverage Method.

The Centre of Gravity calculation identifies an approximate weighted geographical centre near Camí de Can Coniller, Terrassa.

The Factor-Rating Method identifies Can Roqueta as the highest-scoring qualitative candidate, with a score of 4.20/5.

The Geographic Coverage Method identifies Els Bellots as the strongest geographical candidate, with 87.9% baseline coverage of total hospital demand.

However, the project owner's primary priority is minimizing total annual costs, including supply transport, distribution transport, fixed operating, variable processing and establishment costs.

The Cost Model identifies Cova Solera as the lowest-cost candidate, with an estimated annual equivalent cost of €1,821,014.

The estimated annual saving compared with the second-ranked candidate, Can Jardí, is €15,707.

**Final decision: Cova Solera, Rubí, is the preferred location because it achieves the lowest estimated annual equivalent cost of €1,821,014 under the adopted project assumptions.**

The recommendation is conditional on the validation of actual property availability, rental conditions, operational capacity, utility requirements, regulatory compliance and transport arrangements.

---

# References

1. **Course lecture material.** _Location Strategies_. Methods applied include Centre of Gravity, Factor-Rating, Cost Models and geographical coverage assessment.
2. **Institut Cartogràfic i Geològic de Catalunya (ICGC).** Geocoding and reverse-geocoding services.\
   https://eines.icgc.cat/geocodificador/
3. **EPSG Geodetic Parameter Dataset.** EPSG:4326 — WGS84 coordinate reference system.
4. **GeographicLib.** Geodesic calculation conventions.\
   https://geographiclib.sourceforge.io/
5. **GPS-Coordinates.net.** Reverse-geocoding service used to identify the postal address associated with the calculated Centre of Gravity coordinates.\
   https://www.gps-coordinates.net/
6. **Idealista.** Public industrial warehouse listings in Polígono Cova Solera, Rubí. The comparative reference used in this study is an advertised warehouse of approximately 1,500 m² at approximately €6,000/month.\
   https://www.idealista.com/geo/alquiler-locales/avenida-cova-solera-rubi-barcelona/con-naves/
7. **AMB Naus i Solars.** Industrial property reference for Can Jardí, Rubí: approximately 1,001 m² at €4.80/m²/month.
8. **Masachs.** Industrial rental-market information for Sabadell, published 7 May 2026. Used as indicative market context for industrial rental assumptions.
9. **FROET.** Spanish articulated-vehicle operating-cost benchmark, report dated 17 September 2026, with costs updated July 2026. General-goods articulated vehicle reference: €1.424/km. Used as a comparative transport-cost proxy.
10. **UBICAT.** Sabadell, Can Roqueta II, industrial warehouse development, reference 1178.\
    https://www.ubicat.cat/es/sabadell/p\_i\_can\_roqueta\_ii/naves\_industriales/ref-1178
11. **Geographical and property comparison dataset.** Hospital coordinates, candidate industrial-area coordinates and indicative rental references compiled for this study.
