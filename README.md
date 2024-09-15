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
Dataset content:

1. Latitude
- Description: The latitude coordinate of the EV charging station.
- Usage: Helps to pinpoint the geographic location of the station on a map. Latitude ranges from -90 to 90 degrees, with positive values indicating the northern hemisphere.
2. Longitude
- Description: The longitude coordinate of the EV charging station.
- Usage: Like latitude, this helps to locate the station on a map. Longitude ranges from -180 to 180 degrees, with positive values indicating the eastern hemisphere.
3. Station_Name
- Description: The name of the EV charging station.
- Usage: Provides a human-readable identifier for the charging station, which could include brand names, location names, or station-specific identifiers.
4. ConnectionTypeID
- Description: An identifier for the type of connection used by the charging station.
- Usage: This is usually an ID referring to the type of charging connector available at the station. The actual type (e.g., Type 1, Type 2, CCS, CHAdeMO) would need to be cross-referenced with a lookup table or API documentation that maps ConnectionTypeID to the specific connection types.
5. Amps
- Description: The current capacity of the charging station in amperes (Amps).
- Usage: Indicates the electrical current that the charger can provide. Higher values typically result in faster charging if other factors (such as voltage) are also high.
6. Voltage
- Description: The voltage level of the charging station in volts (V).
- Usage: This specifies the electric potential at the charging station. Combined with Amps, it determines the power output of the charger.
7. PowerKW
- Description: The total power capacity of the charging station in kilowatts (kW).
- Usage: Indicates the maximum power the charging station can deliver to a vehicle. It is calculated as PowerKW = Amps * Voltage / 1000. Higher values generally result in faster charging.
8. Quantity
- Description: The number of charging connectors or points at the station.
- Usage: Indicates how many vehicles can charge at the station simultaneously. A higher number means more vehicles can use the station at once.
9. Comments
- Description: Free-text field for any additional information about the station.
- Usage: May include extra details such as station operational hours, pricing information, or any special notes for users.

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
