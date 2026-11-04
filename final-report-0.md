# Centralized Hospital Laundry Location Study

## Location Analysis for a Centralized Hospital Laundry in Vallès Occidental, Catalonia

**Group Members:** Meabh Geary - 1829913, Thea Isberg - 1822816, Annemyn Ooschoeu – 1829120, Louis-Marie Loe - 1833548\
**Report status:** Final analytical location completed — location selection completed; property for the location selected\
**Study area:** Vallès Occidental, Barcelona, Catalonia, Spain\
**Selected location:** **Industrial warehouse in Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain)** 

---

# Executive Summary

This study evaluates six candidate industrial areas for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental.

The hospital network comprises **2,515 beds**. Using an assumed laundry-generation factor of 3.0 kg per bed per day, the estimated processing demand is:

- **Daily demand:** 7,545 kg/day.
- **Annual demand:** 2,753,925 kg/year.

Four complementary location-analysis methods are applied:

1. Centre of Gravity Method.
2. Factor-Rating Method.
3. Cost Model.
4. Geographic Coverage Method.

Each method evaluates a different aspect of the location decision.

| Method              | Preferred result                | Main finding                                                |
| ------------------- | ------------------------------- | ----------------------------------------------------------- |
| Centre of Gravity   |  Camí de Can Coniller, 08220 Terrassa | Demand-weighted geographical balance                        |
| Factor-Rating       | IA-S2 — Can Roqueta             | Highest qualitative score: 4.20/5                           |
| Cost Model          | IA-R2 — Cova Solera             | Lowest estimated annual equivalent cost                     |
| Geographic Coverage | IA-T — Els Bellots              | Lowest weighted mean distance and highest baseline coverage |

The project owner's principal priority is to compare transport-supply, transport-distribution and operating costs, including fixed, variable and establishment costs. Therefore, **the Cost Model is the controlling method for the final selection**.

The Cost Model identifies Cova Solera, Rubí, as the lowest-cost candidate:

**Estimated annual equivalent cost: €1,821,014.**

This is €15,707 lower per year than the second-ranked candidate, Can Jardí.

**Final recommendation:** Select an industrial warehouse in **Polígon Industrial de Cova Solera, Rubí (Barcelona, Spain)** as the preferred location under the adopted assumptions.

A publicly available property listing provides indicative evidence of a warehouse of approximately 1,500 m² in Cova Solera, with an asking rent of €6,000/month.

---

# 1. Introduction

## 1.1 Project Background

This study evaluates potential locations for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental, Catalonia.

The proposed facility will collect soiled textiles, process them centrally and distribute clean textiles to the healthcare facilities.

Location affects transport requirements, delivery distances, property costs and operating expenditure. The study therefore compares candidate industrial areas using geographical, qualitative and economic criteria.

## 1.2 Objective of the Location Study

The objective is to identify the most appropriate industrial location by applying four complementary methods:

- Centre of Gravity Method.
- Factor-Rating Method.
- Cost Model.
- Geographic Coverage Method.

The methods are not expected to produce the same result because they address different decision criteria.

The project owner's stated priority is:

> Compare transport-supply, transport-distribution and operating costs; include fixed, variable and establishment costs.

Accordingly, the Cost Model determines the final recommendation.

# 1.3 Study Methodology and Scope
The study is geographically limited to Vallès Occidental, Catalonia, which defines the regional scope for both the healthcare demand network and the potential location of the centralized laundry facility. 


Seven healthcare facilities within this region were identified as demand points, and six existing industrial areas in the region were shortlisted as potential locations. 

The shortlist was based on their geographical position, their identification as established industrial areas or corridors, and the availability of relevant public geographical and industrial information. 


It provides a manageable set of plausible alternatives for comparative analysis, without implying formal technical or regulatory validation of individual properties.

---

# 2. Data Collection and Assumptions

## 2.1 Healthcare Facilities

The proposed laundry will serve seven healthcare facilities.

| ID   | Hospital / Service Point                    | Municipality          | Beds      |
| ---- | ------------------------------------------- | --------------------- | --------- |
| H01  | Hospital de Sabadell – Parc Taulí           | Sabadell              | 861       |
| H02  | Hospital de Terrassa                        | Terrassa              | 460       |
| H03  | Mútua de Terrassa + Àptima Centre Clínic    | Terrassa              | 604       |
| H04  | Hospital Universitari General de Catalunya  | Sant Cugat del Vallès | 304       |
| H05  | Centre de Prevenció i Rehabilitació Asepeyo | Sant Cugat del Vallès | 138       |
| H06  | Hospital de Sant Llàtzer                    | Terrassa              | 77        |
| H07  | Hospital Quirónsalud del Vallès             | Sabadell              | 71        |
| <br> | **Total**                                   | <br>                  | **2,515** |

The three largest service points (H01, H02 and H03) account for 1,925 beds.

Their share of total demand weight is:

$$\
\frac{861+460+604}{2515}\times100\
\=76.54%\
$$

Approximately 76.5% of the demand weight is concentrated in these three facilities.

## 2.2 Laundry Demand Estimation

An average laundry-generation rate of 3.0 kg per bed per day is assumed.

The estimated daily demand is:

$$\
Q\_{\text{daily}}=N\times L\
$$

Where:

- $N$ = Total number of beds.
- $L$ = Laundry-generation factor.

Substituting the project values:

$$\
Q\_{\text{daily}}=2515\times3.0\
$$

$$\
\boxed{Q\_{\text{daily}}=7,545\text{ kg/day}}\
$$

Assuming 365 operating days per year:

$$\
Q\_{\text{annual}}=Q\_{\text{daily}}\times365\
$$

$$\
Q\_{\text{annual}}=7545\times365\
$$

$$\
\boxed{Q\_{\text{annual}}=2,753,925\text{ kg/year}}\
$$

The 3.0 kg/bed/day factor is a planning assumption, not measured consumption data from the individual hospitals.

## 2.3 Geographical Data

Hospital and candidate-area coordinates are expressed in WGS84 (EPSG:4326).

Metric geographical calculations use ETRS89 / UTM Zone 31N (EPSG:25831).

### 2.3.1 Hospital Coordinates

| ID  | Latitude | Longitude |
| --- | -------- | --------- |
| H01 | 41.55719 | 2.10989   |
| H02 | 41.55679 | 2.05277   |
| H03 | 41.56383 | 2.01718   |
| H04 | 41.47491 | 2.04463   |
| H05 | 41.49010 | 2.07843   |
| H06 | 41.56261 | 2.01721   |
| H07 | 41.53233 | 2.11760   |

### 2.3.2 Candidate Industrial Areas

| ID    | Candidate Industrial Area                          | Municipality |
| ----- | -------------------------------------------------- | ------------ |
| IA-T  | Els Bellots / Santa Margarida / Can Parellada      | Terrassa     |
| IA-S1 | Sud-Oest / Sant Pau de Riu-sec                     | Sabadell     |
| IA-S2 | Sabadell Parc Empresarial / Can Roqueta            | Sabadell     |
| IA-R1 | Can Sant Joan / Can Jardí                          | Rubí         |
| IA-R2 | Central/southern industrial corridor / Cova Solera | Rubí         |
| IA-C  | Cerdanyola industrial corridor / Parc de l'Alba    | Cerdanyola   |

The coordinates represent candidate industrial areas rather than precise building entrances. 
The six candidate areas were identified within the defined regional study scope. 
Each candidate is evaluated against the complete network of seven healthcare facilities, irrespective of the municipality in which the candidate area or healthcare facility is located.

## 2.4 General Modelling Assumptions

| Parameter                       | Adopted assumption |
| ------------------------------- | ------------------ |
| Healthcare facilities           | 7                  |
| Total demand weight             | 2,515 beds         |
| Laundry-generation factor       | 3.0 kg/bed/day     |
| Daily demand                    | 7,545 kg/day       |
| Annual demand                   | 2,753,925 kg/year  |
| Candidate industrial areas      | 6                  |
| Reference warehouse area        | 1,500 m²           |
| Factor-Rating scale             | 1–5                |
| Baseline coverage radius        | 7.5 km             |
| Road-distance conversion factor | 1.30               |
| Transport cost benchmark        | €1.424/km          |
| Annual operating days           | 365                |

The common reference area of 1,500 m² is used to normalize rental costs across all candidates.

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

# 3. Centre of Gravity Method

## 3.1 Methodology

The Centre of Gravity Method identifies a theoretical geographical location using the coordinates and demand weights of the healthcare facilities.

The weighted coordinates are:

$$\
X^\*=\frac{\sum\_{i=1}^{n}W_iX_i}{\sum\_{i=1}^{n}W_i}\
$$

$$\
Y^\*=\frac{\sum\_{i=1}^{n}W_iY_i}{\sum\_{i=1}^{n}W_i}\
$$

Where:

- $X_i,Y_i$ = Projected coordinates of hospital $i$.
- $W_i$ = Number of beds at hospital $i$.
- $n$ = Number of healthcare facilities.

The calculations use projected metric coordinates rather than directly averaging latitude and longitude.

## 3.2 Coordinate Reference System

Hospital coordinates were converted to **ETRS89 / UTM Zone 31N (EPSG:25831)**.

This projection is suitable for the study area and allows the calculations to be performed in metres.

## 3.3 Results

The total demand weight is:

$$\
\sum\_{i=1}^{7}W_i=2515\
$$

The independently recalculated weighted projected coordinates are:

$$\
\boxed{E^\*=422010.6094\text{ m}}\
$$

$$\
\boxed{N^\*=4599632.8017\text{ m}}\
$$

The inverse projection gives:

$$\
\text{Latitude}=41.5445552556^\circ\
$$

$$\
\text{Longitude}=2.0649425975^\circ\
$$

Therefore:

$$\
\boxed{41.544555^\circ\text{ N},\quad2.064943^\circ\text{ E}}\
$$

The nearest identifiable address returned by reverse geocoding is: **Camí de Can Coniller, 08220 Terrassa, Barcelona, Spain.**

## 3.4 Interpretation

The Centre of Gravity identifies **Camí de Can Coniller, 08220 Terrassa, Barcelona, Spain.** as the geographic  weighted center of gravity for all seven hospital facilities. The identified location would serve as the location of the laundry facility if the center of gravitiy method was the deciding factor for the final location. However as already established in the executive summary, the business owner follows the Cost Factor model strategy.


---

# 4. Factor-Rating Method

## 4.1 Methodology

The Factor-Rating Method compares candidate locations using weighted qualitative criteria.

Each criterion receives a weight, and each candidate receives a score from 1 (least favourable) to 5 (most favourable).

The weighted score is:

$$\
S_j=\sum\_{k=1}^{m}w_kr\_{jk}\
$$

Where:

- $S_j$ = Weighted score of candidate $j$.
- $w_k$ = Weight of criterion $k$.
- $r\_{jk}$ = Candidate score for criterion $k$.
- $m$ = Number of criteria.

The maximum possible score is 5.

## 4.2 Evaluation Criteria

| Criterion                                   | Weight   |
| ------------------------------------------- | -------- |
| Proximity to healthcare facilities          | 25%      |
| Road accessibility                          | 20%      |
| Evidence of suitable premises               | 20%      |
| Industrial compatibility                    | 15%      |
| Utilities and infrastructure                | 10%      |
| Environmental and residential compatibility | 10%      |
| **Total**                                   | **100%** |

## 4.3 Candidate Scores

| Candidate | Proximity | Roads | Premises | Industrial | Utilities | Environment |
| --------- | --------- | ----- | -------- | ---------- | --------- | ----------- |
| IA-T      | 5         | 4     | 3        | 5          | 3         | 3           |
| IA-S1     | 4         | 4     | 2        | 5          | 3         | 3           |
| IA-S2     | 3         | 5     | 5        | 5          | 4         | 3           |
| IA-R1     | 2         | 4     | 4        | 5          | 4         | 3           |
| IA-R2     | 2         | 4     | 4        | 5          | 4         | 3           |
| IA-C      | 2         | 5     | 2        | 3          | 4         | 3           |

The scores are indicative comparative assessments based on the available geographical and industrial evidence. They are not the result of formal site inspections or technical audits.

## 4.4 Weighted Results

For IA-S2 — Can Roqueta:

$$
\begin{aligned}
S_{\text{IA-S2}}={}&0.25(3)+0.20(5)+0.20(5)\\
&+0.15(5)+0.10(4)+0.10(3)
\end{aligned}
$$

$$
\boxed{S_{\text{IA-S2}}=4.20/5}
$$

The weighted results for all candidates are:

| Candidate | Weighted Score | Rank |
|---|---:|---:|
| **IA-S2 — Can Roqueta** | **4.20** | **1** |
| IA-T — Els Bellots | 4.00 | 2 |
| IA-S1 — Sant Pau de Riu-sec | 3.55 | 3 |
| IA-R1 — Can Jardí | 3.55 | 3 |
| IA-R2 — Cova Solera | 3.55 | 3 |
| IA-C — Cerdanyola | 3.05 | 6 |

IA-S2 — Can Roqueta achieves the highest weighted score of **4.20/5**, followed by IA-T — Els Bellots with **4.00/5**. IA-S1, IA-R1 and IA-R2 are tied in third place, each scoring **3.55/5**.

## 4.5 Interpretation

The Factor-Rating Method identifies IA-S2 — Can Roqueta as the highest-scoring candidate.

Its result is supported by its favourable assessment of road accessibility, evidence of suitable industrial premises and industrial compatibility.

IA-T — Els Bellots ranks second, supported by its geographical proximity to the healthcare facilities.

The Factor-Rating Method is a qualitative assessment. Its result depends on the selected criteria, weights and assigned scores. It complements, but does not replace, the economic comparison.

---

# 5. Cost Model

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

$$\
d\_{\text{road}}=d\_{\text{map}}\times f\
$$

Transport cost is estimated using:

$$\
C\_{\text{transport}}=\
d\_{\text{map}}\times f\times q\times c\times n\
$$

Where:

- $d\_{\text{map}}$ = Geographical distance.
- $f$ = Road-distance conversion factor.
- $q$ = Number of journeys per operating period.
- $c$ = Transport cost per kilometre.
- $n$ = Number of operating periods per year.

The adopted assumptions are:

| Parameter                       | Assumption                      |
| ------------------------------- | ------------------------------- |
| Road-distance conversion factor | 1.30                            |
| Transport cost benchmark        | €1.424/km                       |
| Distribution tours              | 2 complete multi-stop tours/day |
| Distribution operating days     | 365 days/year                   |
| Supply journeys                 | 2 round trips/week              |
| Supply operating weeks          | 52 weeks/year                   |

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

| Candidate                   | Distribution/year | Supply/year | Combined/year |
| --------------------------- | ----------------- | ----------- | ------------- |
| IA-T — Els Bellots          | €43,544           | €9,213      | €52,757       |
| IA-S1 — Sant Pau de Riu-sec | €43,854           | €7,161      | €51,015       |
| IA-S2 — Can Roqueta         | €47,740           | €8,028      | €55,768       |
| IA-R1 — Can Jardí           | €42,838           | €6,698      | €49,536       |
| IA-R2 — Cova Solera         | €41,392           | €6,837      | €48,229       |
| IA-C — Cerdanyola           | €49,670           | €5,940      | €55,610       |

Combined transport cost is:

$$\
C\_{\text{transport}}=\
C\_{\text{distribution}}+\
C\_{\text{supply}}\
$$

For Cova Solera:

$$\
C\_{\text{transport,IA-R2}}=\
41,392+6,837\
$$

$$\
\boxed{C\_{\text{transport,IA-R2}}=€48,229/year}\
$$

Cova Solera has both the lowest estimated distribution transport cost (€41,392/year) and the lowest combined supply and distribution transport cost (€48,229/year) among the six candidate locations.

## 5.4 Property Rental Costs

A common reference warehouse area of 1,500 m² is used for all candidates.

The annual rental cost is:

$$\
C\_{\text{rent}}=R\times A\times12\
$$

Where:

- $R$ = Monthly rental rate (€ / m²).
- $A$ = Reference warehouse area (m²).
- $12$ = Months per year.

For Cova Solera:

$$\
C\_{\text{rent}}=4.00\times1,500\times12\
$$

$$\
\boxed{C\_{\text{rent}}=€72,000/year}\
$$

The comparative rental estimates are:

| Candidate                   | Indicative rent €/m²/month | Annual rent |
| --------------------------- | -------------------------- | ----------- |
| IA-R2 — Cova Solera         | €4.00                      | €72,000     |
| IA-R1 — Can Jardí           | €4.80                      | €86,400     |
| IA-S2 — Can Roqueta         | €5.00                      | €90,000     |
| IA-S1 — Sant Pau de Riu-sec | €5.50                      | €99,000     |
| IA-C — Cerdanyola           | €5.45                      | €98,100     |
| IA-T — Els Bellots          | €5.95                      | €107,100    |

These are indicative rental estimates, not confirmed contractual prices.

## 5.5 Fixed, Variable and Establishment Costs

The common operating-cost assumptions are:

| Cost component               | Calculation           | Annual cost    |
| ---------------------------- | --------------------- | -------------- |
| Fixed operating costs        | Planning estimate     | €1,000,000     |
| Variable processing costs    | €0.20 × 2,753,925 kg  | €550,785       |
| Establishment costs          | €1,500,000 / 10 years | €150,000       |
| **Total common annual cost** | <br>                  | **€1,700,785** |

### Variable Processing Costs

$$\
C\_{\text{variable}}=\
Q\_{\text{annual}}\times c\_{\text{variable}}\
$$

$$\
C\_{\text{variable}}=\
2,753,925\times0.20\
$$

$$\
\boxed{C\_{\text{variable}}=€550,785/year}\
$$

### Annual Establishment Cost

The €1,500,000 establishment investment is allocated over ten years using a simple straight-line method:

$$\
C\_{\text{establishment,annual}}=\
\frac{1,500,000}{10}\
$$

$$\
\boxed{C\_{\text{establishment,annual}}=€150,000}\
$$

### Total Common Annual Cost

$$\
C\_{\text{common}}=\
C\_{\text{fixed}}+\
C\_{\text{variable}}+\
C\_{\text{establishment,annual}}\
$$

$$\
C\_{\text{common}}=\
1,000,000+550,785+150,000\
$$

$$\
\boxed{C\_{\text{common}}=€1,700,785/year}\
$$

These figures are planning assumptions, not supplier quotations or a detailed financial feasibility estimate. The establishment cost uses a simple straight-line annual allocation, without a financing rate or discounted cash-flow calculation.

Because these costs are held constant across all candidates, they do not affect the relative ranking.

## 5.6 Total Annual Equivalent Cost

The total annual equivalent cost is:

$$\
\begin{aligned}\
C\_{\text{total},j}={}&C\_{\text{rent},j}\\\
&+C\_{\text{supply},j}\\\
&+C\_{\text{distribution},j}\\\
&+C\_{\text{fixed}}\\\
&+C\_{\text{variable}}\\\
&+\frac{C\_{\text{establishment}}}{10}\
\end{aligned}\
$$

For Cova Solera:

$$\
\begin{aligned}\
C\_{\text{total,IA-R2}}={}&72,000+6,837+41,392\\\
&+1,000,000+550,785+150,000\
\end{aligned}\
$$

$$\
\boxed{C\_{\text{total,IA-R2}}=€1,821,014/year}\
$$

### Cost Comparison

| Rank  | Candidate                   | Rent        | Transport   | Common costs   | Annual total   |
| ----- | --------------------------- | ----------- | ----------- | -------------- | -------------- |
| **1** | **IA-R2 — Cova Solera**     | **€72,000** | **€48,229** | **€1,700,785** | **€1,821,014** |
| 2     | IA-R1 — Can Jardí           | €86,400     | €49,536     | €1,700,785     | €1,836,721     |
| 3     | IA-S2 — Can Roqueta         | €90,000     | €55,768     | €1,700,785     | €1,846,553     |
| 4     | IA-S1 — Sant Pau de Riu-sec | €99,000     | €51,015     | €1,700,785     | €1,850,800     |
| 5     | IA-C — Cerdanyola           | €98,100     | €55,610     | €1,700,785     | €1,854,495     |
| 6     | IA-T — Els Bellots          | €107,100    | €52,757     | €1,700,785     | €1,860,642     |

## 5.7 Cost Model Result

Cova Solera achieves the lowest estimated annual equivalent cost:

**€1,821,014/year.**

The second-ranked candidate, Can Jardí, has an estimated annual cost of €1,836,721.

The difference is:

$$\
1,836,721-1,821,014\
\=\boxed{€15,707/year}\
$$

The economic advantage is relatively modest and depends on the adopted rental and transport assumptions. Nevertheless, Cova Solera ranks first under the stated Cost Model and the project owner's priorities.

---

# 6. Geographic Coverage Method

The Geographic Coverage Method evaluates how effectively each candidate industrial area covers the seven healthcare facilities within specified geographical distance thresholds.

Hospital bed capacity is used as the demand weight.

**Distance qualification:** The calculations use geodesic straight-line distances between representative coordinates. They are geographical proxies, not road-network shortest paths or vehicle travel times.

## 6.1 Weighted Mean Distance

The weighted mean distance provides a comparative measure of proximity between each candidate and the hospital network.

For candidate $j$:

$$\
D_j=\
\frac{\sum\_{i=1}^{n}W_i d\_{ij}}\
{\sum\_{i=1}^{n}W_i}\
$$

Where:

- $D_j$ = Weighted mean distance for candidate $j$.
- $W_i$ = Bed capacity of hospital $i$.
- $d\_{ij}$ = Straight-line distance between hospital $i$ and candidate $j$.
- $n$ = Number of healthcare facilities.

The results are:

| Candidate                   | Weighted mean distance |
| --------------------------- | ---------------------- |
| IA-T — Els Bellots          | **4.48 km**            |
| IA-S1 — Sant Pau de Riu-sec | 6.22 km                |
| IA-S2 — Can Roqueta         | 6.75 km                |
| IA-C — Cerdanyola           | 8.46 km                |
| IA-R2 — Cova Solera         | 8.61 km                |
| IA-R1 — Can Jardí           | 9.37 km                |

Els Bellots achieves the lowest weighted mean straight-line distance.

This is a weighted mean distance analysis, not a median calculation or a road-network shortest-path model.

## 6.2 Coverage Methodology

For candidate $j$ and coverage radius $R$, covered demand is:

$$\
C_j(R)=\sum\_{i=1}^{n}W_i I(d\_{ij}\leq R)\
$$

Where:

- $C_j(R)$ = Covered demand for candidate $j$.
- $W_i$ = Bed capacity of hospital $i$.
- $d\_{ij}$ = Straight-line geographical distance.
- $R$ = Selected coverage radius.
- $I(\cdot)$ = Indicator equal to 1 when the hospital is within the radius and 0 otherwise.

Coverage percentage is:

$$\
Coverage_j(R)=\
\frac{C_j(R)}{2515}\times100\
$$

The baseline coverage radius is:

$$\
\boxed{R=7.5\text{ km}}\
$$

This is a project modelling assumption, not a statutory requirement or established operational service standard.

## 6.3 Baseline Coverage Results

| Candidate | Covered beds | Coverage |
|---|---:|---:|
| **IA-T — Els Bellots** | **2,211** | **87.9%** |
| IA-S1 — Sant Pau de Riu-sec | 1,834 | 72.9% |
| IA-S2 — Can Roqueta | 1,530 | 60.8% |
| IA-C — Cerdanyola | 513 | 20.4% |
| IA-R1 — Can Jardí | 442 | 17.6% |
| IA-R2 — Cova Solera | 442 | 17.6% |
| **Total network demand (reference)** | **2,515** | **100%** |

For Els Bellots:

$$\
Coverage\_{\text{IA-T}}=\
\frac{2211}{2515}\times100\ = 87.9
$$

Els Bellots therefore provides the highest baseline geographical coverage of 87.9\%.

## 6.4 Sensitivity to Coverage Radius

The coverage calculation is repeated using 5 km, 7.5 km and 10 km thresholds.

| Candidate                   | 5 km  | 7.5 km | 10 km |
| --------------------------- | ----- | ------ | ----- |
| IA-T — Els Bellots          | 45.4% | 87.9%  | 100%  |
| IA-S1 — Sant Pau de Riu-sec | 42.5% | 72.9%  | 100%  |
| IA-S2 — Can Roqueta         | 37.1% | 60.8%  | 60.8% |
| IA-R1 — Can Jardí           | 12.1% | 17.6%  | 38.9% |
| IA-R2 — Cova Solera         | 17.6% | 17.6%  | 65.8% |
| IA-C — Cerdanyola           | 5.5%  | 20.4%  | 72.9% |

Els Bellots and Sant Pau de Riu-sec achieve 100% coverage at 10 km.

The results also show that candidate performance depends on the selected distance threshold.

## 6.5 Interpretation

The geographical results favour Els Bellots:

- Lowest weighted mean distance: **4.48 km**.
- Highest baseline coverage: **87.9%**.
- Complete coverage at the 10 km threshold.

These results make Els Bellots the strongest candidate from a geographical proximity and coverage perspective.

However, the project owner's primary decision priority is total operating cost. The geographical results are therefore complementary evidence and do not override the Cost Model.

---

# 7. Summary Results and Final Selection

## 7.1 Comparison of the Methods

| Method              | Preferred result                | Main result                                             |
| ------------------- | ------------------------------- | ------------------------------------------------------- |
| Centre of Gravity   | Theoretical point near Terrassa | Demand-weighted geographical balance                    |
| Factor-Rating       | IA-S2 — Can Roqueta             | Highest score: 4.20/5                                   |
| Cost Model          | IA-R2 — Cova Solera             | Lowest annual cost: €1,821,014                          |
| Geographic Coverage | IA-T — Els Bellots              | 4.48 km weighted mean distance; 87.9% baseline coverage |

The methods produce different results because they evaluate different location criteria.

- **Centre of Gravity:** Identifies a theoretical demand-weighted geographical balance point.
- **Factor-Rating:** Favours Can Roqueta based on the weighted qualitative criteria.
- **Geographic Coverage:** Favours Els Bellots based on proximity and geographical coverage.
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

$$\
R=\frac{6000}{1500}\
$$

$$\
\boxed{R=€4.00/\text{m}^2/\text{month}}\
$$

The annual rental cost is:

$$\
C\_{\text{annual}}=6000\times12\
$$

$$\
\boxed{C\_{\text{annual}}=€72,000/year}\
$$

## 7.4 Selection Rationale

Cova Solera is selected because:

1. It achieves the lowest estimated annual equivalent cost.
2. It has the lowest indicative rental cost among the six candidates.
3. It has the lowest estimated distribution transport cost.
4. Its combined supply and distribution transport cost is competitive.
5. An identifiable warehouse listing supports the rental assumption.
6. Its selection directly reflects the project owner's cost-based priorities.

---

# 8. Conclusion

This study compared six candidate industrial areas for a centralized hospital laundry serving seven healthcare facilities in Vallès Occidental.

The estimated demand is **7,545 kg/day**, equivalent to **2,753,925 kg/year**, based on the assumed generation rate of 3.0 kg per bed per day.

Four complementary location-analysis methods were applied:

- Centre of Gravity Method.
- Factor-Rating Method.
- Cost Model.
- Geographic Coverage Method.

The results identify different strengths among the candidates. Can Roqueta achieves the highest Factor-Rating score, while Els Bellots provides the best geographical proximity and coverage.

However, the project owner's primary priority is minimizing total annual costs, including supply transport, distribution transport, fixed operating, variable processing and establishment costs.

**Final decision: Cova Solera, Rubí, is the preferred location because it achieves the lowest estimated annual equivalent cost of €1,821,014 under the adopted project assumptions.**
---

# References

1. **Course lecture material.** *Location Strategies*. Methods applied include Centre of Gravity, Factor-Rating, Cost Models and geographical coverage assessment.
2. **Institut Cartogràfic i Geològic de Catalunya (ICGC).** Geocoding and reverse-geocoding services.\
   [https://eines.icgc.cat/geocodificador/](https://eines.icgc.cat/geocodificador/)
3. **EPSG Geodetic Parameter Dataset.** EPSG:25831 — ETRS89 / UTM Zone 31N.
4. **GeographicLib.** Geodesic calculation conventions.\
   [https://geographiclib.sourceforge.io/](https://geographiclib.sourceforge.io/)
5. **Idealista.** Public industrial warehouse listings in Polígono Cova Solera, Rubí. The comparative reference used in this study is an advertised warehouse of approximately 1,500 m² at approximately €6,000/month.\
   [https://www.idealista.com/geo/alquiler-locales/avenida-cova-solera-rubi-barcelona/con-naves/](https://www.idealista.com/geo/alquiler-locales/avenida-cova-solera-rubi-barcelona/con-naves/)
6. **AMB Naus i Solars.** Industrial property reference for Can Jardí, Rubí: approximately 1,001 m² at €4.80/m²/month.
7. **Masachs.** Industrial rental-market information for Sabadell, published 7 May 2026. Used as indicative market context for industrial rental assumptions.
8. **FROET.** Spanish articulated-vehicle operating-cost benchmark, report dated 17 September 2026, with costs updated July 2026. General-goods articulated vehicle reference: €1.424/km. Used as a comparative transport-cost proxy.
9. **UBICAT.** Sabadell, Can Roqueta II, industrial warehouse development, reference 1178.\
   [https://www.ubicat.cat/es/sabadell/p_i_can_roqueta_ii/naves_industriales/ref-1178](https://www.ubicat.cat/es/sabadell/p_i_can_roqueta_ii/naves_industriales/ref-1178)
10. **Geographical and property comparison dataset.** Hospital coordinates, candidate industrial-area coordinates and indicative rental references compiled for this study.
