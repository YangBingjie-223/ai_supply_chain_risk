# AI Supply Chain Risk Analysis

## Project Overview

This project builds a data-driven supply chain risk screening framework for selected Chinese listed companies in the digital infrastructure and technology manufacturing sectors.

The project uses company-level financial and operating indicators from 2021 to 2025, constructs supply-chain-related risk features, generates annual risk scores, applies machine learning validation and clustering analysis, and finally produces a business-oriented company watchlist.

The goal is not to predict that a specific company will definitely experience supply chain disruption. Instead, the project provides a structured screening framework to identify companies that may require further due diligence.

---

## Dataset Scope

- Observation period: 2021-2025
- Number of companies: 10
- Main sample coverage: listed companies related to digital infrastructure, servers, electronic manufacturing, PCB, and ICT supply chain
- Data type: company financial and operating indicators manually collected and standardized from public annual reports

---

## Project Workflow

1. Data collection and initial inspection
2. Data cleaning and field standardization
3. Feature engineering for supply chain risk indicators
4. Annual risk scoring and company ranking
5. Machine learning validation and clustering analysis
6. Final business interpretation and watchlist construction
7. Portfolio and reporting asset generation

---

## Key Outputs

### 1. Annual Risk Ranking

In the latest year, the highest risk score company is **神州数码**, with a risk score of **64.05**.

### 2. Risk Trend Analysis

- Risk increasing companies: 2
- Risk stable companies: 5
- Risk decreasing companies: 3

### 3. Final Watchlist

The final watchlist is not based on a single-year score only. It combines:

- Latest-year risk level
- Risk score trend
- Risk score increase from the base year
- Cluster profile label as supplementary interpretation

Main watchlist companies:

- 神州数码 (000034): 最新年度风险得分位于样本前25%；风险得分呈明显上升趋势；相较基准年份风险增幅较大；聚类画像显示供应链暴露程度或经营压力需要关注
- 浪潮信息 (000977): 最新年度风险得分位于样本前25%；风险得分呈明显上升趋势；相较基准年份风险增幅较大；聚类画像显示供应链暴露程度或经营压力需要关注
- 工业富联 (601138): 最新年度风险得分位于样本前25%；聚类画像显示供应链暴露程度或经营压力需要关注

Supplementary attention companies:

- 紫光股份 (000938): 聚类画像显示供应链暴露程度或经营压力需要关注

---

## Business Interpretation

The final result suggests that companies such as **神州数码** and **浪潮信息** deserve closer attention because they show both high latest-year risk levels and clear upward risk trends.

**工业富联** is better interpreted as a comparison case: its latest-year risk level is relatively high, but its risk trend is more stable, so it should not be described as a rapidly deteriorating case.

**紫光股份**, if included, should only be treated as a supplementary observation object because its risk score did not show clear deterioration.

---

## Project Limitations

This project should be interpreted as a risk screening framework rather than a definitive prediction model.

Main limitations include:

1. The sample size is relatively small.
2. Some supply chain variables are proxy indicators due to disclosure limitations in annual reports.
3. The risk score depends on feature design and weighting assumptions.
4. Clustering results are used for profile interpretation, not direct risk classification.
5. The framework identifies companies for further review but does not replace fundamental research or field due diligence.

---

## Tools Used

- Python
- pandas
- numpy
- matplotlib
- scikit-learn
- openpyxl
- Jupyter Notebook / VS Code

---

## Repository Structure

```text
ai_supply_chain_risk/
│
├── notebooks/
│   ├── Note01_data_loading.ipynb
│   ├── Note02_data_cleaning.ipynb
│   ├── Note03_feature_engineering.ipynb
│   ├── Note04_risk_scoring.ipynb
│   ├── Note05_ml_validation.ipynb
│   ├── Note06_final_business_insights.ipynb
│   └── Note07_portfolio_report_assets.ipynb
│
├── outputs/
│   ├── note06_final_business_insights.xlsx
│   ├── note06_final_business_summary.txt
│   └── note06_charts/
│
├── github_assets/
│
├── README.md
├── requirements.txt
└── .gitignore
```