# Telecom CDR Analytics - Ordered End-to-End Project

This repository is organized in exact implementation order:

1. Dimension tables + mapping + SQL
2. Raw table cleansing
3. Staging
4. Fact table creation
5. KPI queries
6. Dashboard reporting

## Folder Structure

```text
project1/
|-- SQL_Scripts/
|   |-- 00_raw_and_staging_tables.sql
|   |-- 01_cleansing_logic.sql
|   |-- 02_dimension_tables.sql
|   |-- 03_fact_table_creation.sql
|   `-- 04_kpi_queries.sql
|-- Project_Flow_Ordered/
|   |-- 01_Dimensions_Mapping_and_SQL/
|   |-- 02_Raw_Table_Cleansing/
|   |-- 03_Staging_Load/
|   |-- 04_Fact_Table_Creation/
|   |-- 05_KPIs/
|   `-- 06_Dashboard_Reports/
|-- IICS_Mappings_and_Workflows/
|-- Architecture_Diagrams/
|-- BI_Dashboards/
`-- README.md
```

## Step 1 - Dimension Tables + Mapping + SQL

### What is done
- Designed star schema dimensions: `DIM_CUSTOMER`, `DIM_TIME`, `DIM_TOWER`, `DIM_CALL_TYPE`
- Collected mapping/diagram screenshots for dimension flow
- Added SQL for creating all dimension tables

### SQL file
- `SQL_Scripts/02_dimension_tables.sql`

### Images
![Dimension and Mapping 1](Project_Flow_Ordered/01_Dimensions_Mapping_and_SQL/01_dimensions_mapping_and_sql_01.jpeg)
![Dimension and Mapping 2](Project_Flow_Ordered/01_Dimensions_Mapping_and_SQL/01_dimensions_mapping_and_sql_05.png)

## Step 2 - Cleansing for Raw Table

### What is done
- Cleaned mixed datatype fields from raw CDR source
- Standardized timestamps, call type, duration, revenue
- Created clean staging-ready data

### SQL file
- `SQL_Scripts/01_cleansing_logic.sql`

### Images
![Raw Cleansing 1](Project_Flow_Ordered/02_Raw_Table_Cleansing/02_raw_table_cleansing_13.jpeg)
![Raw Cleansing 2](Project_Flow_Ordered/02_Raw_Table_Cleansing/02_raw_table_cleansing_16.png)

## Step 3 - Staging Layer

### What is done
- Created raw and staging tables
- Loaded cleansed records into staging schema
- Prepared keys/columns for dimensional loading

### SQL file
- `SQL_Scripts/00_raw_and_staging_tables.sql`

### Images
![Staging 1](Project_Flow_Ordered/03_Staging_Load/03_staging_load_19.jpeg)
![Staging 2](Project_Flow_Ordered/03_Staging_Load/03_staging_load_24.jpeg)

## Step 4 - Fact Table Creation

### What is done
- Built `FACT_CALL` with FK links to all dimensions
- Added measures: duration, revenue, international flag, call count
- Ready for KPI aggregation

### SQL file
- `SQL_Scripts/03_fact_table_creation.sql`

### Images
![Fact Table 1](Project_Flow_Ordered/04_Fact_Table_Creation/04_fact_table_creation_25.jpeg)
![Fact Table 2](Project_Flow_Ordered/04_Fact_Table_Creation/04_fact_table_creation_30.jpeg)

## Step 5 - KPI Queries

### What is done
- KPI 1: Daily Call Volume
- KPI 2: Call Type Performance
- KPI 3: International Call Monitoring
- KPI 4: Revenue Data

### SQL file
- `SQL_Scripts/04_kpi_queries.sql`

### Images
![KPI 1](Project_Flow_Ordered/05_KPIs/05_kpis_31.jpeg)
![KPI 2](Project_Flow_Ordered/05_KPIs/05_kpis_36.png)

## Step 6 - Dashboard Reports

### What is done
- Built recruiter-friendly final dashboard visuals
- Included call volume, revenue, and international call insight charts

### Images
![Dashboard 1](Project_Flow_Ordered/06_Dashboard_Reports/06_dashboard_reports_40.png)
![Dashboard 2](Project_Flow_Ordered/06_Dashboard_Reports/06_dashboard_reports_43.png)

## How To Apply Images In README (Important)

1. Put image file in the correct folder, for example:
   - `Project_Flow_Ordered/04_Fact_Table_Creation/my_fact_image.png`
2. Use markdown image syntax in `README.md`:

```md
![Fact Table Mapping](Project_Flow_Ordered/04_Fact_Table_Creation/my_fact_image.png)
```

3. Commit and push. GitHub automatically renders the image in the repository front page.

## Execution Order Summary

- Run `00_raw_and_staging_tables.sql`
- Run `01_cleansing_logic.sql`
- Run `02_dimension_tables.sql`
- Run `03_fact_table_creation.sql`
- Run `04_kpi_queries.sql`

This sequence exactly matches the project flow and screenshots.
