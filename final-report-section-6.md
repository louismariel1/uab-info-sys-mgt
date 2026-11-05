# 6. Geographic Coverage Method

## 6.1 Methodology and Objective

The Geographic Coverage Method evaluates how effectively each of the six candidate industrial areas serves the seven healthcare facilities within Vallès Occidental.

The method considers two geographical performance measures:

1. Weighted mean distance: Measures the average distance between a candidate location and the healthcare network, giving greater importance to hospitals with more beds.
2. Geographical coverage: Measures the proportion of total hospital-bed demand located within a specified distance of each candidate.

Hospital bed capacity is used as a proxy for laundry demand.

All geographical distances are calculated as straight-line distances using the WGS84 geographical coordinates of the hospitals and representative coordinates of the candidate industrial areas.

These distances are geographical measurements, not road-network distances or actual vehicle travel times.

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

### Step 2: Calculate the weighted mean distance for Els Bellots

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

Best geographical proximity: Els BellotsEls Bellots achieves the lowest weighted mean distance, indicating that it provides the closest overall geographical position relative to the demand-weighted hospital network.

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
