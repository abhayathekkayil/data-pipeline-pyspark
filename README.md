# data-pipeline-pyspark
Production ETL pipeline using PySpark with optimizations and Delta Lake storage

# PySpark ETL Pipeline

## Overview
Production-grade ETL pipeline using Apache Spark on Databricks. 
Processes customer transaction data with transformations, optimization, and Delta Lake storage.

## Architecture

Raw Data (CSV) → DataFrame Loading → Cleaning & Validation → Complex Transformations (joins, aggregations) → Window Functions → Optimization (partitioning, caching) → Delta Lake Storage → Analytics-ready output


## Project Structure

data-pipeline-pyspark/ ├── notebooks/ │ ├── 1_data_loading.py │ ├── 2_transformations.py │ ├── 3_window_functions.py │ ├── 4_optimization.py │ └── 5_delta_storage.py ├── data/ │ ├── input/ # Raw CSV files │ └── output/ # Processed Delta tables ├── docs/ │ ├── ARCHITECTURE.md │ └── PERFORMANCE_REPORT.md ├── README.md └── requirements.txt


## Requirements
- Databricks Runtime 12.2 LTS+
- Apache Spark 3.3+
- Python 3.10+

## How to Run
1. Upload `notebooks/` to Databricks workspace
2. Run in order: 1_data_loading → 2_transformations → 3_window_functions → 4_optimization → 5_delta_storage
3. Monitor performance metrics in each notebook

## Key Features
✓ CSV ingestion with schema validation
✓ Data cleaning & quality checks
✓ Complex joins (customer + transactions + products)
✓ Window functions (ranking, time-series)
✓ Performance optimization (repartition, cache)
✓ Delta Lake for ACID compliance

## Performance Metrics
- Data volume: 100K+ records
- Execution time (optimized): ~30 seconds
- Partitions: 4 (by date)
- Cache hit rate: 87%

## Author
Abhaya | Data Engineer | Oct 2026