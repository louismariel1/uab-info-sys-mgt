# Centralized Hospital Laundry Location Study

## Location Analysis for a Centralized Hospital Laundry in Vallès Occidental, Catalonia

**Report status:** Final analytical report — location selection completed; final property validation pending\
**Study area:** Vallès Occidental, Barcelona, Catalonia, Spain\
**Selected industrial area:** Polígon Industrial de Cova Solera, Rubí

---

# Executive Summary

This study evaluates six candidate industrial areas for the establishment of a centralized hospital laundry facility serving seven healthcare facilities in Vallès Occidental, Catalonia.

The objective is to identify an industrial location that balances geographical proximity, accessibility, property suitability and, most importantly, the estimated total annual cost of operating the proposed facility.

The hospital network comprises 2,515 beds. Applying the assumed laundry-generation factor of 3.0 kg per bed per day results in an estimated processing demand of:

**7,545 kg/day, equivalent to 2,753,925 kg/year.**

Four complementary location-analysis approaches have been applied:

1. Centre of Gravity Method.
2. Factor-Rating Method.
3. Cost Model.
4. Graph-Based Location Analysis, using preliminary geographical distance and coverage proxies.

The main findings are summarized below.

| Method | Preferred result | Main finding |
| --- | --- | --- |
| Centre of Gravity | Theoretical point between Sabadell and Terrassa | Weighted geographical balance |
| Factor-Rating | IA-S2 – Can Roqueta | Highest qualitative suitability score: 4.20/5 |
| Cost Model | IA-R2 – Cova Solera | Lowest estimated annual equivalent cost |
| Graph-Based geographical proxies | IA-T – Els Bellots | Lowest weighted mean distance and highest baseline coverage |

The geographical calculations have been independently recalculated using consistent coordinate and distance conventions.

The principal verification findings are:

- The Centre of Gravity coordinates have been independently reproduced.
- Five of the six weighted mean distances agree with the original reported values at two decimal places.
- Can Roqueta requires a rounding correction from 6.74 km to 6.75 km.
- All 18 coverage percentages have been reproduced.
- The underlying covered-bed counts have also been verified.
- The Factor-Rating calculations have been checked against the stated criteria, weights and scores.

The Cost Model identifies IA-R2, Cova Solera in Rubí, as the lowest-cost candidate, with an estimated annual equivalent cost of €1,821,014.

The second-ranked candidate, Can Jardí, has an estimated annual equivalent cost of €1,836,721. The difference is €15,707 per year.

**The final recommendation is therefore to select an industrial warehouse in Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain), as the preferred location under the adopted economic assumptions.**

This is a location-selection recommendation rather than confirmation of a completed property acquisition or lease. Final property availability, technical suitability and regulatory compliance remain subject to validation.

---

# 1\. Introduction

## 1.1 Project Background

This study evaluates potential locations for a centralized hospital laundry facility serving seven healthcare facilities in Vallès Occidental, Catalonia.

The objective is to identify an industrial location that can support the collection, processing and distribution of hospital textiles while considering transportation requirements, operating costs, industrial suitability and access to the healthcare facilities.

Centralizing laundry operations may offer operational efficiencies through shared infrastructure, consolidated processing and coordinated logistics. However, the location of the facility is important because it influences transport distances, delivery times, property costs and the overall cost of the proposed operation.

## 1.2 Objective of the Location Study

The primary objective is to compare six candidate industrial areas using four location-analysis approaches:

- Centre of Gravity Method.
- Factor-Rating Method.
- Cost Model.
- Graph-Based Location Analysis.

Each method evaluates location from a different perspective. The results are therefore not expected to identify the same candidate.

The final decision is based on the priorities of the project owner, whose principal objective is to compare transport-supply, transport-distribution and operating costs, including fixed, variable and establishment costs.

Consequently, the Cost Model is treated as the controlling method for the final location recommendation.

## 1.3 Scope

The study focuses on the geographical and economic comparison of candidate industrial areas.

It uses available geographical information, indicative property rental references and explicit planning assumptions to estimate the relative costs of operating a centralized laundry facility.

The study is intended as an academic location-selection exercise. It is not a detailed engineering design, property inspection, regulatory approval or commercial feasibility assessment.

---

# 2\. Data Collection and Assumptions

## 2.1 Healthcare Facilities

The proposed laundry facility will serve seven healthcare facilities in Vallès Occidental. The number of beds is used as a proxy for estimating laundry demand.

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

Their percentage of total demand weight is:

$$
\frac{861+460+604}{2515}\times100 = 76.54\%
$$

Approximately 76.5% of the total demand weight is therefore concentrated in these three facilities.

This concentration is particularly relevant when evaluating geographical proximity and transportation requirements.

## 2.2 Laundry Demand Estimation

For the purpose of this study, an average laundry-generation rate of 3.0 kg per bed per day is assumed.

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

Assuming operations throughout the year:

$$
Q_{\text{annual}}=Q_{\text{daily}}\times365
$$

$$
Q_{\text{annual}}=7545\times365
$$

$$
\boxed{Q_{\text{annual}}=2,753,925\text{ kg/year}}
$$

The assumed generation rate is a planning parameter rather than measured consumption data from the individual hospitals. It provides a common demand estimate for comparing the candidate locations.

## 2.3 Geographical Data

Hospital and candidate-area coordinates are expressed in WGS84 (EPSG:4326).

Metric geographical calculations use ETRS89 / UTM Zone 31N (EPSG:25831).

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

| ID | Candidate Industrial Area | Municipality | Latitude | Longitude |
| --- | --- | --- | --- | --- |
| IA-T | Els Bellots / Santa Margarida / Can Parellada | Terrassa | 41.549829 | 2.041354 |
| IA-S1 | Sud-Oest / Sant Pau de Riu-sec | Sabadell | 41.513398 | 2.099462 |
| IA-S2 | Sabadell Parc Empresarial / Can Roqueta | Sabadell | 41.537660 | 2.134320 |
| IA-R1 | Can Sant Joan / Can Jardí | Rubí | 41.473458 | 2.020948 |
| IA-R2 | Central/southern industrial corridor / Cova Solera | Rubí | 41.480448 | 2.026145 |
| IA-C | Cerdanyola industrial corridor / Parc de l'Alba | Cerdanyola | 41.485460 | 2.107650 |

These coordinates represent candidate industrial areas for comparative analysis. They are not necessarily the precise coordinates of individual buildings.

## 2.4 General Modelling Assumptions

| Parameter | Adopted assumption |
| --- | --- |
| Number of healthcare facilities | 7 |
| Total demand weight | 2,515 beds |
| Laundry-generation factor | 3.0 kg/bed/day |
| Estimated daily demand | 7,545 kg/day |
| Estimated annual demand | 2,753,925 kg/year |
| Candidate industrial areas | 6 |
| Master coordinate system | WGS84 (EPSG:4326) |
| Projected coordinate system | ETRS89 / UTM 31N (EPSG:25831) |
| Reference warehouse area | 1,500 m² |
| Factor-Rating scale | 1–5 |
| Coverage baseline radius | 7.5 km |
| Road-distance conversion factor | 1.30 |
| Transport cost benchmark | €1.424/km |
| Annual operating days | 365 |

The common reference area of 1,500 m² is a modelling assumption applied to all candidates to ensure comparability. The Cova Solera property reference also provides an advertised industrial warehouse of approximately 1,500 m².

## 2.5 Data Limitations

The geographical analysis uses representative industrial-area coordinates rather than confirmed building entrances.

The bed figures are used as relative demand weights and do not represent measured laundry consumption.

Property rental values are indicative asking rents, not confirmed contractual rents.

The transport estimates use converted geographical distances and assumed operating frequencies rather than validated road-network routes or transport-provider quotations.

These limitations are maintained throughout the analysis.

---

# 3\. Centre of Gravity Method

## 3.1 Methodology

The Centre of Gravity Method identifies a theoretical location based on the geographical coordinates and demand weights of the healthcare facilities.

The weighted coordinates are calculated using:

$$
X^*=\frac{\sum_{i=1}^{n}W_iX_i}{\sum_{i=1}^{n}W_i}
$$

$$
Y^*=\frac{\sum_{i=1}^{n}W_iY_i}{\sum_{i=1}^{n}W_i}
$$

Where:

- $X_i$ = Projected easting of healthcare facility $i$.
- $Y_i$ = Projected northing of healthcare facility $i$.
- $W_i$ = Number of beds at facility $i$.
- $n$ = Number of healthcare facilities.

The calculation uses projected metric coordinates rather than directly averaging latitude and longitude degrees.

## 3.2 Coordinate Reference System

The hospital coordinates were converted from WGS84 to:

**ETRS89 / UTM Zone 31N (EPSG:25831).**

The projected coordinate system is suitable for the study area and allows the weighted geographical calculations to be performed in metres.

The calculation uses the GRS80 ellipsoid and the EPSG:25831 projection parameters.

## 3.3 Calculation

The total weighting factor is:

$$
\sum_{i=1}^{7}W_i=2515
$$

The independently recalculated weighted projected coordinates are:

$$
E^*=
\frac{\sum W_iE_i}{2515}
$$

$$
\boxed{E^*=422010.6094\text{ m}}
$$

Similarly:

$$
N^*=
\frac{\sum W_iN_i}{2515}
$$

$$
\boxed{N^*=4599632.8017\text{ m}}
$$

The inverse projection converts these coordinates back to geographical coordinates.

The resulting coordinates are:

$$
\text{Latitude}=41.5445552556^\circ
$$

$$
\text{Longitude}=2.0649425975^\circ
$$

Therefore:

$$
\boxed{41.544555^\circ\text{ N},\quad2.064943^\circ\text{ E}}
$$

Using reverse geocoding, the nearest identifiable address is: **Camí de Can Coniller, 08220 Terrassa, Barcelona, Spain**. The Centre of Gravity is therefore useful for preliminary geographical screening but does not determine the final industrial property.

---

# 4\. Factor-Rating Method

## 4.1 Methodology

The Factor-Rating Method evaluates candidate locations using qualitative and operational criteria.

Each criterion receives a weight according to its relative importance, and each candidate receives a score from 1 to 5.

The weighted score is:

$$
S_j=\sum_{k=1}^{m}w_kr_{jk}
$$

Where:

- $S_j$ = Weighted score of candidate $j$.
- $w_k$ = Weight assigned to criterion $k$.
- $r_{jk}$ = Score of candidate $j$ for criterion $k$.
- $m$ = Number of evaluation criteria.

The maximum possible score is 5.

## 4.2 Evaluation Criteria and Weights

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

Scores are assigned on a scale from 1 (least favourable) to 5 (most favourable).

| Candidate | Proximity | Roads | Premises | Industrial | Utilities | Environment |
| --- | --- | --- | --- | --- | --- | --- |
| IA-T | 5 | 4 | 3 | 5 | 3 | 3 |
| IA-S1 | 4 | 4 | 2 | 5 | 3 | 3 |
| IA-S2 | 3 | 5 | 5 | 5 | 4 | 3 |
| IA-R1 | 2 | 4 | 4 | 5 | 4 | 3 |
| IA-R2 | 2 | 4 | 4 | 5 | 4 | 3 |
| IA-C | 2 | 5 | 2 | 3 | 4 | 3 |

The scores represent a comparative assessment based on the available geographical and industrial evidence. They are indicative rather than the result of a formal site inspection or verified technical audit.

## 4.4 Weighted Score Calculations

The calculations use the stated criterion weights.

For IA-S2 – Can Roqueta:

$$
S_{\text{IA-S2}}=
0.25(3)+0.20(5)+0.20(5)
$$

$$
+0.15(5)+0.10(4)+0.10(3)
$$

$$
=0.75+1.00+1.00+0.75+0.40+0.30
$$

$$
\boxed{S_{\text{IA-S2}}=4.20/5}
$$

For IA-T – Els Bellots:

$$
S_{\text{IA-T}}=
0.25(5)+0.20(4)+0.20(3)
$$

$$
+0.15(5)+0.10(3)+0.10(3)
$$

$$
=1.25+0.80+0.60+0.75+0.30+0.30
$$

$$
\boxed{S_{\text{IA-T}}=4.00/5}
$$

The remaining candidates are calculated using the same method.

| Candidate | Weighted Score | Rank |
| --- | --- | --- |
| **IA-S2 – Can Roqueta** | **4.20** | **1** |
| IA-T – Els Bellots | 4.00 | 2 |
| IA-S1 – Sant Pau de Riu-sec | 3.55 | 3 |
| IA-R1 – Can Jardí | 3.55 | 3 |
| IA-R2 – Cova Solera | 3.55 | 3 |
| IA-C – Cerdanyola | 3.05 | 6 |

## 4.5 Interpretation

The Factor-Rating Method identifies IA-S2, Sabadell Parc Empresarial / Can Roqueta, as the highest-scoring candidate.

Its result is primarily supported by its favourable assessment of road accessibility, evidence of suitable industrial premises and industrial compatibility.

IA-T, in Terrassa, obtains the second-highest score, reflecting its geographical proximity to the healthcare facilities.

The calculation confirms the reported score of 4.20/5 for Can Roqueta.

The Factor-Rating Method is a qualitative comparison. Its outcome depends on the selected criteria, weights and assigned scores. It is therefore useful as a complementary assessment but does not replace the quantitative cost comparison required for the final decision.

---

# 5\. Cost Model

## 5.1 Methodology

The Cost Model compares the estimated annual costs associated with operating the centralized laundry at each candidate location.

The model considers:

- Property rental costs.
- Transport-supply costs.
- Transport-distribution costs.
- Fixed operating costs.
- Variable processing costs.
- Establishment costs.

The objective is to identify the candidate with the lowest estimated annual equivalent cost under the adopted assumptions.

## 5.2 Transport Cost Estimation

The transport calculation uses geographical distances converted into estimated road distances through a conversion factor.

$$
d_{\text{road}}=d_{\text{map}}\times f
$$

The estimated transport cost is calculated as:

$$
C_{\text{transport}}=
d_{\text{map}}\times f\times q\times c\times n
$$

Where:

- $d_{\text{map}}$ = Geographical distance.
- $f$ = Road-distance conversion factor.
- $q$ = Applicable transport quantity or number of journeys.
- $c$ = Transport cost per kilometre.
- $n$ = Number of operating periods.

The adopted assumptions are:

| Parameter | Assumption |
| --- | --- |
| Road-distance conversion factor | 1.30 |
| Transport cost benchmark | €1.424/km |
| Distribution tours | 2 complete multi-stop tours/day |
| Operating days | 365 days/year |
| Supply journeys | 2 round trips/week |
| Supply operating weeks | 52 weeks/year |

The transport benchmark is based on an indicative Spanish articulated-vehicle operating-cost reference. It is used as a comparative cost proxy rather than as a quotation from a laundry transport provider.

### Distribution transport

The model estimates two complete multi-stop tours per day:

1. Clean-linen delivery to the seven healthcare facilities.
2. Soiled-linen collection from the seven healthcare facilities.

The tours visit all seven facilities, using a nearest-neighbour sequence based on representative geographical coordinates.

### Supply transport

The model assumes two weekly round trips to a representative logistics supplier hub in the Barcelona area.

The resulting transport costs are comparative estimates based on converted geographical distances and assumed transport frequencies. They are not based on verified vehicle routes or transport-provider quotations.

## 5.3 Annual Transport Cost Estimates

The annual transport costs are divided into two components:

- Distribution cost: Covers the transportation of clean and soiled linen between the centralized laundry and the seven healthcare facilities.
- Supply cost: Covers the transportation of supplies from the external supplier hub to the centralized laundry.

The combined transport costs for all six candidates are shown below.

| Candidate | Distribution Cost/year | Supply Cost/year | Combined Cost/year |
| --- | --- | --- | --- |
| IA-T – Els Bellots | €43,544 | €9,213 | €52,757 |
| IA-S1 – Sant Pau de Riu-sec | €43,854 | €7,161 | €51,015 |
| IA-S2 – Can Roqueta | €47,740 | €8,028 | €55,768 |
| IA-R1 – Can Jardí | €42,838 | €6,698 | €49,536 |
| IA-R2 – Cova Solera | €41,392 | €6,837 | €48,229 |
| IA-C – Cerdanyola | €49,670 | €5,940 | €55,610 |

The combined transport costs are:

$$
C_{\text{transport}}=
C_{\text{distribution}}+
C_{\text{supply}}
$$

For Cova Solera:

$$
C_{\text{transport,IA-R2}}=
41,392+6,837
$$

$$
\boxed{C_{\text{transport,IA-R2}}=€48,229/year}
$$

The same calculation is applied to all candidates.

## 5.4 Property Rental Costs

A common reference warehouse area of 1,500 m² is used to compare rental costs.

The annual rental cost is calculated as:

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

| Candidate | Indicative Rent €/m²/month | Annual Rent |
| --- | --- | --- |
| IA-R2 – Cova Solera | €4.00 | €72,000 |
| IA-R1 – Can Jardí | €4.80 | €86,400 |
| IA-S2 – Can Roqueta | €5.00 | €90,000 |
| IA-S1 – Sant Pau de Riu-sec | €5.50 | €99,000 |
| IA-C – Cerdanyola | €5.45 | €98,100 |
| IA-T – Els Bellots | €5.95 | €107,100 |

The rental values are indicative estimates based on available industrial property references and market information.

The common 1,500 m² area provides a normalized comparison. It does not establish that all candidates have a suitable property of that size.

## 5.5 Fixed, Variable and Establishment Costs

The operating-cost assumptions are:

| Cost Component | Calculation | Annual Cost |
| --- | --- | --- |
| Fixed operating costs | Planning estimate | €1,000,000 |
| Variable processing costs | €0.20 × 2,753,925 kg | €550,785 |
| Establishment costs | €1,500,000 over 10 years | €150,000 |
| **Total common annual cost** |  | **€1,700,785** |

### Fixed operating costs

$$
C_{\text{fixed}}=€1,000,000/year
$$

### Variable processing costs

The assumed variable processing cost is €0.20 per kilogram.

$$
C_{\text{variable}}=
2,753,925\times0.20
$$

$$
\boxed{C_{\text{variable}}=€550,785/year}
$$

### Annualised establishment costs

The initial establishment investment is assumed to be €1,500,000, annualised over ten years.

$$
C_{\text{establishment,annual}}=
\frac{1,500,000}{10}
$$

$$
\boxed{C_{\text{establishment,annual}}=€150,000}
$$

### Total common annual costs

$$
C_{\text{common}}=
1,000,000+550,785+150,000
$$

$$
\boxed{C_{\text{common}}=€1,700,785/year}
$$

These operating and establishment values are planning assumptions for the academic comparison, not supplier quotations or a detailed financial feasibility estimate.

Since fixed operating, variable processing and annualised establishment costs are assumed to be identical across all candidate locations, they do not affect the relative ranking.

The differences in estimated total cost are therefore driven by property rental and transportation costs.

## 5.6 Total Annual Equivalent Cost

The total annual equivalent cost is calculated as:

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
C_{\text{total,IA-R2}}=
72,000+6,837+41,392+1,000,000
$$

$$
+550,785+150,000
$$

$$
\boxed{C_{\text{total,IA-R2}}=€1,821,014/year}
$$

The full comparison is:

| Rank | Candidate | Rent | Supply + Distribution | Common Operating + Establishment | Annual Total |
| --- | --- | --- | --- | --- | --- |
| **1** | **IA-R2 – Cova Solera** | **€72,000** | **€48,229** | **€1,700,785** | **€1,821,014** |
| 2 | IA-R1 – Can Jardí | €86,400 | €49,536 | €1,700,785 | €1,836,721 |
| 3 | IA-S2 – Can Roqueta | €90,000 | €55,768 | €1,700,785 | €1,846,553 |
| 4 | IA-S1 – Sant Pau de Riu-sec | €99,000 | €51,015 | €1,700,785 | €1,850,800 |
| 5 | IA-C – Cerdanyola | €98,100 | €55,610 | €1,700,785 | €1,854,495 |
| 6 | IA-T – Els Bellots | €107,100 | €52,757 | €1,700,785 | €1,860,642 |

This indicates that Cova Solera is the lowest-cost candidate under the adopted assumptions, but its economic advantage is relatively modest.


# 6\. Geographical Distance and Coverage Models

Two complementary geographical models are used to evaluate the proximity of the six candidate industrial areas to the seven healthcare facilities:

1. Discrete Weighted Simple Median Model.
2. Geographical Coverage Model.

Both models use the seven hospital service points, weighted by their respective bed capacities, and the six candidate industrial areas.

The purpose of this section is to evaluate geographical proximity and potential service coverage independently of the economic comparison presented in Section 5.

**Methodological qualification:** The numerical analysis uses geodesic straight-line distances calculated from representative hospital and industrial-area coordinates. These distances provide a preliminary geographical assessment but do not represent actual road-network distances or vehicle travel times. The results should therefore be interpreted as geographical screening indicators rather than definitive transport optimization outcomes.

## 6.1 Discrete Weighted Simple Median Model

### 6.1.1 Methodology

The Discrete Weighted Simple Median Model identifies which of the six predetermined candidate locations minimizes the total demand-weighted geographical distance to the healthcare facilities.

This is a discrete weighted 1-median comparison because the analysis evaluates six predetermined candidate locations rather than searching for an unrestricted optimal point.

For candidate location $j$, the total weighted distance is:

$$
D_j=\sum_{i=1}^{n}W_i d_{ij}
$$

Where:

- $D_j$ = Total weighted distance for candidate $j$.
- $W_i$ = Demand weight of hospital $i$, represented by its number of beds.
- $d_{ij}$ = Geographical distance between hospital $i$ and candidate $j$.
- $n$ = Number of healthcare facilities (7).

For easier interpretation, the results are expressed as weighted mean distance:

$$
\bar d_j=
\frac{\sum_{i=1}^{n}W_i d_{ij}}
{\sum_{i=1}^{n}W_i}
$$

The total demand weight is:

$$
\sum_{i=1}^{7}W_i=2,515
$$

The calculation uses geodesic straight-line distances derived from the geographical coordinates of the hospitals and candidate industrial areas.

### 6.1.2 Results

The independently recalculated weighted mean distances are presented below.

| Rank | Candidate | Weighted Mean Distance |
| --- | --- | --- |
| 1 | **IA-T — Els Bellots** | **4.48 km** |
| 2 | IA-S1 — Sant Pau de Riu-sec | 6.22 km |
| 3 | IA-S2 — Can Roqueta | 6.75 km |
| 4 | IA-C — Cerdanyola Industrial Corridor / Parc de l'Alba | 8.46 km |
| 5 | IA-R2 — Cova Solera | 8.61 km |
| 6 | IA-R1 — Can Jardí | 9.37 km |

**Data correction:** Can Roqueta's independently recalculated weighted mean distance is 6.75 km, correcting the previously reported value of 6.74 km.

### 6.1.3 Result and Interpretation

The best candidate under the weighted geographical distance comparison is:

$$
\boxed{\text{IA-T — Els Bellots}}
$$

Els Bellots achieves the lowest weighted mean straight-line distance to the seven healthcare facilities, at 4.48 km.

Its relatively central geographical position between the main hospital demand concentrations in Terrassa and Sabadell results in the lowest demand-weighted geographical distance among the six candidate industrial areas.

This makes Els Bellots the strongest candidate under the Discrete Weighted Simple Median Model.

However, geographical proximity does not necessarily translate directly into the shortest operational transport routes. Actual road configurations, access restrictions and traffic conditions may influence transport distances and travel times.

## 6.2 Geographical Coverage Model

### 6.2.1 Methodology

The Geographical Coverage Model evaluates the proportion of hospital demand located within a specified geographical distance of each candidate laundry facility.

Unlike the Simple Median Model, which minimizes overall weighted distance, the Coverage Model measures how much demand is located within a predefined distance threshold.

For candidate $j$ and coverage radius $R$:

$$
C_j(R)=\sum_{i=1}^{n}W_i I(d_{ij}\leq R)
$$

Where:

- $C_j(R)$ = Total covered demand for candidate $j$.
- $W_i$ = Demand weight of hospital $i$, represented by its number of beds.
- $d_{ij}$ = Geographical distance between hospital $i$ and candidate $j$.
- $R$ = Selected coverage radius.
- $I(\cdot)$ = Indicator function, equal to 1 when the hospital is within the coverage radius and 0 otherwise.

The coverage percentage is calculated as:

$$
Coverage_j(R)=
\frac{C_j(R)}{2,515}\times100
$$

The baseline coverage radius adopted for the study is:

$$
\boxed{R=7.5\text{ km}}
$$

This distance is a project modelling assumption used to compare the candidate locations. It is not a statutory requirement or an established operational service standard.

### 6.2.2 Baseline Coverage Results

The baseline coverage results using the 7.5 km radius are:

| Rank | Candidate | Covered Beds | Coverage |
| --- | --- | --- | --- |
| 1 | **IA-T — Els Bellots** | **2,211** | **87.9%** |
| 2 | IA-S1 — Sant Pau de Riu-sec | 1,834 | 72.9% |
| 3 | IA-S2 — Can Roqueta | 1,530 | 60.8% |
| 4 | IA-C — Cerdanyola Industrial Corridor / Parc de l'Alba | 513 | 20.4% |
| 5 | IA-R1 — Can Jardí | 442 | 17.6% |
| 5 | IA-R2 — Cova Solera | 442 | 17.6% |
|  | **Total hospital demand** | **2,515** | **100%** |

For Els Bellots, the coverage percentage is:

$$
Coverage_{\text{IA-T}}=
\frac{2,211}{2,515}\times100
$$

$$
\boxed{Coverage_{\text{IA-T}}=87.9\%}
$$

The same calculation is applied to all six candidates.

### 6.2.3 Sensitivity to Coverage Radius

To examine how geographical coverage changes with the selected distance threshold, the calculation is repeated using three alternative radii:

- 5 km: More restrictive geographical coverage.
- 7.5 km: Baseline coverage assumption.
- 10 km: Extended geographical coverage.

The resulting coverage percentages are:

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| IA-T — Els Bellots | 45.4% | 87.9% | 100% |
| IA-S1 — Sant Pau de Riu-sec | 42.5% | 72.9% | 100% |
| IA-S2 — Can Roqueta | 37.1% | 60.8% | 60.8% |
| IA-R1 — Can Jardí | 12.1% | 17.6% | 38.9% |
| IA-R2 — Cova Solera | 17.6% | 17.6% | 65.8% |
| IA-C — Cerdanyola Industrial Corridor / Parc de l'Alba | 5.5% | 20.4% | 72.9% |

The results show that geographical coverage increases or remains unchanged as the radius increases.

Els Bellots and Sant Pau de Riu-sec achieve complete coverage at 10 km, while Can Roqueta remains at 60.8%.

### 6.2.4 Result and Interpretation

Els Bellots achieves the highest baseline geographical coverage:

$$
\boxed{87.9\%\text{ of weighted hospital demand}}
$$

It also achieves 100% coverage at the extended 10 km radius.

The sensitivity analysis demonstrates that the relative performance of some candidates changes considerably as the coverage radius increases.

For example, Cova Solera increases its coverage from 17.6% at 7.5 km to 65.8% at 10 km.

This demonstrates the importance of the selected coverage radius when interpreting geographical proximity.

Overall, Els Bellots provides the strongest geographical coverage among the six candidates under the tested straight-line distance assumptions.

## 6.3 Overall Geographical Results and Relevance to the Final Location Decision

Both geographical models identify the same preferred candidate:

$$
\boxed{\text{IA-T — Els Bellots}}
$$

The main findings are summarized below:

| Evaluation Method | Preferred Candidate | Main Result |
| --- | --- | --- |
| Discrete Weighted Simple Median Model | IA-T — Els Bellots | Lowest weighted mean distance: 4.48 km |
| Geographical Coverage Model | IA-T — Els Bellots | Highest baseline coverage: 87.9% |
| Extended geographical coverage (10 km) | IA-T and IA-S1 | Both achieve 100% coverage |

The agreement between the two models provides consistent geographical evidence in favour of Els Bellots. Els Bellots is the strongest candidate geographically because it minimizes weighted mean distance and maximizes baseline geographical coverage. However, the project owner's principal decision priority is minimizing the estimated total annual operating cost. Consequently, the Cost Model remains the controlling method for the final location recommendation.

**Accordingly, the geographical analysis identifies Els Bellots as the strongest candidate in terms of proximity and geographical coverage, while Cova Solera remains the preferred location under the project's economic decision criteria.**



# 7. Summary Results and Final Selection

## 7.1 Summary of the Four Methods and their Significance

The four approaches produce different preferred locations because they evaluate different aspects of the location decision.

| Method | Preferred Candidate | Main Objective | Key Result |
| --- | --- | --- | --- |
| Centre of Gravity | Camí de Can Coniller, 08220 Terrassa, Barcelona | Weighted geographical centrality | Theoretical demand-weighted geographical balance point |
| Factor-Rating | IA-S2 – Can Roqueta | Weighted qualitative suitability | Highest weighted score: 4.20/5 |
| Cost Model | IA-R2 – Cova Solera | Lowest estimated annual equivalent cost | €1,821,014/year |
| Simple Median Model | IA-T – Els Bellots | Minimum weighted geographical distance | Lowest weighted mean distance: 4.48 km |
| Coverage Model | IA-T – Els Bellots | Geographical demand coverage | Highest baseline coverage: 87.9% within 7.5 km |

The results are not contradictory, as each method evaluates a different aspect of the location decision:

- **Centre of Gravity:** Identifies the theoretical geographical balance point of the seven healthcare facilities.
- **Factor-Rating:** Favours Can Roqueta, with the highest qualitative suitability score of **4.20/5**.
- **Simple Median Model:** Favours Els Bellots, with the lowest weighted mean geographical distance of **4.48 km**.
- **Coverage Model:** Favours Els Bellots, covering **87.9%** of weighted hospital demand within 7.5 km and 100% within 10 km.
- **Cost Model:** Favours Cova Solera, with the lowest estimated annual equivalent cost of **€1,821,014**, saving €15,707 annually compared with Can Jardí.

The geographical models support Els Bellots in terms of proximity and coverage, although they use straight-line distances rather than validated road-network routes. The Factor-Rating Model provides complementary qualitative evidence for Can Roqueta.

**The Cost Model is the controlling method for the final selection**, as the project owner's primary objective is to minimize total annual costs, including transport-supply, transport-distribution, fixed, variable and establishment costs.

Therefore, **Cova Solera, Rubí (IA-R2), remains the preferred location** under the project's adopted decision priorities.

## 7.2 Cost Model Selection and Assumptions

The Cost Model is of strategic significance for the business owner. It identifies IA-R2, Cova Solera in Rubí, as the candidate with the lowest estimated annual equivalent cost.

Its principal advantage is the comparatively low estimated rental cost, combined with relatively low distribution transport costs.

The result is based on the adopted assumptions.

In particular:

- Transport distances have not been validated against actual road-network routes.
- The road-distance conversion factor is a generalized assumption.
- Transport costs are not based on provider quotations.
- Rental prices are indicative rather than confirmed contractual values.
- Fixed and variable operating costs are common planning assumptions.
- Establishment costs are annualised without a detailed financing or depreciation model.

---

## 7.3 Selected Location and Rationale

The selected location is: 
**Industrial warehouse in Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain).** This corresponds to candidate IA-R2.

An identifiable public property listing provides a reference for an industrial warehouse of approximately 1,500 m² in the Cova Solera industrial area, advertised at approximately €6,000 per month.

The equivalent rental rate is:

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
\boxed{C_{\text{annual}}=€72,000}
$$

This provides a real property-market reference consistent with the rental assumption used in the Cost Model.

The listing demonstrates that a property of the required approximate scale has been marketed in the selected industrial area.

## Rationale for Selection

Cova Solera is selected because:

1. It achieves the lowest estimated annual equivalent cost.
2. Its indicative rental rate is the lowest among the six candidates.
3. Its estimated distribution transport cost is the lowest among the candidates.
4. Its combined supply and distribution transport cost remains competitive.
5. An identifiable industrial warehouse property reference of approximately 1,500 m² supports the rental assumption.
6. Its selection is consistent with the project's priority of minimizing estimated total operating cost.

# 8\. Conclusion

This study has evaluated six candidate industrial areas for a centralized hospital laundry facility serving seven healthcare facilities in Vallès Occidental.

The healthcare network comprises 2,515 beds and produces an estimated laundry demand of 7,545 kg/day, equivalent to 2,753,925 kg/year under the adopted assumption of 3.0 kg per bed per day.

Four complementary location-analysis approaches were applied:

1. Centre of Gravity Method.
2. Factor-Rating Method.
3. Cost Model.
4. Graph-Based Location Analysis using preliminary geographical distance and coverage proxies.

**Final decision: Cova Solera, Rubí, is the preferred candidate because it achieves the lowest estimated total annual equivalent cost under the adopted project assumptions.**

---

# References and Evidence Record

The following public sources were used or identified during the project research. Property listings and market information should be rechecked because asking prices and availability can change.

1. Institut Cartogràfic i Geològic de Catalunya (ICGC), geocoding and reverse-geocoding services: https://eines.icgc.cat/geocodificador/
2. Ajuntament de Sabadell / URBACT, _Integrated Action Plan — Green Transition in Industry, City of Sabadell_, 2026.
3. Invertica, industrial/logistics warehouse listing in Can Roqueta, Sabadell, reference BCN-IND-00247: https://www.invertica.es/index.php/inmuebles/nave-industrial-logistica-en-sabadell-bcn-ind-00247
4. UBICAT, _Sabadell: Proyecto de 4 naves, tipo B, con todos los servicios_, reference 1178: https://www.ubicat.cat/es/sabadell/p\_i\_can\_roqueta\_ii/naves\_industriales/ref-1178
5. Public industrial property listings for Els Bellots, Can Jardí, Cova Solera and Parc Tecnològic, as recorded in the project's comparative rental dataset.
6. Public geographical mapping references used to establish hospital and candidate-area coordinates, as recorded in the project's geographical dataset.
7. EPSG Geodetic Parameter Dataset, EPSG:25831 — ETRS89 / UTM Zone 31N.
8. GeographicLib / WGS84 geodesic calculation conventions, used as the reference methodology for the independent distance recalculation.

---
