# 📊 Predicting Corporate Profitability Using ESG & Financial Indicators

## 1. Project Overview

In recent years, Environmental, Social, and Governance (ESG) performance has become a critical factor in corporate strategy. Organizations and investors want to understand not only how ESG impacts sustainability outcomes, but also whether it influences **financial performance**.

This project analyzes the relationship between **financial metrics, ESG indicators, and corporate profitability**, and builds machine learning models to predict a company’s **Profit Margin**.

The project combines:
- Financial performance data  
- ESG scoring data  
- Environmental performance metrics  
- Machine learning modeling  

to generate both **predictive insights** and **strategic decision support**.

---

## 2. Aim & Objectives

### 🎯 Main Aim  
To develop a machine learning model that predicts a company’s **profit margin** based on its financial and ESG performance.

### ✅ Specific Objectives
- Analyze relationships between ESG metrics and profitability  
- Identify the strongest drivers of profit margins  
- Compare performance across industries and regions  
- Build and evaluate predictive models  
- Provide insights for ESG-driven investment and strategy decisions  

---

## 3. Dataset Description

The dataset contains financial, ESG, and environmental data for **1,000 companies** from **2015 to 2025** across multiple industries and regions.

### 📌 Key Features

| Feature | Description |
|--------|-------------|
| CompanyID | Unique company identifier |
| CompanyName | Company name |
| Industry | Industry sector |
| Region | Geographic region |
| Year | Reporting year |
| Revenue | Annual revenue (USD) |
| ProfitMargin | Profit margin (%) → **Target variable** |
| MarketCap | Market capitalization |
| GrowthRate | Revenue growth rate (%) |
| ESG_Overall | Overall ESG score |
| ESG_Environmental | Environmental score |
| ESG_Social | Social score |
| ESG_Governance | Governance score |
| CarbonEmissions | CO₂ emissions |
| WaterUsage | Water consumption |
| EnergyConsumption | Energy usage |

---

## 4. Data Cleaning & Feature Engineering

### 🧹 Data Cleaning
- The column `GrowthRate` contained missing values for the year **2015**.
- All rows with missing values were removed.
- Final dataset contains **10,000 rows** from **2016 to 2025**.

### 🛠 Feature Engineering
Environmental indicators were highly correlated.  
They were combined into a new composite index:

Env_Intensity_Index = (CarbonEmissions + WaterUsage + EnergyConsumption) / 3

## 5. Methodology

### 5.1 Exploratory Data Analysis (EDA)

The EDA phase includes:

- Distribution analysis of financial and ESG metrics  
- Industry and regional comparisons  
- Correlation analysis between ESG scores and profit margins  

---

### 5.2 Machine Learning Modeling

Several regression models were built and evaluated, including:

- Linear Regression  
- Random Forest  
- XGBoost  
- CatBoost  

Model performance was evaluated using the following metrics:

- **R² score**  
- **Mean Absolute Error (MAE)**  
- **Root Mean Squared Error (RMSE)**  

📓 **Notebook used:**  
`ESG_notebook.ipynb`

---

## 6. Project Structure

```bash
📁 Project Root
├── ESG_notebook.ipynb                
├── README.md                         
├── catboost_info/                   
├── data/                            
│   └── company_esg_financial_dataset.csv
├── Notebooks/
├── └── data_EDA.ipynb
├── └── data.ipynb        
├── .DS_Store                        
├── optuna_history.html              
└── rf_study.db                       