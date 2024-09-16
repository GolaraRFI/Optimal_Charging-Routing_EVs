# Optimal Charging and Routing of Electric Vehicles (EVs)

### Project Overview

This project focuses on optimizing both the routing and charging processes for Electric Vehicles (EVs) to enhance travel efficiency and convenience. By leveraging data on road conditions, battery status, and charging infrastructure, the system provides intelligent routing solutions that balance travel time, charging needs, and cost-efficiency.

### Objective

- Routing Optimization: Identify the most efficient route for EVs by considering key factors such as distance, traffic conditions, and road quality to minimize travel time and energy consumption.
- Charging Optimization: Determine optimal charging stops along the route to minimize charging time, reduce costs, and ensure vehicles maintain sufficient battery levels throughout the journey.

### Dataset

EV Charging Stations Dataset (Open Charge Map):
https://openchargemap.org/site/develop/api

Road Network and Routing Data (OpenStreetMap):
https://www.openstreetmap.org/

Traffic Data:
HERE Traffic API: https://developer.here.com/products/traffic

OpenTraffic: https://opentraffic.io/

EV Specifications (EPA Vehicle Data):
https://www.fueleconomy.gov/feg/ws/index.shtml

The dataset contains detailed information about EV charging stations, including their location (Latitude, Longitude), type of connection (ConnectionTypeID), and electrical characteristics (Amps, Voltage, PowerKW).

## Dataset Content

| **Field Name**     | **Description**                                                                                                                 | **Usage**                                                                                                                      |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Latitude**        | The latitude coordinate of the EV charging station.                                                                             | Helps to pinpoint the geographic location of the station on a map. Latitude ranges from -90 to 90 degrees.                    |
| **Longitude**       | The longitude coordinate of the EV charging station.                                                                            | Locates the station on a map. Longitude ranges from -180 to 180 degrees.                                                      |
| **Station_Name**    | The name of the EV charging station.                                                                                            | Provides a human-readable identifier for the charging station (e.g., brand names, location names, or specific identifiers).    |
| **ConnectionTypeID**| An identifier for the type of connection used by the charging station.                                                          | Refers to the type of charging connector (e.g., Type 1, Type 2, CCS, CHAdeMO). Requires cross-referencing with an ID table.    |
| **Amps**            | The current capacity of the charging station in amperes (Amps).                                                                 | Indicates the electrical current that the charger can provide. Higher values typically result in faster charging.              |
| **Voltage**         | The voltage level of the charging station in volts (V).                                                                         | Specifies the electric potential. Combined with Amps, it determines the power output of the charger.                          |
| **PowerKW**         | The total power capacity of the charging station in kilowatts (kW).                                                             | Indicates the maximum power the charging station can deliver. PowerKW = Amps * Voltage / 1000. Higher values result in faster charging. |
| **Quantity**        | The number of charging connectors or points at the station.                                                                     | Indicates how many vehicles can charge at the station simultaneously.                                                         |
| **Comments**        | Free-text field for any additional information about the station.                                                               | May include details such as station operational hours, pricing information, or special notes for users.                       |


## Installation

To run this project, you'll need to install the following Python libraries:

```bash
pip install osmnx requests pandas geopy networkx folium pulp shapely
```

### Key Features

- Real-Time and Historical Traffic Data Integration: Incorporates traffic data to suggest routes that minimize delays and improve overall travel efficiency.
- Battery Level Monitoring and Prediction: Tracks current battery levels and predicts future energy consumption, ensuring that vehicles don’t run out of charge mid-journey.
- Charging Station Optimization: Identifies the best charging stations based on availability, pricing, and proximity to the route, allowing users to balance between time and cost.
- User Preferences: Customizes the route and charging recommendations based on user priorities, such as preferring the fastest route or the most economical charging options.  
