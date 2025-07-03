# Optimizing-Electric-Vehicle-Charging-Stations-and-Distributed-Generators-in-Smart-Grids
Optimizing EV Charging Stations and Distributed Generators in Smart Grids
## Overview
This repository provides source code, input datasets, and result outputs for the research work titled "Optimizing Electric Vehicle Charging Stations and Distributed Generators in Smart Grids: A Multi-Objective Meta-Heuristic Approach." This work presents a Modified Weighted Teaching-Learning Based PSO Algorithm (MWTLB-PSA) to optimally place Electric Vehicle Charging Stations (EVCS) and Distributed Generators (DGs) in a coupled distribution and road network.

## Key Features
Hybrid Optimization Algorithm (MWTLB-PSA): Combines the exploration strength of PSO with the exploitation ability of Weighted Teaching-Learning Based Optimization for superior convergence and global search capability.

Joint Planning of EVCS and DGs: Simultaneous placement considering power system efficiency and consumer travel behavior in urban road networks.

Consumer Cost Index (EVCCI): Introduces a new metric that quantifies user inconvenience in terms of distance and energy consumed to reach EVCS.

Active Power Loss Index (APLI): Measures power loss reduction after integrating EVCS and DG.

Spatially Coupled Network: Integrates IEEE 33-bus distribution system with a 25-node realistic urban road network.

##  Files Description
yaml
Copy
Edit
/scripts/ – MATLAB code used in simulation

run_MWTLB_PSA.m          : Main script for optimization
load_flow_analysis.m     : Backward/forward sweep load flow
compute_EVCCI_APLI.m     : Calculates indices and objective function
compare_algorithms.m     : Compares MWTLB-PSA with PSO & HTLBO-PSO

/data/ – Input data files

ieee_33_rdn.mat          : 33-bus RDN data
road_network_25.mat      : 25-node road network data
EV_demand_data.mat       : Demand profile and distance matrix

/results/ – Output from simulations

evcs_locations_case1.csv
evcs_dg_case3_output.csv
voltage_profiles_plot.png
loss_comparison_chart.png
economic_analysis_chart.png

## Tested Scenarios
This study tested three major planning scenarios plus a base case:

Base Case – No EVCS or DG units.

Case 1 – Only EVCS optimally placed (based on consumer travel distance).

Case 2 – EVCS with added DG units to reduce voltage drop and losses.

Case 3 – Simultaneous placement of EVCS and DGs using MWTLB-PSA.

## ⚙️ Key Specifications
Distribution system: IEEE 33-bus system

Road network: 25-node urban layout

EV population: 238 vehicles

Voltage level: 11 kV

Power base: 100 MVA

##  Results Summary
Case	Method	Active Power Loss (APL)	Minimum Voltage	EV Consumer Cost Index (EVCCI)
Case 1	MWTLB-PSA	252.71 kW	0.9048 pu	0.5425
Case 2	MWTLB-PSA	71.01 kW	0.9825 pu	0.5425
Case 3	MWTLB-PSA	57.75 kW	0.9887 pu	0.3958

##  MWTLB-PSA consistently outperformed other algorithms like PSO and HTLBO-PSO in all scenarios.

# Economic and Sensitivity Analysis
Installation cost of EVCS:

MWTLB-PSA: $2.95 million

HTLBO-PSO: $3.14 million

PSO: $3.38 million

## Sensitivity analysis confirmed optimal weights for the multi-objective function:

EVCCI weight (w₁): 0.2

APLI weight (w₂): 0.8

## Applications
This method is useful in:

Urban EV infrastructure planning

Smart grid design and control

Renewable integration scenarios

Military and critical grid resilience systems

## Limitations
Slightly higher computation time for large networks due to dual-phase optimization in each iteration.

Designed for radial distribution networks (RDN) – extension to meshed systems requires further work.


