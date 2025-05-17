# Vehicle Routing Problem (VRP) Optimization Using Ant Colony Optimization (ACO)

Summary
-------
This project implements a Vehicle Routing Problem (VRP) optimizer using Ant Colony Optimization (ACO) in Python. It aims to efficiently assign delivery orders to trucks based on maximum weight constraints and optimize the delivery routes to minimize total travel distance.

The program loads distance data between cities and order data, then assigns orders to trucks considering the maximum truck load weight. For each truck, it optimizes the delivery route using ACO, an iterative probabilistic technique inspired by the behavior of ants searching for paths between their colony and food sources.

This project includes a user-friendly Tkinter GUI where users can input maximum truck weight and receive detailed optimized routing results, including number of trucks used, assigned orders, total weight per truck, optimized routes, and the minimum total delivery distance.

Description

The Vehicle Routing Problem (VRP) is a fundamental combinatorial optimization challenge in logistics, where a fleet of vehicles must deliver goods to various locations while minimizing total travel cost and adhering to constraints such as vehicle capacities.

Input data includes:
- Distance matrix between cities (CSV file)
- Orders with source city and weight (CSV file)

This implementation focuses on:

- Reading and preparing distance and order datasets.
- Grouping orders by truck load capacity.
- Using Ant Colony Optimization (ACO) to find near-optimal routes for each truck.
- Providing a graphical interface for user interaction and result display.

The ACO algorithm simulates a colony of artificial ants that build candidate solutions based on pheromone trails and heuristic information. Over iterations, the pheromone trails are updated to reinforce better paths, guiding future ants towards optimized routes.

The algorithm groups orders into trucks based on maximum weight capacity and optimizes each truck's delivery route using ACO. 
Results include the number of trucks needed, the orders per truck, total weight, optimized routes, and minimum travel cost.

The project includes a graphical user interface (GUI) built with Tkinter for easy data input and results visualization.

---

Usage License
-------------
This software is provided under the MIT License:

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), 
to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, 
and/or sell copies of the Software, subject to the following conditions:

- The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
- THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.


Project Details
---------------
Input Files:
- Distance CSV: Columns `Source`, `Destination`, `Distance(M)` representing distances between cities.
- Orders CSV: Columns `Order_ID`, `Source`, `Weight` listing each order’s origin and weight.

Workflow:
1. Load distance and order data, build a distance matrix.
2. Group orders into trucks respecting max weight capacity.
3. For each truck, create a sub-distance matrix of the relevant cities.
4. Use Ant Colony Optimization to find optimized routes minimizing total travel cost.
5. Display number of trucks, assigned orders, total weights, routes, and cost.

---

Additional Information
----------------------
- GUI built with Tkinter for user-friendly inputs and outputs.
- ACO parameters (ants count, iterations, alpha, beta, evaporation) adjustable in the code.
- Designed for educational and small-to-medium scale VRP problems; can be extended.

---

Acknowledgments
---------------
Inspired by classical Ant Colony Optimization algorithms and Vehicle Routing Problem research literature.
