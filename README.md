# Dashboard and Data Pipeline for data from OpenAQ
A real-time and historical air quality monitoring dashboard built with Python, Dash, Plotly, and DuckDB.

## Overview
This project is a live-updating dashboard that visualizes air quality data from OpenAQ (or other sources). It processes both real-time and historical air pollution data, stores it efficiently using DuckDB, and presents it in an interactive Dash (Plotly) dashboard.

## Key features:
1. Real-time data updates (pollutant levels, AQI, trends)
2. Historical data analysis (time-series trends, comparisons)
3. Scalable data pipeline (easily add new locations without downtime)
4. Efficient storage with DuckDB (fast querying, low overhead)
5. Interactive visualizations with Plotly & Dash

## Technologies Used

- Backend	Python, DuckDB (for lightweight SQL-based storage)
- Dashboard	Plotly, Dash (for interactive web visualizations)
- Data Tools	Pandas (data processing), DBeaver (DB management)
- Data Source	OpenAQ API
