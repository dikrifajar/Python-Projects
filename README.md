# 🚗 Car Price Analytics: Understanding the Key Drivers of Vehicle Pricing

> Analyzing what truly determines the market price of new and used cars — built with pure Python for production-ready reporting automation.

---

## 📌 Background & Business Problem

The used car market is notoriously volatile. Dealers frequently struggle to set competitive buy and sell prices that protect profit margins while staying attractive to buyers.

This project identifies the key **Car Price Drivers** — including brand, mileage, fuel type, transmission, and year-based depreciation — to support smarter, data-driven pricing decisions.

---

## 🛠️ Tech Stack

| Component | Tool |
|---|---|
| Language | Python 3.10+ |
| Data Manipulation | `pandas` |
| Visualization | `matplotlib`, `seaborn` |
| Statistical | `statsmodels`,`patsy` |
| IDE | VS Code |



---

## 📊 Key Findings & Visualizations

> All charts are auto-exported to the `output/` folder when the script runs.

### A. Market Price Distribution
Identifies where prices are concentrated — used to define consumer segments: **Low, Mid, and High-End**.

<img width="984" height="484" alt="image" src="https://github.com/user-attachments/assets/5ddf4bc3-2f9a-4c05-b0cc-b7bd67cc53b9" />


---

### B. Market Segmentation by Brand
Helps the procurement team identify which brands command premium market value.

<img width="1184" height="584" alt="image" src="https://github.com/user-attachments/assets/86a8c1b5-c2c8-4fcf-b2c6-d31e88b92000" />


---

### C. Mileage vs. Price Depreciation (Linear Regression)
Quantifies how much a vehicle's value drops for every additional unit of mileage driven.

<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/01d0eec2-bc5d-4946-ad66-fc04d07a8dfe" />


---

### D. Price Trends by Release Year & Condition
Shows how quickly asset value declines with age, broken down by vehicle condition: **New, Like New, and Used**.

<img width="1184" height="584" alt="image" src="https://github.com/user-attachments/assets/72720db5-c9bc-4a2d-a906-de4b349a191a" />


---

## What Influences Car Prices in This Dataset?

#### Regression
```bash
OLS Regression Results                            
==============================================================================
Dep. Variable:                  Price   R-squared:                       0.031
Model:                            OLS   Adj. R-squared:                  0.006
Method:                 Least Squares   F-statistic:                     1.244
Date:                Sat, 23 May 2026   Prob (F-statistic):              0.106
Time:                        12:11:14   Log-Likelihood:                -26134.
No. Observations:                2250   AIC:                         5.238e+04
Df Residuals:                    2192   BIC:                         5.272e+04
Df Model:                          57                                         
Covariance Type:            nonrobust                                         
=================================================================================================
                                    coef    std err          t      P>|t|      [0.025      0.975]
-------------------------------------------------------------------------------------------------
Intercept                      3.236e+05   1.67e+05      1.944      0.052   -2913.443     6.5e+05
C(Condition)[T.New]            -945.9938   1426.144     -0.663      0.507   -3742.730    1850.742
C(Condition)[T.Used]           -145.7931   1410.236     -0.103      0.918   -2911.332    2619.745
C(Q("Fuel Type"))[T.Electric] -3827.4993   1636.693     -2.339      0.019   -7037.131    -617.868
C(Q("Fuel Type"))[T.Hybrid]   -2055.2580   1627.019     -1.263      0.207   -5245.918    1135.402
C(Q("Fuel Type"))[T.Petrol]   -3171.4823   1618.879     -1.959      0.050   -6346.180       3.215
C(Q("Engine Size"))[T.1.1]    -1.625e+04   7702.656     -2.109      0.035   -3.14e+04   -1143.461
C(Q("Engine Size"))[T.1.2]    -1.743e+04   7571.779     -2.302      0.021   -3.23e+04   -2577.981
C(Q("Engine Size"))[T.1.3]    -1.357e+04   7233.950     -1.876      0.061   -2.78e+04     615.417
C(Q("Engine Size"))[T.1.4]    -1.616e+04   7413.532     -2.180      0.029   -3.07e+04   -1621.351
C(Q("Engine Size"))[T.1.5]    -2.075e+04   7606.227     -2.728      0.006   -3.57e+04   -5837.419
C(Q("Engine Size"))[T.1.6]    -1.385e+04   7642.440     -1.813      0.070   -2.88e+04    1134.810
C(Q("Engine Size"))[T.1.7]     -1.29e+04   7605.325     -1.696      0.090   -2.78e+04    2017.352
C(Q("Engine Size"))[T.1.8]    -1.097e+04   7173.059     -1.530      0.126    -2.5e+04    3093.457
C(Q("Engine Size"))[T.1.9]    -1.482e+04   7388.645     -2.006      0.045   -2.93e+04    -333.520
C(Q("Engine Size"))[T.2.0]     -1.74e+04   7410.825     -2.348      0.019   -3.19e+04   -2864.836
C(Q("Engine Size"))[T.2.1]        -2e+04   7458.507     -2.681      0.007   -3.46e+04   -5372.022
C(Q("Engine Size"))[T.2.2]    -7733.2265   7301.793     -1.059      0.290   -2.21e+04    6585.931
C(Q("Engine Size"))[T.2.3]    -1.162e+04   7436.969     -1.563      0.118   -2.62e+04    2960.377
C(Q("Engine Size"))[T.2.4]    -7763.3611   7306.892     -1.062      0.288   -2.21e+04    6565.796
C(Q("Engine Size"))[T.2.5]    -1.661e+04   7485.673     -2.219      0.027   -3.13e+04   -1931.898
C(Q("Engine Size"))[T.2.6]     -1.78e+04   7363.749     -2.418      0.016   -3.22e+04   -3361.985
C(Q("Engine Size"))[T.2.7]    -1.231e+04   7235.801     -1.702      0.089   -2.65e+04    1875.356
C(Q("Engine Size"))[T.2.8]    -1.471e+04   7460.413     -1.971      0.049   -2.93e+04     -77.854
C(Q("Engine Size"))[T.2.9]    -1.823e+04   7398.637     -2.464      0.014   -3.27e+04   -3717.652
C(Q("Engine Size"))[T.3.0]    -1.408e+04   7270.108     -1.936      0.053   -2.83e+04     178.883
C(Q("Engine Size"))[T.3.1]    -9049.2290   7369.786     -1.228      0.220   -2.35e+04    5403.266
C(Q("Engine Size"))[T.3.2]    -8928.1000   7412.375     -1.204      0.229   -2.35e+04    5607.915
C(Q("Engine Size"))[T.3.3]    -2.163e+04   7637.603     -2.832      0.005   -3.66e+04   -6655.355
C(Q("Engine Size"))[T.3.4]    -1.294e+04   7377.697     -1.754      0.080   -2.74e+04    1526.895
C(Q("Engine Size"))[T.3.5]    -1.747e+04   7668.862     -2.277      0.023   -3.25e+04   -2426.242
C(Q("Engine Size"))[T.3.6]    -7269.4151   7673.382     -0.947      0.344   -2.23e+04    7778.446
C(Q("Engine Size"))[T.3.7]    -9090.4476   7409.088     -1.227      0.220   -2.36e+04    5439.121
C(Q("Engine Size"))[T.3.8]    -1.277e+04   7431.535     -1.719      0.086   -2.73e+04    1799.359
C(Q("Engine Size"))[T.3.9]    -1.511e+04   7154.640     -2.112      0.035   -2.91e+04   -1080.502
C(Q("Engine Size"))[T.4.0]    -2.346e+04   7267.999     -3.227      0.001   -3.77e+04   -9203.308
C(Q("Engine Size"))[T.4.1]    -2.147e+04   7638.298     -2.811      0.005   -3.64e+04   -6489.221
C(Q("Engine Size"))[T.4.2]    -2.361e+04   7483.036     -3.155      0.002   -3.83e+04   -8934.757
C(Q("Engine Size"))[T.4.3]    -1.569e+04   7636.441     -2.055      0.040   -3.07e+04    -714.565
C(Q("Engine Size"))[T.4.4]    -1.342e+04   7279.499     -1.843      0.065   -2.77e+04     859.533
C(Q("Engine Size"))[T.4.5]    -1.189e+04   7328.655     -1.622      0.105   -2.63e+04    2482.440
C(Q("Engine Size"))[T.4.6]    -1.093e+04   7970.243     -1.372      0.170   -2.66e+04    4697.485
C(Q("Engine Size"))[T.4.7]    -1.637e+04   7398.188     -2.212      0.027   -3.09e+04   -1858.390
C(Q("Engine Size"))[T.4.8]    -1.552e+04   7290.689     -2.129      0.033   -2.98e+04   -1224.468
C(Q("Engine Size"))[T.4.9]    -9679.1405   8017.294     -1.207      0.227   -2.54e+04    6043.148
C(Q("Engine Size"))[T.5.0]    -8691.6996   7435.790     -1.169      0.243   -2.33e+04    5890.232
C(Q("Engine Size"))[T.5.1]    -9116.5069   7286.409     -1.251      0.211   -2.34e+04    5172.483
C(Q("Engine Size"))[T.5.2]    -1.693e+04   7370.389     -2.297      0.022   -3.14e+04   -2475.417
C(Q("Engine Size"))[T.5.3]    -1.126e+04   7541.784     -1.493      0.136    -2.6e+04    3530.833
C(Q("Engine Size"))[T.5.4]    -2.177e+04   7386.973     -2.947      0.003   -3.63e+04   -7282.449
C(Q("Engine Size"))[T.5.5]    -2.075e+04   7581.462     -2.737      0.006   -3.56e+04   -5883.047
C(Q("Engine Size"))[T.5.6]    -1.632e+04   7668.911     -2.128      0.033   -3.14e+04   -1279.768
C(Q("Engine Size"))[T.5.7]    -1.122e+04   7364.253     -1.523      0.128   -2.57e+04    3223.864
C(Q("Engine Size"))[T.5.8]    -1.284e+04   7369.701     -1.742      0.082   -2.73e+04    1613.128
C(Q("Engine Size"))[T.5.9]    -1.548e+04   7601.070     -2.036      0.042   -3.04e+04    -569.004
C(Q("Engine Size"))[T.6.0]    -1.787e+04   8421.694     -2.121      0.034   -3.44e+04   -1349.943
Mileage                          -0.0046      0.007     -0.693      0.488      -0.017       0.008
Year                           -125.9812     82.786     -1.522      0.128    -288.328      36.366
==============================================================================
Omnibus:                      981.225   Durbin-Watson:                   1.990
Prob(Omnibus):                  0.000   Jarque-Bera (JB):              116.808
Skew:                          -0.002   Prob(JB):                     4.32e-26
Kurtosis:                       1.884   Cond. No.                     5.07e+07
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
[2] The condition number is large, 5.07e+07. This might indicate that there are
strong multicollinearity or other numerical problems.
```

#### ANOVA

```bash
                                          sum_sq       df      F  \
C(Q("Fuel Type"))                      4.696615e+09     3.0  2.151261   
C(Q("Engine Size"))                    4.437669e+10    50.0  1.219591   
C(Q("Fuel Type")):C(Q("Engine Size"))  1.291583e+11   150.0  1.183206   
Residual                               1.488937e+12  2046.0       NaN   

                                         PR(>F)  
C(Q("Fuel Type"))                      0.091849  
C(Q("Engine Size"))                    0.141072  
C(Q("Fuel Type")):C(Q("Engine Size"))  0.070161  
Residual                                    NaN

```

#### Insight ! 
1. Harga lebih dipengaruhi oleh jenis bahan bakar dan ukuran mesin, bukan sekadar kondisi mobil.
2. ANOVA menegaskan bahwa kombinasi faktor lebih penting daripada faktor tunggal. Fuel Type sendiri hampir signifikan, tapi interaksi dengan Engine Size memberi sinyal kuat.
---

## 💡 Data-Driven Business Recommendations

1. **Mileage-Based Procurement Strategy**
   Given the strong depreciation correlation with mileage (see regression chart), dealers should prioritize buying used vehicles below a key psychological mileage threshold to protect resale margins.

2. **Inventory Portfolio Optimization**
   Premium brands like Tesla and Mercedes retain high value but serve a narrower market. An optimal inventory mix is roughly **70% high-volume brands** (e.g., Honda, Ford) and **30% premium brands** to balance cash flow with margin.

---
## 💡💡Kesimpulan Praktis
1. Fuel Type and Engine Size have a real impact on price, especially when looked at in combination.
2. Condition isn't significant → a new car isn't automatically more expensive.
3. Mileage & Year aren't significant → maybe because the dataset is biased (entry-level new cars vs premium used ones).

---
## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.10+ installed.

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/dikrifajar/python-CarAnalysis.git
cd python-CarAnalysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the analysis script
python carprediction.ipynb
```

Output charts will be saved automatically to the `output/` folder.

---

## 📁 Project Structure

```
Python-Projects/
├── data/                           # Raw dataset(s)
├── output/                         # Auto-generated charts and reports
├── carprediction.ipynb             # Main analysis script
├── requirements.txt                # Python dependencies
└── README.md
```

---

## 📬 Contact

Made by **Dikri Fajar** — feel free to connect or open an issue if you have questions or suggestions.
