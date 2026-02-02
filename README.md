# Data Engineering Homework Repository

## 📚 Overview

This repository contains homework assignments and solutions for the Data Engineering course, focusing on NYC Taxi data analysis using modern data engineering tools and practices.

## 🎯 Assignments Completed

### NYC Taxi Data Quiz
- **File Size Analysis**: Calculated file sizes using shell commands
- **Data Aggregation**: Analyzed Yellow and Green taxi trips for 2020
- **Time-based Queries**: Extracted March 2021 trip counts
- **Timezone Configuration**: Implemented proper timezone handling in Kestra

**See detailed answers:** [nyc-taxi-quiz-answers.md](answers-notes.md)

## 🛠️ Technologies Used

- **Python**: Data processing and analysis
  - `pandas`: Data manipulation
  - `duckdb`: SQL queries on parquet files
- **Kestra**: Workflow orchestration
- **Shell Scripts**: File operations and automation
- **Parquet**: Columnar data format

## 📊 Key Findings

| Dataset | Time Period | Trip Count |
|---------|-------------|------------|
| Yellow Taxi | All of 2020 | 24,648,499 |
| Green Taxi | All of 2020 | 1,734,051 |
| Yellow Taxi | March 2021 | 1,925,152 |

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas duckdb pyarrow
```

### Running the Scripts
**docker container up:**
```bash
docker-compose up
```

**Yellow Taxi 2020 Analysis:**
```bash
python scripts/count_yellow_2020.py
```

**Green Taxi 2020 Analysis:**
```bash
python scripts/count_green_2020.py
```

**March 2021 Analysis:**
```bash
python scripts/yellow_taxi_trips.py
```

## 📝 Data Sources

All data is sourced from the NYC Taxi & Limousine Commission:
- Base URL: `https://d37ci6vzurychx.cloudfront.net/trip-data/`
- Format: Parquet files
- Naming convention: `{color}_tripdata_{YYYY-MM}.parquet`

## 🔧 Kestra Configuration

To run Kestra workflows with proper timezone:

```yaml
timezone: "America/New_York"
```

This ensures all scheduled tasks run according to New York time, including automatic DST adjustments.

## 📌 Notes

- File sizes are reported in MiB (Mebibytes)
- All trip counts are based on row counts in parquet files
- Data covers Yellow and Green taxi trips only (excludes FHV, FHVHV)

## 👤 Author

Noran Salm

## 📅 Last Updated

February 2026

---

**Happy Data Engineering! 🚖📊**
