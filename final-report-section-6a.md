# 6\. Geographic Coverage Method

## 6.1 Methodology

The Geographic Coverage Method evaluates how effectively each candidate industrial area can serve the seven healthcare facilities within a defined geographical distance.

The objective is to identify which candidate location provides the greatest coverage of hospital demand within an acceptable service radius.

Hospital bed capacity is used as a proxy for laundry demand. Consequently, hospitals with more beds contribute more heavily to the coverage calculation.

The method uses geodesic straight-line distances between the representative coordinates of each candidate industrial area and the seven healthcare facilities.

**Distance qualification:** These are geographical distances, not road-network distances or actual vehicle travel times.

The coverage calculation is based on the following formula:

$$
C_j(R)=\sum_{i=1}^{n}W_i I(d_{ij}\leq R)
$$

Where:

- $C_j(R)$ = Total covered beds for candidate location $j$.
- $W_i$ = Number of beds at healthcare facility $i$.
- $d_{ij}$ = Straight-line distance between hospital $i$ and candidate location $j$.
- $R$ = Selected geographical coverage radius.
- $I(d_{ij}\leq R)$ = Indicator function, equal to 1 if the hospital is within the selected radius and 0 otherwise.
- $n$ = Total number of healthcare facilities (7).

The coverage percentage is calculated as:

$$
Coverage_j(R)=
\frac{C_j(R)}{\sum_{i=1}^{n}W_i}\times100
$$

The total hospital demand weight is:

$$
\sum_{i=1}^{7}W_i=2515\text{ beds}
$$

The baseline geographical coverage radius adopted for this study is:

$$
\boxed{R=7.5\text{ km}}
$$

The 7.5 km radius is a project modelling assumption used consistently across all six candidate locations. It is not a statutory requirement or an established operational service standard.

## 6.2 Worked Calculation Example – IA-T (Els Bellots)

To demonstrate how the Geographic Coverage Method is applied, IA-T (Els Bellots) is used as an example.

The first step is to compare the straight-line distance from Els Bellots to each of the seven healthcare facilities against the selected coverage radius of 7.5 km.

For each hospital:

- If its distance from Els Bellots is 7.5 km or less, its bed capacity is included in the covered demand.
- If its distance exceeds 7.5 km, its bed capacity is excluded.

The calculation can be represented as follows:

$$
C_{IA-T}(7.5)=
\sum_{i=1}^{7}W_i I(d_{i,IA-T}\leq7.5)
$$

Substituting the actual hospital bed capacities:

$$
\begin{aligned}
C_{IA-T}(7.5)={}&861I(d_{1,IA-T}\leq7.5)\\
&+460I(d_{2,IA-T}\leq7.5)\\
&+604I(d_{3,IA-T}\leq7.5)\\
&+304I(d_{4,IA-T}\leq7.5)\\
&+138I(d_{5,IA-T}\leq7.5)\\
&+77I(d_{6,IA-T}\leq7.5)\\
&+71I(d_{7,IA-T}\leq7.5)
\end{aligned}
$$

Based on the reported coverage result, Els Bellots covers 2,211 beds within the 7.5 km radius.

The coverage percentage is therefore:

$$
Coverage_{IA-T}(7.5)=
\frac{2211}{2515}\times100 = 87.9
$$

This means that, under the adopted geographical distance threshold, Els Bellots covers approximately 87.9% of the total hospital bed capacity.

The remaining demand is:

$$
2515-2211=304\text{ beds}
$$

Therefore, 304 beds, representing approximately 12.1% of total demand, are located outside the baseline coverage radius.

## 6.3 Baseline Geographic Coverage Results

The same calculation is applied to all six candidate industrial areas using the same 7.5 km coverage radius.

| Candidate | Covered beds | Coverage |
| --- | --- | --- |
| **IA-T — Els Bellots** | **2,211** | **87.9%** |
| IA-S1 — Sant Pau de Riu-sec | 1,834 | 72.9% |
| IA-S2 — Can Roqueta | 1,530 | 60.8% |
| IA-C — Cerdanyola | 513 | 20.4% |
| IA-R1 — Can Jardí | 442 | 17.6% |
| IA-R2 — Cova Solera | 442 | 17.6% |
| **Total network demand (reference)** | **2,515** | **100%** |

Els Bellots achieves the highest geographical coverage, with 2,211 beds or 87.9% of total hospital demand within the 7.5 km radius.

Sant Pau de Riu-sec ranks second, covering 72.9% of total demand, followed by Can Roqueta with 60.8%.

Cova Solera and Can Jardí achieve the lowest baseline coverage, each covering 17.6% of total demand.

## 6.4 Sensitivity Analysis – Alternative Coverage Radii

To assess whether the results depend significantly on the selected coverage radius, the calculation is repeated using three different geographical thresholds:

- 5 km.
- 7.5 km.
- 10 km.

This sensitivity analysis demonstrates how the proportion of hospital demand covered changes as the acceptable geographical service radius increases.

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| IA-T — Els Bellots | 45.4% | 87.9% | 100% |
| IA-S1 — Sant Pau de Riu-sec | 42.5% | 72.9% | 100% |
| IA-S2 — Can Roqueta | 37.1% | 60.8% | 60.8% |
| IA-R1 — Can Jardí | 12.1% | 17.6% | 38.9% |
| IA-R2 — Cova Solera | 17.6% | 17.6% | 65.8% |
| IA-C — Cerdanyola | 5.5% | 20.4% | 72.9% |

The results indicate that Els Bellots and Sant Pau de Riu-sec both achieve 100% geographical coverage when the radius is increased to 10 km.

Els Bellots remains the strongest geographical candidate at the baseline 7.5 km threshold and also performs particularly well at the 5 km threshold.

The analysis also demonstrates that the relative coverage of some candidates changes substantially when the geographical radius increases. Therefore, the selection of a coverage threshold influences the comparative results.

## 6.5 Interpretation

The Geographic Coverage Method identifies **IA-T — Els Bellots** as the strongest candidate from a geographical coverage perspective.

Its main advantages are:

- Highest baseline coverage: 87.9%.
- Highest covered demand: 2,211 beds.
- 100% geographical coverage at the 10 km threshold.
- Strong performance at the more restrictive 5 km threshold.

These results indicate that Els Bellots offers the best geographical proximity to the hospital network under the adopted coverage assumptions.

However, geographical coverage is only one dimension of the overall location decision.

The project owner's principal priority is to compare transport-supply, transport-distribution and operating costs, including fixed, variable and establishment costs.

Consequently, although Els Bellots performs best geographically, the Cost Model remains the controlling method for the final location selection.

Cova Solera, Rubí, is therefore retained as the preferred location because it achieves the lowest estimated annual equivalent cost of €1,821,014 under the adopted assumptions.
