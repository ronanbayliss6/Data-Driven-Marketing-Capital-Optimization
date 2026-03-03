# 📊 Data-Driven-Marketing-Capital-Optimization

> **Data-driven marketing optimization framework that analyzes ROAS, profitability, and campaign efficiency to identify underperforming spend. Built with Python and SQL, the reallocation engine simulates a $1.2M profit optimization and improves ROAS from 4.88X to 5.21X.**

## 📌 Executive Summary
This project identifies capital-at-risk within a global digital advertising portfolio ($54M Revenue / 4.88X baseline ROAS) and algorithmically reallocates wasted spend to high-performing assets using strict financial guardrails. By employing a micro-simulation engine and ANOVA sensitivity testing, the final model demonstrates significant profit optimization while strictly decreasing total capital exposure.

## 🛠️ The Tech Stack & Pipeline
This project features a complete end-to-end data pipeline:
* **Data Storage:** SQLite (`global_ad_ops_warehouse.db`) storing 1,800 global operational days.
* **Data Extraction & Cleaning:** Python (Pandas, NumPy) to handle missing revenue columns, logical grain analysis, and data quality checks.
* **Statistical Analysis:** Python (SciPy) for ANOVA testing to determine campaign sensitivity.
* **Business Visualization:** Power BI (`Data Analytics Marketing.pbix`) for executive-level dashboarding.

## 📈 Executive Dashboard
![Power BI Executive Dashboard](Captura%20de%20pantalla%202026-03-02%20084516.png)

## 🎯 Risk Management & Key Findings
To uncover hidden daily inefficiencies across Google Ads, Meta Ads, and TikTok Ads, this project quantified variance and risk at a granular level:
* **CPA Profitability Thresholds:** Identified the exact Cost Per Acquisition (CPA) boundaries for each platform where campaigns cross from profitable returns into negative expected value.
* **Probability of Loss:** Modeled the statistical probability of a campaign losing capital under specific daily conditions. By treating campaign variance as a measurable metric, the engine automatically cuts funding to channels that exceed acceptable risk limits.
* **The Core Mechanism:** We demonstrate that top-of-funnel campaign efficiency (clicks, impressions, and CTR) remains stable, but rising CPAs push capital into negative-yield risk zones. The engine mitigates this by dynamically shifting budget to more cost-effective daily alternatives.

![Power BI Risk Dashboard]()

## ⚙️ Methodology & Engine Mechanics
1. **Defensive Data Auditing:** Custom Python functions (`check_data_quality`) were built to differentiate between logical overlaps and technical duplicates, ensuring absolute data integrity before any financial models were applied.
2. **ANOVA Sensitivity Testing:** Conducted statistical variance tests to ensure that the performance differences between channels were statistically significant, preventing the algorithm from chasing random noise.
3. **Surgical Reallocation Algorithm:** Engineered a script that shifts capital away from mathematically inefficient campaigns into high-yield avenues. The algorithm is bounded by strict financial guardrails to prevent over-allocation and diminishing returns.

## 📦 Key Outputs & Deliverables
The Python engine programmatically generates clean data assets for downstream use:
* `surgical_strategy_full_audit.csv`: The optimized daily reallocation ledger.
* `vw_performance_metrics.csv`: The cleaned, validated baseline data ready for BI ingestion.

## 📁 Repository Structure
```text
├── data/
│   ├── global_ad_ops_warehouse.db           # Raw SQLite database
│   └── global_ads_performance_dataset.csv   # Exported raw metrics
├── notebooks/
│   └── marketing_budget_optimization_audit.ipynb  # Core engine & Python logic
├── dashboards/
│   └── Data Analytics Marketing.pbix        # Interactive Power BI dashboard
└── README.md
