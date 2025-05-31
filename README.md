# Vehicle Routing Problem (VRP) with Real Coordinates

## Overview
This project implements and visualizes a solution to the classical **Vehicle Routing Problem (VRP)** using real-world geographic coordinates. It focuses on optimizing delivery routes for a fleet of vehicles while considering customer demands, vehicle capacities, and delivery time windows. The solution uses Google's OR-Tools to solve the routing problem and `geopy` to compute geographic distances.

## Project Goals
- Use real-world coordinates to simulate delivery locations
- Compute distance matrix using Haversine (geodesic) distance
- Optimize delivery routes for multiple vehicles
- Visualize the resulting delivery routes
- Enforce constraints such as:
  - Vehicle capacity limits
  - Time windows for delivery availability

## Implemented Methods
- **Distance Matrix Calculation** using the `geopy` library and real lat/lon coordinates
- **Route Optimization** using OR-Tools `RoutingModel`
- **Time Windows and Capacity Constraints** via `AddDimension`
- **Visualization** of delivery routes using `matplotlib`

## Analytical Aspects
- Customers and depot modeled with real-world coordinates
- Time and distance matrices derived from geographic distances
- Demands and delivery windows simulate practical delivery constraints
- Routes optimized across multiple vehicles to minimize total travel

## Project Files
This project is implemented in a Jupyter Notebook:

- `vehicle_routing_problem.ipynb`

Additional files generated include:

- `arxiv_coauthorship_largest_component.gexf` (from the previous project, if applicable)

## How to Run
1. Install required packages:
   ```bash
   pip install ortools geopy matplotlib
   ```

2. Open and run the notebook step-by-step (e.g., in JupyterLab or Google Colab).

3. The output includes:
   - Printed solution for each vehicle
   - Graphical visualization of all optimized routes

## Visualizations
### Vehicle Route Visualization
![VRP Route Plot](images/vrp_sample_plot.png)
Each vehicle's route is plotted using a different color, showing the order of visits based on geographic coordinates.

## Example Analyses
- Observe how vehicles split the workload among delivery points
- Assess how route efficiency is impacted by time windows and capacity
- Visualize different routing configurations by changing parameters (e.g., number of vehicles, demand)

## Notes
- The coordinates used simulate areas around New York City
- Time constraints are approximated (1 meter = 0.01 minute)
- The solution may change depending on runtime and solver strategy

## License
This project is intended for educational and academic use. Feel free to adapt and expand it for more complex logistics simulations.