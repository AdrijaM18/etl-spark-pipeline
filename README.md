
# Sales Data ETL Pipeline Overview

This code performs an end-to-end ETL (Extract, Transform, Load) process on sales data stored in a CSV file using Databricks and PySpark.

## Steps

1. **Read CSV Data**
   - Loads sales data from a Unity Catalog Volume CSV file.
   - Infers schema and handles multiline records.
   - Casts the `Sales` column to double for numeric operations.

2. **Data Cleaning & Type Standardization**
   - Safely casts the `Sales` column to double using `try_cast`.
   - Removes rows with malformed or null sales values.

3. **Regional Sales Analytics**
   - Aggregates total sales by region.
   - Adds a timestamp column (`created_at`) to the results.
   - Displays the regional sales summary.
   - Writes the final sales report to a single CSV file in Unity Catalog Volume.

---
This pipeline ensures clean, reliable sales analytics and produces a ready-to-use regional sales report.
