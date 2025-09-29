### Mini-Case Study Title:
**22nd Century Sporting League: Optimizing Flight Logistics with Time Series**

### Overview

This project applies **time series forecasting (SARIMA)** to predict jet fuel prices and analyze team flight schedules for the fictional *22nd Century Sporting League*.

The goals were to:

1. Estimate the **maximum number of jets** the league needs to own.
2. Forecast **2102 jet fuel prices** based on 2101 data.
3. Compute the **total projected fuel spend** for all flights in 2102.

### Data

* **team_flights.csv** → Contains team flight schedules (departure/landing times, distances).
* **fuel_price.csv** → Contains daily jet fuel prices for the 2101 season.

### Methods

* **Exploratory Data Analysis** → Visualized flights in air over time.
* **Time Series Modeling** → Differenced fuel prices to achieve stationarity, identified seasonality (weekly cycle), and fit a **SARIMA(1,1,1)(1,1,1,7)** model.
* **Forecasting** → Generated daily 2102 fuel price forecasts.
* **Cost Projection** → Combined forecasted prices with flight distances to calculate **total spend**.

### Results

* 📌 **Max jets needed**: `19`.
* 📌 **Total projected 2102 fuel spend**: `$1.87M` .
* Fuel prices show both **short-term dependence** and a **weekly seasonal pattern**, confirming the value of SARIMA modeling.

### Business Impact

Efficient scheduling and fuel cost forecasting allow the league to:

* Avoid **over-purchasing jets**.
* Better **plan budgets** for transportation.
* Make **data-driven operational decisions**.

### Repository Structure

```
├── data/
│   ├── team_flights.csv
│   ├── fuel_price.csv
├── notebooks.ipynb
├── README.md
```