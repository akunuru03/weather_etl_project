# Weather ETL & Visualization

This Jupyter notebook performs a complete ETL pipeline on live weather data for multiple U.S. cities, then visualizes key metrics.

## Project Overview

1. **Extract**  
   Fetches current weather data from the OpenWeatherMap API for cities: New York, Chicago, Indiana, Los Angeles, Houston, Miami.

2. **Transform**  
   Simplifies the JSON payload to the fields:  
   - city, country  
   - temperature (°C), feels_like (°C)  
   - humidity (%)  
   - description (weather)  
   - wind_speed (m/s)  

3. **Load**  
   Inserts the transformed records into a MySQL table (`weather_data`).

4. **Visualize**  
   Reads back from MySQL via SQLAlchemy into a Pandas DataFrame and produces bar-charts of temperature and humidity by city.

## Files

- `weather_etl_analysis.ipynb` – the full notebook with code, comments, and charts  
- `requirements.txt` – list of Python dependencies  

## Setup Instructions

1. **Clone the repo**

   ```bash
   git clone https://github.com/<your-username>/weather_etl_project.git
   cd weather_etl_project

