# Panel Regression Analysis of Gross Profit Margins in Japan's Bakery and Restaurant Industries

## 1. Overview

### Purpose

- In Japan, wheat is centrally imported and resold to food manufacturers at a fixed government price (official government selling price).
- Due to non-tariff barriers (import quotas), this price effectively determines the wheat input cost for companies.
- This project analyzes how government pricing policy affects corporate gross profit margins using firm-level panel data, with attention to inter-industry differences.
- **Null Hypothesis 1**: Government wheat prices have no effect on gross profit margins in bakery and restaurant firms.
- **Null Hypothesis 2**: The effect of government wheat prices on gross profit margins is the same across industries.
- We aim to statistically test and potentially reject these hypotheses.

### Target Firms

Firms with quarterly financial statements from two industries:

- **Bakery**: Yamazaki Baking Co., Ltd., Daiichiya Seipan, Nisshin Seifun Group Inc.
- **Restaurant**: Gyoza no Ohsho, Toridoll Holdings Corporation, Skylark Holdings Co., Ltd.

### Period

- 2015 Q1 to 2025 Q4

---

## 2. Project Structure

- `README_en.md`: short overview document (English)
- `README_full_en.md`: This overview document (English)
- `code.ipynb`: Main analysis notebook (fully reproducible by running sequential cells)
- `panel_data.xlsx`: Input dataset
- `output/`: Output folder containing visualizations and summary files

---

## 3. Data Sources

- **Gross Profit Margins**: IRBANK, financial reports from each company
- **Consumer Price Index (CPI)**: Statistics Bureau of Japan (specifically "Bread" and "Restaurant" CPI series)
- **Government Wheat Prices**: Ministry of Agriculture, Forestry and Fisheries (MAFF), official announcement documents

---

## 4. Analysis Workflow

1. Data preprocessing (quarterly encoding, lag variable creation, PCA, spline basis functions)
2. Fixed effects panel regression  
   (with **Driscoll-Kraay robust covariance estimation** and interaction terms)
3. Residual diagnostics (plots, ACF, VIF)
4. Model results and figure exports

---

## 5. How to Run

- Required libraries: `pandas`, `numpy`, `statsmodels`, `linearmodels`, `joblib`, `matplotlib`, `seaborn`
- Run `code.ipynb` using Jupyter Notebook
- Make sure `panel_data.xlsx` is placed in the same directory

---

## 6. Key Findings

- Wheat prices have a **statistically significant impact** on gross profit margins in both bakery and restaurant sectors (rejecting Null Hypothesis 1)
- The degree of sensitivity varies by industry (rejecting Null Hypothesis 2)
- Spline terms on AR(1) and AR(4) components help capture non-linearities
- Residuals generally satisfy assumptions of normality and independence
- Internal corporate factors may have stronger influence than external pricing factors

---

## 7. Limitations

- Sample size is limited to 6 firms
- Lag settings and variable selection were based on exploratory testing

---

## 8. Output Folder Contents

### 0. Load and preprocess data
- `output_processed_panel_data.xlsx`
- `output_panel_data_coverage_heatmap.png`

### 1. Visualize Data Structure
- `output_Gross_Profit_Margin_by_company_timeseries.png`
- `output_Government_Sale_Price_by_company_timeseries.png`
- `output_CPI_by_company_timeseries.png`

### 2. Multicollinearity
- `output_VIF_results.csv`

### 3. Identify Optimal Lags
- `output_lag_combination_R2_list.csv`
- `output_lag_combination_R2_heatmap.png`

### 4. Main Model
- `industry_MAE_R2_df3.png`
- `industry_metrics.csv`
- `model_summaries.pkl`
- `Bakery_summary.txt`
- `Bakery_residuals_vs_GovPrice_lag4_1000_LOWESS.png`
- `Bakery_residuals_vs_fitted_LOWESS.png`
- `Bakery_residuals_vs_CPI_lag0_LOWESS.png`
- `Bakery_residual_histogram.png`
- `Bakery_residual_ACF.png`
- `Restaurant_summary.txt`
- `Restaurant_residuals_vs_GovPrice_lag4_1000_LOWESS.png`
- `Restaurant_residuals_vs_fitted_LOWESS.png`
- `Restaurant_residuals_vs_CPI_lag0_LOWESS.png`
- `Restaurant_residual_histogram.png`
- `Restaurant_residual_ACF.png`

### 5. Coefficient Trends by Lag
- `output_gov_price_lag_coeff_trend.png`
- `output_cpi_lag_coeff_trend.png`

### 6. Interaction Term Model
- `interaction_model_summary.txt`
- `interaction_model_residuals_vs_Interaction_GovPrice_by_industry.png`
- `interaction_model_residuals_vs_GovPrice_centered_by_industry.png`
- `interaction_model_residuals_vs_CPI_lag0_by_industry.png`
- `interaction_model_residual_histogram.png`
- `interaction_model_residual_ACF.png`
- `interaction_model_metrics_comparison.png`
