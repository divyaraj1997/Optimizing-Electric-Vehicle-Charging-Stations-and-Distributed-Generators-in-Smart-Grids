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
