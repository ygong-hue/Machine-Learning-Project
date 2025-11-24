# 📊 Predicting Corporate Profitability: The Impact of ESG and Financial Metrics

## 🎯 Aim of the Project

### Context

Companies today face increasing pressure to balance financial performance with sustainability goals. Business leaders want to understand how operational metrics (e.g., revenue, market position, growth) and sustainability metrics (e.g., ESG scores, carbon emissions, resource usage) influence a company’s overall profitability.

To support data-driven strategic decisions, this analysis uses a multi-industry dataset containing financial, ESG, and environmental indicators for each company.

### Objective

The goal of this project is to build a predictive model that estimates a company’s **Profit Margin** using its financial, ESG, and environmental attributes. Specifically, the model aims to:

- Identify key drivers that influence profitability.  
- Quantify the relationship between ESG performance and profit margin.  
- Compare profitability patterns across different industries and regions.  
- Support strategic recommendations by highlighting improvement opportunities.  

The final model provides organizations with actionable insights to optimize performance while strengthening sustainability positioning.

---

## ⚙️ Project Setup and Execution

The core analysis and model building are performed in the following Jupyter Notebooks:

- `data_EDA.ipynb` – Exploratory Data Analysis  
- `data.ipynb` – Modeling and portfolio recommendation

### Prerequisites

- Python 3.8+
- Required libraries (imported in the notebooks):
numpy
pandas
seaborn
matplotlib
scipy
scikit-learn
xgboost


## 💾 Dataset Structure

Dataset contains 1,000 companies from 2015–2025.

| Column | Description | Type |
|--------|------------|------|
| CompanyID | Company ID | Numeric |
| CompanyName | Company name | Categorical |
| Industry | Business sector | Categorical |
| Region | Location | Categorical |
| Year | Reporting year | Numeric |
| Revenue | Revenue (M USD) | Numeric |
| ProfitMargin | Target variable (%) | Numeric |
| MarketCap | Market capitalization | Numeric |
| GrowthRate | Revenue growth (%) | Numeric |
| ESG_Overall | ESG score | Numeric |
| ESG_Environmental | Environmental score | Numeric |
| ESG_Social | Social score | Numeric |
| ESG_Governance | Governance score | Numeric |
| CarbonEmissions | CO₂ emissions | Numeric |
| WaterUsage | Water usage | Numeric |
| EnergyConsumption | Energy use | Numeric |

---


## 📝 Data Cleaning and Feature Engineering

### Missing Values
- GrowthRate had NaN values for year 2015.
- 1,000 rows were removed.
- Final dataset: 10,000 rows (2016–2025).

### Feature Engineering

Environmental features were highly correlated. They were replaced by:

Env_Intensity_Index = (CarbonEmissions + WaterUsage + EnergyConsumption) / 3

The original three columns were removed.

---


## ✅ Project Output

This project provides:
- Profit margin prediction  
- ESG impact analysis  
- Sustainability-focused portfolio insights  

It provides decision-makers with actionable insights to improve financial outcomes while strengthening ESG positioning.