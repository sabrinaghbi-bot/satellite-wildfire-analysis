## Data Pipeline Architecture

```mermaid
flowchart TD

A[NASA FIRMS Data<br>MODIS Satellite CSV] --> B[Python Data Ingestion<br>Download & Cleaning]

B --> C[(SQL Server<br>Staging Table<br>stg_fires_raw)]

C --> D[SSIS ETL Process<br>Transformations & Data Quality]

D --> E[(SQL Server<br>Curated Table<br>fires)]

E --> F[SQL Analytical Views<br>Daily trends<br>Spatial aggregation]

F --> G[Power BI Dashboard<br>Maps • Trends • KPIs]

##
This pipeline demonstrates a complete Business Intelligence workflow:
data ingestion, ETL processing, data modelling, and visualization.
