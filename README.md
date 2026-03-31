# Databricks Finance Pipeline

End-to-end data pipeline using real banking stock data, built on Databricks Free Edition.

---

## Stack
Databricks · PySpark · Delta Lake · Databricks SQL

## Architecture
```
yfinance API → Bronze (raw) → Silver (clean) → Gold (KPIs) → Dashboard
```

## What it does
- Ingests 2 years of stock data for JPM, BAC, GS, C, WFC
- Cleans and validates with PySpark
- Engineers daily return %, 7-day rolling average, and price range
- Visualizes trends in a Databricks SQL dashboard

## Notebooks
| File | Description |
|------|-------------|
| `01_bronze_ingest.py` | Download and store raw data |
| `02_silver_clean.py` | Clean and validate |
| `03_gold_transform.py` | Calculate KPIs |
| `04_analyze.py` | SQL queries and dashboard |

## How to run
1. Create a free account at [databricks.com/try-databricks](https://www.databricks.com/try-databricks)
2. Run each notebook in order
3. Data is pulled automatically via `yfinance`

---

Built with [Databricks Free Edition](https://www.databricks.com/try-databricks)
