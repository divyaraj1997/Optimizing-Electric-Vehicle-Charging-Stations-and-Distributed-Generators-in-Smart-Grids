# Optimizing-Electric-Vehicle-Charging-Stations-and-Distributed-Generators-in-Smart-Grids

## Manuscript Information

**Title:** Optimizing Electric Vehicle Charging Stations and Distributed Generators in Smart Grids: A Multi-Objective Meta-Heuristic Approach  
**Manuscript ID:** IEEE LATAM Submission ID: 9630  

**Authors:**  
- **Divya Bharathi R**  
  Doctoral Scholar, Department of Electrical and Electronics Engineering  
  National Institute of Technology, Tiruchirappalli, India  
  ✉️ Email: divyabharathi123@gmail.com  

- **Venkatakirthiga Murali (M’13–SM’19)**  
  Professor, Department of Electrical and Electronics Engineering  
  National Institute of Technology, Tiruchirappalli, India  
  ✉️ Email: venkatakirthiga@nitt.edu  

---

## 📘 Overview

This repository provides MATLAB source code, input datasets, and simulation results for the research work titled:  
**"Optimizing Electric Vehicle Charging Stations and Distributed Generators in Smart Grids: A Multi-Objective Meta-Heuristic Approach."**

The study proposes a **Modified Weighted Teaching-Learning Based PSO Algorithm (MWTLB-PSA)** to determine the optimal location and size of Electric Vehicle Charging Stations (EVCS) and Distributed Generators (DGs) in an integrated radial distribution and road network.

---

## 🧠 Key Features

- **Hybrid Optimization Algorithm (MWTLB-PSA):** Combines PSO and Weighted TLBO for better convergence.
- **Multi-Objective Planning:** Minimizes power loss and EV consumer travel cost (EVCCI).
- **Power-Loss Index (APLI):** Captures power system improvement post-integration.
- **Spatial Coupling:** Combines IEEE 33-bus RDN with a realistic 25-node road network.
- **Sensitivity Analysis:** Explores the impact of objective weights on the outcome.

---

## 📁 Files Description

### `/scripts/` – MATLAB Simulation Scripts
- `run_MWTLB_PSA.m` – Main execution file for running all scenarios
- `load_flow_analysis.m` – Backward/forward load flow calculation
- `compute_EVCCI_APLI.m` – Computes EVCCI and APLI values
- `compare_algorithms.m` – Compares MWTLB-PSA vs. PSO & HTLBO-PSO

### `/data/` – Input Data Files
- `ieee_33_rdn.mat` – IEEE 33-bus radial distribution system
- `road_network_25.mat` – 25-node road network graph
- `EV_demand_data.mat` – EV demand profile and distance matrix

### `/results/` – Output Files
- `evcs_locations_case1.csv` – Optimal EVCS locations (Case 1)
- `evcs_dg_case3_output.csv` – EVCS and DGs locations (Case 3)
- `voltage_profiles_plot.png` – Voltage comparison across buses
- `loss_comparison_chart.png` – Active power loss summary
- `economic_analysis_chart.png` – Cost comparison between algorithms

---

## 🔬 Tested Scenarios

- **Base Case** – No EVCS or DGs
- **Case 1** – EVCS only (based on travel cost)
- **Case 2** – DGs added after EVCS
- **Case 3** – Simultaneous placement of EVCS and DGs using MWTLB-PSA

---

## ⚙️ System Specifications

- **Distribution System:** IEEE 33-bus RDN  
- **Road Network:** 25-node urban layout  
- **EV Population:** 238 vehicles  
- **Voltage Level:** 11 kV  
- **Power Base:** 100 MVA  

---

## 📊 Results Summary

| Case     | Method      | Active Power Loss | Min Voltage | EVCCI     |
|----------|-------------|-------------------|-------------|-----------|
| Case 1   | MWTLB-PSA   | 252.71 kW         | 0.9048 pu   | 0.5425    |
| Case 2   | MWTLB-PSA   | 71.01 kW          | 0.9825 pu   | 0.5425    |
| Case 3   | MWTLB-PSA   | 57.75 kW          | 0.9887 pu   | 0.3958    |

---

## 💰 Economic and Sensitivity Analysis

- **Installation Costs:**
  - MWTLB-PSA: $2.95 million
  - HTLBO-PSO: $3.14 million
  - PSO: $3.38 million

- **Optimal Objective Weights:**
  - EVCCI Weight (w₁): 0.2
  - APLI Weight (w₂): 0.8

---

## 🧮 Step-by-Step Algorithm (By Case)

### Base Case – No EVCS or DG
1. Load IEEE 33-bus network
2. Perform load flow
3. Record APL, RPL, and minimum voltage

### Case 1 – EVCS Placement Only
1. Load distribution and road network
2. Define MOF with EVCCI & APLI
3. Initialize and run MWTLB-PSA
4. Output EVCS data, APL, EVCCI, voltage

### Case 2 – DG Placement After EVCS
1. Use EVCS results from Case 1
2. Initialize MWTLB-PSA for DG sizing
3. Update load flow
4. Record improved metrics

### Case 3 – Simultaneous EVCS and DG
1. Load all datasets
2. Set constraints (capacities, voltage)
3. Optimize mixed population
4. Output best solution with all metrics

---

## 📌 Applications

- Urban EV infrastructure planning  
- Smart grid and distribution system design  
- Renewable and EV integration studies  
- Resilient energy planning for critical networks

---

## ⚠️ Limitations

- Slightly higher runtime for large networks due to dual-phase optimization
- Designed for radial networks; extension to meshed networks requires further study

---

## 📧 Contact

For questions or support in reproducing results:

- **Divya Bharathi R** – divyabharathi123@gmail.com  
- **Prof. Venkatakirthiga Murali** – venkatakirthiga@nitt.edu  

> 📎 Note: Please ensure that all MATLAB files and datasets are placed in the appropriate folders before running the scripts.
