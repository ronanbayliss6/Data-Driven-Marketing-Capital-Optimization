# 📊 Data-Driven Marketing Capital Optimization  

> **Capital risk detection and dynamic budget reallocation engine built to optimize a $54M digital advertising portfolio.**
> Using statistical sensitivity analysis and controlled budget redistribution, this framework improves ROAS from **4.88X to 5.21X** while reducing capital exposure to inefficient CPA zones.  
> **Simulated incremental impact: +$1.2M profit uplift with lower risk concentration.**

---

# 🧠 Business Problem

A highly profitable advertising environment (4.88X baseline ROAS) does not guarantee capital efficiency.

This project addresses four strategic questions:

1. Can a high-performing marketing portfolio still hide capital-at-risk?
2. Are rising CPAs eroding profitability despite stable engagement metrics?
3. Can we dynamically reallocate capital without damaging campaign performance?
4. Is platform efficiency structural, or driven by temporary cost inflation?

The result is a statistically validated reallocation engine designed to protect capital while increasing return efficiency.

---

# 🔎 Key Insights

## 1️⃣ Profit erosion is cost-driven, not engagement-driven  

ANOVA sensitivity testing revealed:

- Impressions, Clicks, and CTR remain statistically stable across losing days.
- Profit deterioration is strongly correlated with:
  - CPA inflation  
  - CPC inflation  
  - Excessive ad spend allocation  

**Conclusion:** Campaigns do not fail due to engagement breakdown. They fail when acquisition costs cross statistically measurable risk thresholds.

---

## 2️⃣ CPA Risk Zones Are Quantifiable  

The model identified clear probability-of-loss boundaries:

| CPA Range | Probability of Loss |
|-----------|--------------------|
| < $100    | 4.2% |
| $100–199  | 37.8% |
| $200–250  | 73.7% |
| > $250    | 100% |

- 136 campaign-days were identified as negative-yield events.
- ~$820,366 in capital exposure was classified as statistically inefficient deployment.

Instead of labeling this as “money lost,” the framework treats it as **capital deployed under high-risk conditions.**

---

# ⚙️ The Reallocation Engine

A dynamic day-by-day budget redistribution model was engineered with strict financial guardrails.

## 🔹 Tiered Capital Reduction Logic
- CPA > 100 → 40% capital reduction
- CPA 200–250 → 80% reduction
- CPA > 250 → 100% withdrawal

## 🔹 Controlled Reinjection Mechanism
- Capital is redistributed only to campaigns operating below the $100 CPA efficiency zone that exact day.
- Reinjection capped at 20% of the receiving campaign’s existing spend (prevents saturation and algorithm instability).
- Diminishing returns applied to incremental capital to avoid unrealistic scaling assumptions.

## 🔹 Capital Preservation Layer
Not all withdrawn capital is redeployed.  
~$583,585 is preserved instead of being forced into marginal environments.

---

# 📈 Financial Impact Simulation

| Metric | Baseline | Optimized |
|--------|----------|-----------|
| ROAS | 4.88X | 5.21X |
| Capital Exposure | High in volatile CPA zones | Statistically controlled |
| Estimated Incremental Profit | — | +$1.2M |

More important than the profit estimate is the structural shift:
The portfolio transitions from reactive spending to statistically bounded capital allocation.

## 📊 Executive & Risk Dashboards
![Power BI Executive Dashboard](Dashboards/Executive%20Summary.png)

![Power BI Risk Dashboard](Dashboards/Root%20Cause%20Analysis.png)
![Power BI Risk Dashboard](Dashboards/Daily%20Reallocation%20Engine.png)

---

# 🏗️ Data Architecture & Workflow

## 1️⃣ SQL Risk-Control Layer
- Raw dataset: 1,800 campaign rows / 14 fields
- Fact table schema enforcement with business logic constraints
- Prevention of mathematically impossible states (e.g., clicks > impressions)
- Analytics-ready performance view creation

## 2️⃣ Python Statistical Engine
- Defensive data auditing
- Variance profiling (Baseline vs Anomalies)
- ANOVA sensitivity testing
- Probability-of-loss modeling
- Budget reallocation simulation
- Diminishing return modeling

## 3️⃣ BI Integration
- Programmatically generated analytical CSV outputs
- Power BI dashboard visualizing:
  - Baseline vs Optimized ROAS
  - Risk concentration
  - Daily reallocation ledger
  - Capital-at-risk heatmaps

---

# 🧪 Methodological Rigor

- Dual-layer validation (SQL + Python)
- Statistical significance testing to prevent noise-driven decisions
- Isolation of 136 losing campaign-days
- Conservative scaling assumptions
- Guardrail-based capital reallocation logic

This is not a predictive ML model.  
It is a capital discipline framework built for high-confidence decision-making.

---

# 📦 Key Outputs

- `vw_performance_metrics.csv`
- `anova_results.csv`
- `136_losing_days.csv`
- `metric_variance.csv`
- `cpa_threshold_sensitivity.csv`
- `surgical_strategy_full_audit.csv

