# 🌾 Seasonal Agriculture Performance Analysis

**Beyond Seasonal Averages: A Risk & Archetype-Driven Analysis of Agricultural Performance**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/notebooks/Seasonal_Agriculture_Performance_Analysis.ipynb)

A data analytics project that goes beyond "average yield by season" to answer sharper,
decision-relevant questions about seasonal agricultural performance — using a composite
performance index, unsupervised clustering, season-specific driver analysis, risk-adjusted
profitability, decile benchmarking, and multivariate anomaly detection.

> Built for **VOIS AICTE Batch 2026–2027 — Major Project: Seasonal Agriculture Performance Analysis**

---

## 📋 Table of Contents

- [Problem Statement](#-problem-statement)
- [Project Description](#-project-description)
- [Why This Isn't Just Another Seasonal EDA](#-why-this-isnt-just-another-seasonal-eda)
- [Methods Used](#-methods-used)
- [End Users](#-end-users)
- [Technology Used](#-technology-used)
- [Repository Structure](#️-repository-structure)
- [How to Run](#-how-to-run)
- [Dataset](#-dataset)
- [Sample Findings](#-sample-findings)
- [Future Scope](#-future-scope)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

---

## 🎯 Problem Statement

Agricultural performance is shaped by seasonal variation in environmental conditions, farming
practices, resource availability, and market forces — but raw agricultural data on its own
doesn't reveal *how* performance changes across seasons or *what* patterns drive those
differences. This project analyzes seasonal agricultural data to uncover meaningful patterns,
trends, relationships, and variations in performance across seasons (**Kharif, Rabi, Zaid**),
going beyond simple seasonal averages to understand *why* performance differs and *what*
actionable levers exist for each season.

## 📖 Project Description

This project is a data analytics study of **4,000 farm-level records** spanning three growing
seasons, covering environmental conditions (rainfall, temperature, soil moisture/pH), resource
usage (water, fertilizer, pesticide, irrigation method), and economic outcomes (yield, revenue,
cost, profit). Rather than a generic "compare means by season" exercise, it builds a composite
performance index, discovers natural farm archetypes, tests whether profit drivers shift across
seasons, evaluates risk-adjusted profitability, benchmarks top vs. bottom performers, and flags
statistical anomalies. The output is a fully documented, reproducible Jupyter/Colab notebook
with visualizations, statistical validation, and evidence-based recommendations for seasonal
agricultural planning.

## 🔍 Why This Isn't Just Another Seasonal EDA

| # | Question |
|---|----------|
| Q1 | Which season performs best **overall**, once yield, profit margin, water efficiency, and disease risk are combined into a single composite score? |
| Q2 | Do naturally-occurring **farm archetypes** exist in the data (e.g. high-input/high-yield vs. lean & efficient vs. struggling), independent of the season label? |
| Q3 | Does **what drives profit** actually change from season to season? |
| Q4 | Is the "best" season also the **most consistent**, or does it hide more risk/volatility? |
| Q5 | What separates the **top 10%** from the **bottom 10%** of farms *within the same season*? |
| Q6 | Which farms are genuine **statistical anomalies**, worth a field-level look? |

## 🧪 Methods Used

- **Composite Farm Performance Index (FPI)** — z-scored, multi-metric performance ranking
- **K-Means clustering** — data-driven farm archetype discovery (elbow method for `k`)
- **Season-specific standardized regression** — profit-driver comparison across seasons
- **Coefficient of variation** — risk-adjusted profitability (consistency, not just averages)
- **Decile benchmarking** — top 10% vs. bottom 10% farms, within season
- **Isolation Forest** — multivariate anomaly detection
- **One-way ANOVA & Pearson correlation** — statistical significance testing
- Grouped (Season × Crop) median imputation for missing values

## 👥 End Users

- **Agricultural policymakers / government agriculture departments** — evidence-based seasonal planning, subsidy targeting, extension program design
- **Agricultural extension officers & advisors** — season-specific, data-backed input recommendations for farmers
- **Farmers and farmer cooperatives** — benchmarking against top-performing peers in the same season and region
- **Agri-tech & agri-fintech companies** (crop insurance, input suppliers) — identifying high-risk seasons/regions for better product design
- **Researchers and students** — a case study in applied seasonal/agricultural data analytics
- **NGOs and rural development organizations** — identifying underperforming archetypes or regions needing intervention

## 🛠 Technology Used

| Category | Tools |
|---|---|
| Language | Python 3 |
| Environment | Jupyter Notebook / Google Colab |
| Data handling | pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Statistics | SciPy (ANOVA, Pearson correlation) |
| Machine Learning | scikit-learn (K-Means, Isolation Forest, Linear Regression, StandardScaler) |
| Version Control | Git & GitHub |

## 🗂️ Repository Structure

```
.
├── data/
│   └── seasonal_agriculture_performance_dataset.csv   # raw dataset (4,000 farm records)
├── notebooks/
│   └── Seasonal_Agriculture_Performance_Analysis.ipynb # main analysis notebook
├── reports/                                            # (optional) exported findings / PDF write-up
├── images/                                             # (optional) exported chart images
├── requirements.txt
├── LICENSE
└── README.md
```

## 🚀 How to Run

**Option A — Google Colab (recommended, zero setup)**
1. Click the "Open in Colab" badge above.
2. Run the first cell to upload `seasonal_agriculture_performance_dataset.csv`, or mount your Drive.
3. Run all cells (`Runtime → Run all`).

**Option B — Locally**
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/Seasonal_Agriculture_Performance_Analysis.ipynb
```

## 📊 Dataset

4,000 farm-level records across 3 seasons (Kharif, Rabi, Zaid), covering environmental
conditions (rainfall, temperature, soil), resource usage (water, fertilizer, pesticide), and
economic outcomes (revenue, cost, profit). See `data/` for the raw CSV.

## 📈 Sample Findings

*(Fill this in with your own run's numbers before publishing — see Section 12 of the notebook
for the auto-generated summary.)*

- Highest overall composite performance (FPI): **[season]**
- Most consistent / lowest-risk season for profit: **[season]**
- Profit driver that varies most across seasons: **[factor]**
- Anomalous farms flagged: **[count]** ([rate]% of dataset)

## 🔮 Future Scope

- **Predictive modeling** — Random Forest / XGBoost to predict yield or profit ahead of a season using weather forecasts and planned inputs
- **Time-series expansion** — multi-year trend analysis to detect long-term climate-driven shifts
- **Geospatial analysis** — integrate GIS/satellite data (soil maps, NDVI vegetation indices) for regional recommendations
- **Real-time dashboard** — deploy findings via Streamlit / Power BI / Tableau for live querying
- **Weather API integration** — dynamic, forecast-driven driver insights
- **Causal analysis** — move from correlation to causal inference (e.g., difference-in-differences, matching)
- **Crop-recommendation engine** — extend clustering/archetypes into a recommender for optimal crop-season-region combinations
- **Mobile app integration** — package farmer-facing benchmarking into a lightweight mobile tool

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 🙏 Acknowledgements

Project brief: VOIS AICTE Batch1 2026–2027, "Major Project: Seasonal Agriculture Performance
Analysis."
