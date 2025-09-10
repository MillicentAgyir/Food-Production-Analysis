# Food Production Analysis — Environmental Impacts

A data science project to identify which **foods** and which **lifecycle stages** (farm/feed, processing, transport, packaging, retail) drive the largest environmental burdens — and to recommend the **highest-leverage actions** (dietary swaps, sourcing, logistics/packaging) that reduce impact without undermining nutrition or cost.

---

## Project Overview

We analyze a curated food-impact dataset to answer eight stakeholder-oriented business questions and produce clear, actionable recommendations for policy, procurement/retail, producers, and consumers. The analysis is implemented in Jupyter Notebooks with concise, stakeholder-friendly visuals (annotated bars; long labels auto-wrapped; numeric axes hidden where not needed).

**Key metrics**
- **GHG intensity** (kg CO₂e per kg; and optionally per 1,000 kcal / per 100 g protein)
- **Water** (freshwater withdrawals; scarcity-weighted water use)
- **Land use**
- **Lifecycle stage shares** (land-use change, animal feed, farm, processing, transport, packaging, retail)

---

## Repository Contents

- `Business & Data Understanding.ipynb` — stakeholder brief, KPIs, lean data profiling (details in appendix)
- `EDA.ipynb` — data cleaning + EDA that answers **Q1–Q8** end-to-end
- `Food_Production.csv` — source data
- `Food_Production_clean.csv` — cleaned export (produced by notebook)
- `Food_Production_negative_values.csv` — QA export for inspection (if produced)


---

## Quick Start

### 1) Create and activate a virtual environment

**Windows (PowerShell):**
```ps1
python -m venv .venv
. .venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2) Install core dependencies
```bash
pip install jupyter pandas numpy matplotlib
```

*(Optional)* Save your exact environment:
```bash
pip freeze > requirements.txt
```

### 3) Launch notebooks
```bash
jupyter lab   # or: jupyter notebook
```
Open **`Business & Data Understanding.ipynb`** first, then **`EDA.ipynb`**.

---

## Business Questions (BQ)

1. Which foods are highest/lowest impact by **GHG per kg**, per **1,000 kcal** / **100 g protein**)  
2. Which **lifecycle stages** dominate impacts for each food?  
3. **Pareto leverage**: which **8–10 foods** account for ~**80%** of total GHG, and what stage drives each?  
4. **Water risk**: which foods have extreme **scarcity-weighted water** use, and where do **withdrawals** cluster?  
5. **Dietary swaps**: which realistic substitutions (e.g., **beef → poultry/legumes**; **dairy → plant milks**) yield the largest per-serving reductions?  
6. **Transport & packaging** sensitivity: which foods have these stages **>10–15%** of total GHG?  
7. **Consistency trade-offs**: do lower-GHG foods sometimes have **higher water or land** footprints? What’s the **recommended balance**?  
8. **Scenario impact**: if a retailer shifts **X%** of sales from **high-** to **medium-impact** foods, what is the projected **GHG/water reduction**?

---

## How the Analysis Works

1. **Business & Data Understanding**  
   - Stakeholders, decisions, KPIs, and the 8 questions.  
   - Lean data profiling (types, missingness, ranges); detailed tables parked in an appendix cell.

2. **Data Cleaning (in `EDA.ipynb`)**  
   - Label standardization (short, readable names).  
   - Numeric coercion with `safe_num` helpers; handling of zeros/negatives (QA export optional).  
   - Build `ghg_total_perkg` by summing stage columns if a total is missing.  
   - Robust column detection for water/land/stages even when names vary.

3. **EDA answering Q1–Q8**  
   - Compact, annotated bar charts and stacked shares (dominant stage per food).  
   - Pareto chart (smallest set of foods hitting ~80% of GHG) with **driver stage** labels.  
   - Water risk: Top-N extremes & log-histogram of withdrawals (Q4).  
   - Swaps: per-serving reduction charts on protein/kcal bases (Q5).  
   - Transport/packaging sensitivity lists and stacked shares (Q6).  
   - Trade-off scatters (GHG vs water/land) and “balanced picks” (Q7).  
   - Scenario reallocation (High→Medium) with baseline vs scenario KPI bars (Q8).


---

## Interpreting Results (what to expect)

- **Spread**: large differences in GHG per kg across foods (often ~×200).  
- **Concentration**: a **small set (~8 foods)** typically drives **~80%** of total GHG.  
- **Driver stages**: **Farm/Feed** dominates for heavy hitters; **Transport/Packaging** matters for specific produce.  
- **Water risk**: a few foods (e.g., nuts/oils/dairy/meats) are extreme on **scarcity-weighted water**; withdrawals show a median cluster with a long high tail.  
- **Swaps**: **Beef/Lamb → Poultry/Legumes**, **Dairy milk → Plant milks**, **Shrimp → Fish/Poultry** deliver the largest per-serving reductions.  
- **Scenario**: shifting **~20%** of sales from **High→Medium** reduces portfolio **GHG & water** (see your notebook prints for exact %s based on your weights).


---

## Recommendations

- **Diet & product mix**: Prioritize the swaps above; spotlight “balanced choices” (low GHG and not high water/land) in menus/assortment.  
- **Sourcing & on-farm**: For leverage foods, work supplier side on feed, fertilizer, manure, irrigation, and land-use practices.  
- **Transport & packaging**: For items ≥10–15%, optimize mode/routes/cold chain and right-size/retune packaging.  
- **Portfolio policy**: Adopt the High→Medium shift (e.g., 20%) and track KPI reductions quarterly; run ±5–10 pp sensitivities.

---

## Reproducibility

- Export exact environment:
```bash
pip freeze > requirements.txt
```




