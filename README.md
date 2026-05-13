# Telecom CDR Analytics ETL Project

End-to-end telecom Call Detail Record (CDR) analytics pipeline using a dimensional model, Informatica IICS mappings, and KPI-driven reporting dashboards.

## Project Objective

Build a production-style ETL and analytics solution that:

- Ingests and cleanses telecom CDR data
- Loads a Star Schema (Fact + Dimensions)
- Implements SCD Type 2 logic for historical tracking
- Generates business KPIs for operations and revenue monitoring

## Repository Structure

```text
project1/
|-- SQL_Scripts/
|-- IICS_Mappings_and_Workflows/
|-- Architecture_Diagrams/
|-- BI_Dashboards/
`-- README.md
```

## Technology Stack

- **ETL:** Informatica Intelligent Cloud Services (IICS)
- **Data Modeling:** Star Schema (Fact/Dimension)
- **Database:** Relational warehouse target
- **Reporting:** BI dashboards (charts and KPI views)

## Data Model (Star Schema)

Core model includes:

- `FACT_CALL`
- `DIM_CUSTOMER`
- `DIM_TIME`
- `DIM_TOWER`
- `DIM_CALL_TYPE`

### Physical Data Model

> Add your model image at `Architecture_Diagrams/physical_data_model_star_schema.png`

![Physical Data Model](Architecture_Diagrams/physical_data_model_star_schema.png)

## ETL Workflow (IICS)

Pipeline stages:

1. **Source ingestion** of CDR records
2. **Standardization and cleansing**
3. **Dimension loading** with surrogate keys
4. **SCD Type 2 processing** for historical changes
5. **Fact table loading** and KPI-ready outputs

### SCD Type 2 Mapping Logic (Router + Expression + Insert/Update)

> Add your implementation screenshot at `IICS_Mappings_and_Workflows/iics_scd2_router_expression_logic.png`

![SCD Type 2 Logic](IICS_Mappings_and_Workflows/iics_scd2_router_expression_logic.png)

### Mapping / Workflow Overview

> Add your mapping screenshot at `IICS_Mappings_and_Workflows/iics_mapping_overview.png`

![IICS Mapping Overview](IICS_Mappings_and_Workflows/iics_mapping_overview.png)

## KPI Implementation

Key KPIs produced by SQL and ETL outputs:

- Daily Call Volume
- Revenue by customer/call type/time window
- International Call Monitoring
- Additional operational alerts/notifications

Store SQL in:

- `SQL_Scripts/01_create_dimensions.sql`
- `SQL_Scripts/02_create_fact.sql`
- `SQL_Scripts/03_kpi_queries.sql`

## Dashboard Outputs

### Daily Call Volume

![Daily Call Volume](BI_Dashboards/daily_call_volume.png)

### Revenue Analysis

![Revenue Analysis](BI_Dashboards/revenue_analysis.png)

### International Call Monitoring

![International Call Monitoring](BI_Dashboards/international_call_monitoring.png)

### KPI Dashboard Overview

![KPI Dashboard](BI_Dashboards/kpi_dashboard_overview.png)

## Current Workspace Notes

This workspace already contains IICS export metadata from earlier development. You can keep those exports for traceability and additionally place recruiter-facing screenshots/scripts in the structured folders above.

## How to Run / Validate

1. Deploy or import mappings/workflows into IICS
2. Execute staging -> dimensions -> fact load sequence
3. Run KPI SQL queries
4. Validate dashboard values against SQL output

## Recruiter Highlights

- Enterprise-style folder organization
- Dimensional modeling with clear PK/FK design
- SCD Type 2 history handling in ETL
- KPI-to-dashboard traceability from source to insight
