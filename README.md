# Vehicle Routing Problem (VRP) and Geographic Network Analysis

## Overview
This project demonstrates how to solve the Vehicle Routing Problem (VRP) for a single vehicle tasked with visiting 10 points scattered around Cairo. The objective is to find the optimal route with the least cost and time. This is achieved using Python libraries for geographic network analysis and optimization.

## Key Steps in the Project:

1. **Data Preparation**:
   - **Points**: 18 points in total, with the starting point at coordinates (30.13, 31.35) marked in red.
   - The other points are marked in black.

2. **Network Creation**:
   - The code generates a traffic network around the starting point using the OSMNx library within a 25 km radius.
   - The network includes only roads accessible to vehicles.

3. **Shortest Path Calculation**:
   - The `NetworkX` library’s Dijkstra algorithm is used to compute the shortest path between the points.
   - Dijkstra’s algorithm is a widely used method for finding the shortest paths in a graph, useful in network analysis.

4. **Optimization**:
   - After gathering distance and travel time data, the `ORTools` library from Google is used to solve the routing problem using the `PATH_CHEAPEST_ARC` algorithm.

5. **Route Visualization**:
   - The resulting optimal route is displayed on an interactive map using the `Folium` library.
   - A time distribution of the travel times between the points is also created to identify the fastest and slowest routes.

## Results:

- **Optimal route for the vehicle**:
  - Route: [0, 4, 1, 9, 8, 3, 2, 6, 5, 7]
  - **Total Distance**: 3.32 km
  - **Points Visited**: 10

## How to Run:

1. Clone the repository:
   ```bash
   git clone [repository-url]
