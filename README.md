# WARP Shoe Production Optimization (Operations Research)

This repository contains a deterministic operations research project completed in Winter/Spring 2022 for MIE262 (Operations Research I) at the University of Toronto.

The project formulates and solves a large-scale production planning problem for the WARP Shoe Company using linear and integer programming in AMPL.

---

## Problem Overview

WARP Shoe faced a sudden increase in demand after a competitor exited the market. Management needed to determine how many units of each shoe type to produce in February 2006 in order to maximize total profit while respecting operational constraints.

The optimization model accounts for:

- Raw material budgets and availability  
- Machine operating time limits  
- Labor costs  
- Warehouse capacities  
- Demand forecasts and penalties for unmet demand  

The full project report appears in `OR_Supply_Chain_Report.pdf` :contentReference[oaicite:1]{index=1}.

---

## Modeling Approach

A large-scale mathematical program was developed with:

- **557 decision variables** (pairs of shoes to produce)  
- **1,353 constraints** across materials, machines, warehouses, and demand limits  
- Multiple interacting data tables imported from a modified Microsoft Access database  

### Objective

The objective maximizes monthly profit by combining:

- Revenue from shoe sales  
- Machine operating costs  
- Labor costs  
- Warehouse operating costs  
- Raw material costs  
- Penalties for unmet demand  

### Constraints

Key constraints include:

- Raw material budget and quantity limits  
- Machine work-time limits  
- Demand ceilings  
- Warehouse capacity  
- Non-negativity and integrality  

---

## Solution and Sensitivity Analysis

The original formulation was posed as an **integer program**, but was relaxed to a **linear program** to obtain solutions in reasonable time.

Key outcomes:

- Optimal projected profit: **$10,998,247**  
- 330 shoe types were not produced in the optimal plan  
- 98 raw materials were fully depleted at optimum  
- Warehouse capacity was non-binding, so purchasing extra storage was not economical  
- Increasing machine availability or raw-material budgets did not change the optimal solution  

Several alternative scenarios were tested by modifying constraints and re-solving the model.

---

## Files and Structure

- `ampl_models/`
  - `.mod` — AMPL model files  
  - `.dat` — data files  
  - `.run` — execution scripts  
  - `.out` — solver output logs  

- `OR_Supply_Chain_Report.pdf` — full technical write-up  
- `README.md`

---

## Tools and Methods

- AMPL modeling language  
- Linear and integer programming  
- Sensitivity analysis  
- Large-scale deterministic optimization  
- Database preprocessing in Microsoft Access  
