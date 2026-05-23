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
| IDE | VS Code |

> Built as a **Pure Python Script** for easy scheduling and periodic report automation.

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
<img width="1601" height="1224" alt="image" src="https://github.com/user-attachments/assets/4e661df7-c244-40a0-9104-eda568db2c40" />

#### ANOVA

<img width="1204" height="451" alt="image" src="https://github.com/user-attachments/assets/2dbb7b21-4bf8-4a62-a207-2a58e09890e7" />

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
git clone https://github.com/dikrifajar/Python-Projects.git
cd Python-Projects

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
