# UAV Robust Path Planning

## Overview

This repository contains experimental materials for a
finite-scenario, two-stage robust optimisation framework
for single-UAV path planning in a synthetic two-dimensional
environment with static obstacles.

## Repository contents

- `data/`: environment parameters and graph/route data.
- `results/`: optimisation outputs and validation records.
- `results/figures/`: generated experimental figures.
- `results/recourse_routes/`: scenario-specific route files.
- `documentation/`: methodology and reproduction guidance.
- `UAV_Robust_Optimisation.ipynb`: results inspection notebook.

## Experimental environment

The synthetic workspace is 100 m × 100 m, with a 2 m grid,
six rectangular obstacles and a 2 m safety buffer.

The experiments use uncertainty budgets Γ = 0, 1 and 2.
The reported scenario results are finite-scenario experiments,
not an exhaustive solution over every possible uncertainty
realisation.

## Software

The optimisation experiments used Python, SciPy 1.16.3
and the HiGHS MILP solver.

## Important scope limitation

The environment is synthetic. The results do not constitute
real-world UAV flight testing, 3D collision validation or
hardware validation.

The notebook supplied here inspects the saved experimental
outputs. The original optimisation implementation must also
be included to enable independent rerunning of the MILP.

## Data availability

The repository contains computationally generated
experimental data and associated result files.
