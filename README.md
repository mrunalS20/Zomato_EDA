# Zomato Catalog Delivery: Exploratory Data Analysis

A comprehensive exploratory data analysis (EDA) project on the global Zomato restaurant dataset. This repository uncovers customer behavior patterns, local currency mappings, regional transaction hubs, and localized cuisine popularity across multiple continents using advanced statistical visualizations.

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.12
* **Data Cleansing & Transformation:** Pandas, NumPy
* **Statistical Visualizations:** Seaborn, Matplotlib

---

## 📊 Analytical Pipeline & Code Walkthrough

### 1. Relational Data Merging & Synchronization
Integrated multi-source business logs by implementing a left join between the core restaurant transaction logs (`zomato.csv`) and country definitions (`Country-Code.xlsx`) along the mutual `Country Code` primary key.

```python
df = pd.merge(zomato, country, on='Country Code', how='left')
