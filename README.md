# 🚖 NYC Yellow Taxi Data Analysis with DuckDB and Pandas

This project explores the performance and analytical capabilities of [DuckDB](https://duckdb.org/) by:

- 📊 Performing **descriptive analytics** on NYC Yellow Taxi trip data using SQL
- ⚡ Comparing the performance of **DuckDB** vs. **Pandas** in loading and aggregating large datasets

---

## 📁 Project Structure


---

## 📦 Dataset

- **Name:** NYC Yellow Taxi Trip Records (January 2023)
- **Format:** Parquet
- **Size:** ~500MB
- **Source:** [NYC TLC Trip Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

This dataset includes fields such as pickup datetime, dropoff datetime, passenger count, trip distance, fare amount, and payment type.

---

## 🧪 Notebooks

### 1. `base/describe_analyses.ipynb`

Descriptive statistics using DuckDB:

- Total number of rides
- Passenger count distribution
- Trip distance statistics (min, max, average, std)
- Fare amount distribution and median
- Trips per day and hour
- Payment method distribution
- Outlier detection for trip distances

All queries are executed directly on the Parquet file using SQL in DuckDB — no in-memory loading needed.

---

### 2. `teste_performance.ipynb`

Performance comparison notebook:

- Loads the same `.parquet` file using both **Pandas** and **DuckDB**
- Executes identical `group by` and `aggregation` queries
- Measures:
  - ⏱ Execution time
  - 💾 Memory usage (via `memory_profiler`)
- Conclusion: DuckDB showed faster execution and significantly lower memory usage

---

## ✅ Requirements

Install required libraries:

```bash
pip install duckdb pandas memory-profiler
