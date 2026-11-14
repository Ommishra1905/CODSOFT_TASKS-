# CODSOFT Data Analytics Internship: Tasks 1-3

| Task | Topic | Script |
|---|---|---|
| 1 | Data Cleaning & Preprocessing | `task1/task1_data_cleaning.py` |
| 2 | Exploratory Data Analysis (+ report) | `task2/task2_eda.py`, `task2/EDA_report.md` |
| 3 | Data Visualization Dashboard | `task3/task3_visualization.py` |

## Dataset

`data/raw_ecommerce_orders.csv` is a **synthetic sample dataset** created by `data/generate_dataset.py` (seeded, so it is reproducible). It is deliberately messy: missing values, 60 duplicate rows, inconsistent text (`DELHI`, ` delhi `, `upi`/`UPI`, `COD`), numbers stored as text, mixed date formats, impossible ages and a few extreme prices. To use your own data, replace the CSV and adjust the column names.

## Run

```bash
pip install pandas numpy matplotlib seaborn
python data/generate_dataset.py          # optional: regenerate raw data
python task1/task1_data_cleaning.py      # -> data/cleaned_ecommerce_orders.csv
python task2/task2_eda.py                # -> outputs/eda_findings.txt
python task3/task3_visualization.py      # -> outputs/figures/*.png
```

Run every command from the repo root, in this order.

## What each task does

**Task 1:** inspects structure, counts nulls and duplicates, removes duplicates, fixes dtypes and mixed date formats, standardises text, nulls out impossible ages, fills missing values (median / mode / category median), flags extreme price outliers, and saves the cleaned CSV.

**Task 2:** descriptive statistics, trends, correlations, IQR outlier detection, and key business questions computed with and without the flagged outliers. Findings are in `task2/EDA_report.md`.

**Task 3:** six charts (bar, line, pie, histogram, scatter, bar) plus a combined dashboard in `outputs/figures/`.

## Not done (bonus)

The Power BI / Tableau dashboard in Task 3 is not included.
