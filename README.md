# Satellite Wildfire Analysis — MODIS (NASA FIRMS)

This project analyzes wildfire detections using satellite data from the MODIS instrument provided by NASA FIRMS (Fire Information for Resource Management System).

The goal of this project is to build an end-to-end data pipeline and explore wildfire patterns using data engineering and business intelligence tools.

---

## Project Architecture

The project implements a complete BI data pipeline:

NASA FIRMS (MODIS satellite data)
        ↓
Python data ingestion and preprocessing
        ↓
SQL Server staging database
        ↓
SSIS ETL transformations
        ↓
SQL analytical views
        ↓
Power BI interactive dashboard

---

## Technologies Used

- Python (pandas, data processing)
- SQL Server (data storage and modelling)
- SSIS – SQL Server Integration Services (ETL pipeline)
- Power BI (data visualization)
- Git & GitHub (version control)

---

## Data Source

NASA FIRMS – Fire Information for Resource Management System

Satellite instrument: MODIS

The dataset contains satellite detections of active wildfires around the world.

Typical attributes include:

- latitude
- longitude
- brightness
- acquisition date
- acquisition time
- confidence level
- fire radiative power (FRP)

---

## Repository Structure
satellite-wildfire-analysis
│
├── python
│ └── download_firms_data.py
│
├── sql
│ ├── create_tables.sql
│ └── analytics_views.sql
│
├── ssis
│ └── ETL_FIRMS_MODIS.dtsx
│
├── powerbi
│ └── wildfire_dashboard.pbix
│
├── data_sample
│ └── fires_sample.csv
│
└── docs
└── pipeline_architecture.md
---

## Pipeline Description

### 1 Data ingestion (Python)

Python scripts download and preprocess wildfire data from NASA FIRMS.

Tasks include:

- loading CSV datasets
- cleaning missing values
- preparing data for database ingestion

---

### 2 Data storage (SQL Server)

Data is first loaded into staging tables and then transformed into curated tables optimized for analytics.

---

### 3 ETL process (SSIS)

SSIS packages perform the ETL process:

- data transformation
- type conversions
- data validation
- loading into analytical tables

---

### 4 Data visualization (Power BI)

Power BI dashboards provide interactive analysis including:

- wildfire detections over time
- geographic distribution of fires
- fire intensity indicators

---

## Example Analysis

The analysis focuses on identifying:

- temporal wildfire trends
- geographic hotspots
- seasonal variations in wildfire activity

---

## Future Improvements

Possible improvements for the project:

- integrate additional satellite sources (VIIRS)
- implement automated data ingestion
- add geospatial analysis
- deploy dashboards using Power BI Service

---

## Author

Sabrina Gharbi

Junior Data Analyst — Business Intelligence
