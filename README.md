# Optimization of Wind Farm Layout

## Overview

This project explores the optimization of wind turbine placement within a wind farm to maximize energy output and minimize wake losses. Three approaches are implemented and compared: a **Greedy algorithm** for generating an initial configuration, **Particle Swarm Optimization (PSO)**, and **Pattern Search**.

## Repository Structure

```
├── Wind_Farm_Greedy Initial Configuration.ipynb   # Greedy baseline layout
├── Wind_Farm_PSO.ipynb                            # Particle Swarm Optimization
├── Wind_Farm_Pattern_Search.ipynb                 # Pattern Search optimization
└── Project Report.pdf                             # Full project report
```

## Methodology

### 1. Greedy Initial Configuration
A greedy algorithm is used to generate a starting wind farm layout by placing turbines sequentially in positions that yield the greatest incremental energy gain. This serves as a baseline for comparison with the metaheuristic approaches.

### 2. Particle Swarm Optimization (PSO)
PSO is a population-based metaheuristic inspired by the collective movement of bird flocks. Each particle (candidate layout) moves through the search space guided by its own best known position and the swarm's global best, iteratively converging toward an optimal turbine arrangement.

### 3. Pattern Search
A derivative-free optimization method that searches for improvements by evaluating candidate solutions in a structured pattern around the current best solution, stepping through the layout space without requiring gradient information.

## Problem Formulation

The core challenge in wind farm layout optimization is the **wake effect** — downstream turbines sit in the low-energy wake of upstream turbines, reducing overall power output. The objective is to place *N* turbines within a bounded farm area such that total power output (or AEP) is maximized while accounting for wake interactions.

## Tools & Languages

- **Python** (Jupyter Notebooks)
- Standard scientific Python stack: `numpy`, `matplotlib`

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Amal-Thomas/Optimization-of-Wind-Farm-Layout.git
   cd Optimization-of-Wind-Farm-Layout
   ```

2. Install dependencies:
   ```bash
   pip install numpy matplotlib
   ```

3. Open the notebooks in order:
   - Start with `Wind_Farm_Greedy Initial Configuration.ipynb` to understand the baseline
   - Then explore `Wind_Farm_PSO.ipynb` and `Wind_Farm_Pattern_Search.ipynb` for the optimized layouts

## Results

See `Project Report.pdf` for a detailed writeup of results, methodology, and comparison between the three approaches.
