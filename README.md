# Pharma Clinical Trials Intelligence with Snowflake

## Overview

This project demonstrates an end-to-end data analytics pipeline built on Snowflake for the pharmaceutical domain. It ingests public clinical trial data, transforms it using Snowpark, and exposes business-ready metrics for analysis.

The goal is to simulate how a pharmaceutical company can centralize clinical trial data and enable analytics for decision-making.

---

### Business Problem

Pharmaceutical companies need to monitor clinical trials across multiple dimensions such as:

therapeutic areas
trial phases
sponsors
recruitment status

However, data is often fragmented and not readily accessible for analytics.

This project addresses that challenge by building a centralized analytics layer in Snowflake.

---

### Architecture

### Pipeline Overview:

- Data ingestion from ClinicalTrials.gov API
- Raw data storage in Snowflake
- Data transformation using Snowpark (Python)
- KPI layer creation (fact tables + aggregations)
- Dynamic Tables for automated updates
- Semantic layer for business-friendly querying
  
## Tech Stack
1. Snowflake (Data Warehouse)
2. Snowpark (Python API)
3. Python (data ingestion & transformation)
4. Pandas (initial processing)
5. SQL (analytics layer)
6. Data Source
7. ClinicalTrials.gov (public API)
   
## Data Model
1. Raw Layer
```RAW_CLINICAL_TRIALS```
2. Curated Layer
```FACT_CLINICAL_TRIALS```
3. KPI Layer
``` KPI_TRIALS_BY_PHASE_STATUS```
``` PHARMA_TRIAL_KPIS ``` (Dynamic Table)
   
## Example Business Questions
- Which trial phases have the highest number of studies?
- Which sponsors are most active in oncology?
- What is the average enrollment by trial phase?
- How many trials are currently recruiting?

## Key Features
End-to-end pipeline using Snowflake as the central platform
Snowpark transformations for scalable data processing
Dynamic Tables for automated KPI updates
Designed for business consumption via semantic layer

## How to Run
Configure Snowflake credentials (use environment variables)
## Run the notebook:
1. Data ingestion
2. Data transformation
3. KPI generation
4. Execute SQL scripts in Snowsight for Dynamic Tables
5. Query results using SQL or semantic view

## This project demonstrates:

Building production-style data pipelines in Snowflake
Designing analytical data models (fact + KPI layers)
Using Snowpark for scalable transformations
Translating business problems into data solutions
Future Improvements
Integrate adverse event data (openFDA)
Add machine learning models (trial success prediction)
Build a Streamlit dashboard
Enable natural language queries using Snowflake Cortex

## Author

Juan Enciso
Data Scientist | MLOps Engineer
