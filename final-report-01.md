Below is the revised Section 6, ready to insert into your final report. I have removed the sensitivity analysis, strengthened the explanation of how the winning location is determined, and included a worked calculation.

One important point: the hospital-by-hospital coverage breakdown must be verified against the original distance dataset before inserting individual hospital names. I have therefore retained the confirmed aggregate of 2,211 beds without inventing which hospitals contribute to it.

Writing

# 6\. Geographic Coverage Method

## 6.1 Methodology and Objective

The Geographic Coverage Method evaluates how effectively each candidate industrial area can serve the seven healthcare facilities within a predefined geographical distance.

Unlike the Centre of Gravity Method, which identifies a theoretical geographical balance point, the Geographic Coverage Method identifies the candidate location that provides the greatest coverage of healthcare demand within a specified distance.

Hospital bed capacity is used as the demand weight because it represents the assumed relative laundry demand of each healthcare facility.

The method follows four steps:

1. Calculate the geographical distance between each candidate industrial area and each of the seven hospitals.
2. Identify which hospitals fall within the selected coverage radius.
3. Add the bed capacities of the hospitals within that radius.
4. Calculate the percentage of total hospital demand covered by each candidate.

The candidate covering the highest percentage of total hospital bed capacity is considered the preferred location under this method.

**Distance qualification:** The calculations use geodesic straight-line distances between representative coordinates. They are geographical proxies, not road-network distances or actual vehicle travel times.

## 6.2 Coverage Formula

For candidate location $j$, covered demand is calculated as:

$$
C_j(R)=\sum_{i=1}^{n}W_i I(d_{ij}\leq R)
$$

Where:

- $C_j(R)$ = Total covered hospital beds for candidate $j$.
- $W_i$ = Number of beds at hospital $i$.
- $d_{ij}$ = Straight-line geographical distance between hospital $i$ and candidate $j$.
- $R$ = Selected coverage radius.
- $I(d_{ij}\leq R)$ = Indicator equal to 1 if the hospital is within the coverage radius and 0 otherwise.
- $n$ = Total number of healthcare facilities (7).

Coverage percentage is then calculated as:

$$
Coverage_j(R)=
\frac{C_j(R)}{\sum_{i=1}^{n}W_i}\times100
$$

The total hospital network demand is:

$$
\sum_{i=1}^{7}W_i=2515\text{ beds}
$$

The baseline coverage radius adopted for this study is:

$$
\boxed{R=7.5\text{ km}}
$$

The 7.5 km radius is a project modelling assumption used consistently to compare the six candidate locations. It is not a statutory requirement or an established operational service standard.

## 6.3 Worked Calculation: IA-T — Els Bellots

The coverage calculation is demonstrated using IA-T — Els Bellots.

Based on the geographical distance calculations, hospitals within 7.5 km of Els Bellots account for a combined demand of 2,211 beds.

The calculation is:

$$
Coverage_{IA-T}(7.5)=
\frac{2211}{2515}\times100
$$

$$
Coverage_{IA-T}(7.5)=87.8926\%
$$

Therefore:

$$
\boxed{Coverage_{IA-T}(7.5)=87.9\%}
$$

This means that 87.9% of the total hospital bed capacity is located within a 7.5 km straight-line geographical radius of Els Bellots.

The remaining demand is:

$$
2515-2211=304\text{ beds}
$$

Consequently, 304 beds, equivalent to approximately 12.1% of total demand, fall outside the selected coverage radius.

This example demonstrates how the method converts geographical distances into a measurable percentage of covered hospital demand.

## 6.4 Comparative Coverage Results

The same calculation is applied to all six candidate industrial areas.

| Candidate industrial area | Covered beds | Coverage | Rank |
| --- | --- | --- | --- |
| **IA-T — Els Bellots** | **2,211** | **87.9%** | **1** |
| IA-S1 — Sant Pau de Riu-sec | 1,834 | 72.9% | 2 |
| IA-S2 — Can Roqueta | 1,530 | 60.8% | 3 |
| IA-C — Cerdanyola | 513 | 20.4% | 4 |
| IA-R1 — Can Jardí | 442 | 17.6% | 5 |
| IA-R2 — Cova Solera | 442 | 17.6% | 5 |
| **Total network demand (reference)** | **2,515** | **100%** | — |

The results show that Els Bellots achieves the highest geographical coverage, with 2,211 beds or 87.9% of total hospital demand within the selected 7.5 km radius.

Sant Pau de Riu-sec ranks second with 72.9%, followed by Can Roqueta with 60.8%.

Can Jardí and Cova Solera achieve the lowest coverage, with 17.6% each.

## 6.5 Interpretation and Location Selection

The Geographic Coverage Method identifies **IA-T — Els Bellots as the preferred candidate location**.

Its selection is based on the following findings:

- It covers 2,211 of the network's 2,515 hospital beds.
- It achieves the highest coverage percentage of all six candidates, at 87.9%.
- It provides substantially greater baseline geographical coverage than the other alternatives.

The method therefore selects Els Bellots because it places the largest proportion of hospital demand within the specified geographical service radius.

It is important to distinguish this result from the findings of the other location methods. Geographic Coverage prioritises the proportion of demand located within a defined distance, rather than the lowest operating cost or the highest qualitative assessment.

**Conclusion:** Els Bellots is the preferred location under the Geographic Coverage Method. However, this result does not determine the overall project selection. Since the project owner's primary decision criterion is minimising total annual operating and establishment costs, the Cost Model remains the controlling method for the final location decision. Accordingly, Cova Solera remains the overall recommended location.

## One final check before inserting Section 6

I have deliberately not included a hospital-by-hospital list because the individual distance results are not present in the material available here. The aggregate coverage figures are retained from your report.

If you have the original distance matrix, we should verify that the 2,211 beds are correctly obtained by adding the hospitals within 7.5 km. That is the final detail needed to make this section fully auditable.
