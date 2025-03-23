# Weather ETL Pipeline with Apache Airflow

This project is an **ETL pipeline** built with **Apache Airflow** that extracts weather data from the **Open-Meteo API**, transforms it, and loads it into a **PostgreSQL database**.

## Features
- **Extract**: Fetches weather data for a specific location (London) using Airflow's `HttpHook`.
- **Transform**: Processes and structures the weather data.
- **Load**: Stores the transformed data into a PostgreSQL database.

## Prerequisites
- Apache Airflow installed
- PostgreSQL database set up
- Airflow connections configured:
  - `open_meteo_api` for API requests
  - `postgres_default` for PostgreSQL

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/weather-etl-pipeline.git
   cd weather-etl-pipeline
   ```
2. Ensure Airflow is running:
   ```bash
   airflow scheduler & airflow webserver
   ```
3. Add the DAG to your Airflow DAGs folder.
4. Start the DAG in the Airflow UI through this:
   ```bash
   astro dev start
   ```

## Configuration
- Modify `LATITUDE` and `LONGITUDE` variables in the DAG to fetch data for a different location.
- Ensure PostgreSQL is accessible and properly configured in Airflow connections.

## Usage
Once the DAG is running, it will:
1. Fetch weather data from Open-Meteo.
2. Process the data.
3. Store it in PostgreSQL.


