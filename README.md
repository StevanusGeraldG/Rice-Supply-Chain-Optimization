# 🌾 West Java Rice Supply Chain: Efficiency & Profit Optimization Portfolio
**End-to-End Operational Research & Machine Learning Case Study across 5 Key Districts (Garut, Subang, Karawang, Indramayu, Tasikmalaya)**

---

## Executive Summary & Problem Statement
Agricultural supply chains in Indonesia often suffer from structural disconnects: **high technical operational efficiency does not guarantee economic profitability**. 

This portfolio analyzes multi-tier empirical data across 5 core nodes of the West Java rice distribution network to uncover:
1. Where technical waste and resource leakage occur.
2. Why certain nodes (e.g., Retailers) exhibit strong operational efficiency scores yet suffer structural net margin losses.
3. How Data Envelopment Analysis (DEA) paired with Linear Programming (`PuLP`) and tree-based feature attribution (`XGBoost`, `CatBoost`, `SHAP`) can prescribe optimal profit-maximizing resource allocations.

---

## Supply Chain Architecture
Farmer (n=400) ──> Miller (n=105) ──> Middlemen (n=104) ──> Wholesaler (n=104) ──> Retailer (n=102)

└──────────── Unified Analytical Layer: DEA, PuLP LP & SHAP Attribution ──────────────────────────┘

---

## Key Findings & Insights
* **The Efficiency Paradox**: Retailers achieve high technical efficiency (DEA-VRS ~0.846) yet record structural net margin losses, proving that operating "by the book" cannot rescue a fundamentally flawed unit-economics pricing/margin model.
* **Frontier Clustering**: Millers show the highest clustering at the efficiency frontier (~21.9% full efficiency, avg DEA-VRS ~0.856).
* **Primary Leakage Hotspots**: Farmers (DEA-VRS ~0.580) and Wholesalers (DEA-VRS ~0.599) represent the highest-leverage targets for input-cost reduction and physical/quality loss mitigation (precipitation decay, handling loss).

---

## Methodology Pipeline
1. **Financial Accounting Layer**: Standardized `Total Cost`, `Gross/Net Profit`, and `Margin (%)` across heterogeneous multi-tier structures.
2. **Data Envelopment Analysis (DEA)**: Implemented CRS and VRS input/output-oriented efficiency scoring via `scipy.optimize.linprog` (HiGHS solver).
3. **Prescriptive & Descriptive Modeling**: Combined `PuLP` linear optimization for allocation scenarios with tree-based feature attribution (`XGBoost`, `CatBoost`, `SHAP`) to isolate margin drivers.
