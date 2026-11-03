# Independent recalculation – geographical location analysis

I will use the three agreed methodologies and the original seven hospital locations, six candidate coordinates and bed weights from your report.

The recalculation will distinguish between the mathematical results and the original reported figures, so that any discrepancies can be identified before you update the report.

## 1. Calculation methodology

| Analysis | Method adopted |
| --- | --- |
| Centre of Gravity | Weighted projected coordinates, ETRS89 / UTM 31N (EPSG:25831) |
| Weighted mean distance | WGS84 geodesic distance |
| Coverage | WGS84 geodesic distance, with 5, 7.5 and 10 km thresholds |
| Hospital demand weights | Number of beds |
| Total demand weight | 2,515 beds |

The weighted distance and coverage calculations will use the same geodesic distance convention. This avoids comparing results generated using different distance systems.

## 2. Centre of Gravity – recalculated result

Verified – original result confirmedI independently projected all seven hospital coordinates into ETRS89 / UTM Zone 31N, using the GRS80 ellipsoid and the EPSG:25831 projection parameters.

EPSG:25831

The weighted calculations produced:

$$
E^*=422010.6094\text{ m}
$$

$$
N^*=4599632.8017\text{ m}
$$

The inverse projection produced:

$$
\text{Latitude}=41.5445552556^\circ
$$

$$
\text{Longitude}=2.0649425975^\circ
$$

Verified Centre of Gravity

Confirmed

# 41.544555° N

# 2.064943° E

Original report: 41.544555° N, 2.064943° E

No discrepancy at the reported six-decimal precision.

Conclusion: Keep the original Centre of Gravity result. It has been independently reproduced.

## 3. Weighted mean distances – recalculated results

All six results reproduced, with one rounding discrepancyI calculated the geodesic distance between each of the seven hospitals and each of the six candidate industrial areas using the WGS84 ellipsoid.

This produced 42 individual distances.

### 3.1 Hospital-to-candidate distance matrix

All distances are in kilometres, rounded to three decimal places.

| Hospital | Els Bellots | Sant Pau | Can Roqueta | Can Jardí | Cova Solera | Cerdanyola |
| --- | --- | --- | --- | --- | --- | --- |
| H01 | 5.776 | 4.941 | 2.977 | 11.900 | 11.023 | 7.969 |
| H02 | 1.227 | 6.197 | 7.128 | 9.629 | 8.765 | 9.151 |
| H03 | 2.547 | 8.861 | 10.196 | 10.042 | 9.291 | 11.523 |
| H04 | 8.325 | 6.264 | 10.229 | 1.985 | 1.662 | 5.392 |
| H05 | 7.320 | 3.127 | 7.048 | 5.144 | 4.496 | 2.494 |
| H06 | 2.464 | 8.774 | 10.156 | 9.906 | 9.156 | 11.419 |
| H07 | 6.652 | 2.591 | 1.516 | 10.386 | 9.566 | 5.271 |

### 3.2 Weighted mean distance comparison

The weighted mean distance is calculated using:

$$
\bar d_j=
\frac{\sum_{i=1}^{7}W_id_{ij}}{2515}
$$

The recalculated results are:

| Candidate | Original report | Recalculated | Difference |
| --- | --- | --- | --- |
| Els Bellots | 4.48 km | 4.48 km | 0.00 km |
| Sant Pau | 6.22 km | 6.22 km | 0.00 km |
| Can Roqueta | 6.74 km | 6.75 km | +0.01 km |
| Can Jardí | 9.37 km | 9.37 km | 0.00 km |
| Cova Solera | 8.61 km | 8.61 km | 0.00 km |
| Cerdanyola | 8.46 km | 8.46 km | 0.00 km |

The one identified discrepancy

Rounding correctionCan Roqueta:

$$
\bar d_{\text{Can Roqueta}}=6.7484\text{ km}
$$

Conventional rounding to two decimal places gives:

$$
\boxed{6.75\text{ km}}
$$

The original report states 6.74 km. This may reflect truncation or a slightly different distance convention.

Conclusion: The geographical ranking remains unchanged. The only correction needed is Can Roqueta, from 6.74 km to 6.75 km.

## 4. Coverage sensitivity – recalculated results

All 18 percentages confirmedI recalculated the coverage using the WGS84 geodesic distances, with each hospital's complete bed weight counted when its distance is within the specified threshold.

The calculation is:

$$
C_j(R)=
\frac{
\sum_{i=1}^{7}W_iI(d_{ij}\leq R)
}{2515}\times100
$$

### 4.1 Recalculated coverage table

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| Els Bellots | 45.4% | 87.9% | 100.0% |
| Sant Pau | 42.5% | 72.9% | 100.0% |
| Can Roqueta | 37.1% | 60.8% | 60.8% |
| Can Jardí | 12.1% | 17.6% | 38.9% |
| Cova Solera | 17.6% | 17.6% | 65.8% |
| Cerdanyola | 5.5% | 20.4% | 72.9% |

All values reproduce the original report after rounding to one decimal place.

### 4.2 Additional verification: covered bed counts

The underlying bed counts are also reproduced:

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| Els Bellots | 1,141 | 2,211 | 2,515 |
| Sant Pau | 1,070 | 1,834 | 2,515 |
| Can Roqueta | 932 | 1,530 | 1,530 |
| Can Jardí | 304 | 442 | 979 |
| Cova Solera | 442 | 442 | 1,654 |
| Cerdanyola | 138 | 513 | 1,834 |

### 4.3 Comparison with original results

| Coverage threshold | Original report | Recalculation | Discrepancy |
| --- | --- | --- | --- |
| 5 km | 6 percentages | 6 matching percentages | None |
| 7.5 km | 6 percentages | 6 matching percentages | None |
| 10 km | 6 percentages | 6 matching percentages | None |

Conclusion: All coverage sensitivity results are confirmed. No corrections are required.

## 5. Final discrepancy register

This is the consolidated list of changes needed in your report.

| Result | Original | Verified result | Action |
| --- | --- | --- | --- |
| Centre of Gravity latitude | 41.544555° | 41.544555° | Retain |
| Centre of Gravity longitude | 2.064943° | 2.064943° | Retain |
| Els Bellots weighted distance | 4.48 km | 4.48 km | Retain |
| Sant Pau weighted distance | 6.22 km | 6.22 km | Retain |
| Can Roqueta weighted distance | 6.74 km | 6.75 km | Correct |
| Can Jardí weighted distance | 9.37 km | 9.37 km | Retain |
| Cova Solera weighted distance | 8.61 km | 8.61 km | Retain |
| Cerdanyola weighted distance | 8.46 km | 8.46 km | Retain |
| Coverage sensitivity | All 18 values | All 18 confirmed | Retain |

## 6. Recommended replacement text for your report

The following can replace Sections 6.2–6.5 in your report.

Writing

### 6.2 Weighted Distance Comparison

The weighted mean geographical distance was independently recalculated using WGS84 geodesic distances between the seven healthcare facilities and the six candidate industrial areas.

The number of beds at each healthcare facility was used as the demand weight.

The weighted mean distance is calculated as:

$$
\bar d_j=
\frac{\sum_{i=1}^{7}W_id_{ij}}{\sum_{i=1}^{7}W_i}
$$

where:

- $W_i$ represents the number of beds at healthcare facility $i$.
- $d_{ij}$ represents the WGS84 geodesic distance between healthcare facility $i$ and candidate location $j$.
- The total demand weight is 2,515 beds.

The independently recalculated results are:

| Candidate | Weighted Mean Distance |
| --- | --- |
| IA-T – Els Bellots | **4.48 km** |
| IA-S1 – Sant Pau de Riu-sec | 6.22 km |
| IA-S2 – Can Roqueta | 6.75 km |
| IA-R1 – Can Jardí | 9.37 km |
| IA-R2 – Cova Solera | 8.61 km |
| IA-C – Cerdanyola | 8.46 km |

The results confirm that Els Bellots has the lowest weighted mean geographical distance to the healthcare network.

The recalculation confirms the original results, with one minor rounding correction: Can Roqueta changes from 6.74 km to 6.75 km.

### 6.3 Coverage Analysis

The coverage model evaluates the proportion of total hospital bed capacity located within a specified geodesic distance of each candidate location.

The coverage percentage is calculated as:

$$
C_j(R)=
\frac{
\sum_{i=1}^{7}W_iI(d_{ij}\leq R)
}{
2515
}\times100
$$

where:

- $W_i$ represents the bed capacity of healthcare facility $i$.
- $d_{ij}$ represents the WGS84 geodesic distance between healthcare facility $i$ and candidate $j$.
- $R$ represents the coverage threshold.
- $I(\cdot)$ is an indicator function equal to 1 when the distance is within the specified threshold and 0 otherwise.

The baseline coverage threshold is 7.5 km.

The independently recalculated results are:

| Candidate | Beds Within 7.5 km | Coverage |
| --- | --- | --- |
| IA-T – Els Bellots | 2,211 | **87.9%** |
| IA-S1 – Sant Pau de Riu-sec | 1,834 | 72.9% |
| IA-S2 – Can Roqueta | 1,530 | 60.8% |
| IA-C – Cerdanyola | 513 | 20.4% |
| IA-R1 – Can Jardí | 442 | 17.6% |
| IA-R2 – Cova Solera | 442 | 17.6% |

The results confirm that Els Bellots provides the highest geographical coverage of healthcare demand within the selected 7.5 km threshold.

### 6.4 Sensitivity to the Coverage Threshold

To assess the sensitivity of the coverage results, the calculations were independently repeated using three WGS84 geodesic distance thresholds: 5 km, 7.5 km and 10 km.

| Candidate | 5 km | 7.5 km | 10 km |
| --- | --- | --- | --- |
| IA-T – Els Bellots | 45.4% | 87.9% | 100.0% |
| IA-S1 – Sant Pau de Riu-sec | 42.5% | 72.9% | 100.0% |
| IA-S2 – Can Roqueta | 37.1% | 60.8% | 60.8% |
| IA-R1 – Can Jardí | 12.1% | 17.6% | 38.9% |
| IA-R2 – Cova Solera | 17.6% | 17.6% | 65.8% |
| IA-C – Cerdanyola | 5.5% | 20.4% | 72.9% |

All 18 coverage percentages were independently reproduced and agree with the original results after rounding to one decimal place.

### 6.5 Interpretation and Verification

The independent recalculation confirms that Els Bellots achieves the best geographical performance under both preliminary indicators:

- Lowest weighted mean geographical distance: 4.48 km.
- Highest baseline coverage: 87.9%.
- Full coverage of the hospital network within the 10 km threshold.

The Centre of Gravity calculation was also independently reproduced using weighted projected coordinates in ETRS89 / UTM Zone 31N (EPSG:25831), confirming the reported geographical coordinate of 41.544555° N, 2.064943° E.

These calculations provide a verified geographical comparison using consistent and documented coordinate and distance methodologies.

However, the results remain geographical indicators rather than road-network travel distances or actual vehicle travel times. A full operational logistics assessment would require road-network shortest-path calculations and validated transport routes.

The recalculated results do not change the overall location recommendation. Cova Solera remains the preferred candidate under the Cost Model, while Els Bellots remains the strongest candidate under the geographical distance and coverage criteria.

## 7. Overall conclusion

3 calculation groups independently reproducedYour original geographical analysis is substantially correct.

- Centre of Gravity: confirmed.
- Weighted mean distances: confirmed, with one rounding correction.
- Coverage sensitivity: all 18 percentages confirmed.

Only one numerical correction is necessary: Can Roqueta changes from 6.74 km to 6.75 km.

One final distinction is important: these calculations are independently reproduced from the coordinates and bed weights supplied in your report. They do not independently validate the real-world accuracy of those source coordinates.

The geographical analysis is now reproducible and suitable for inclusion in the interim technical report. The separate road-network and transport-cost validation remains outstanding.
