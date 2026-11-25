# Methodology

## Environment

A synthetic two-dimensional workspace of 100 m × 100 m
was generated using a 2 m grid. The environment contains
six rectangular obstacles and a 2 m safety buffer.

The start and goal coordinates are (5, 5) and (95, 95).

## Graph representation

The environment is represented as a graph. A corridor-
restricted graph is used for the optimisation procedure.
Directed arcs share physical-edge identifiers so that
disturbances are consistently applied to both directions
of a physical edge.

## Uncertainty scenarios

The experiments use uncertainty budgets Γ = 0, 1 and 2.
For positive Γ, up to Γ nominal-route edges are selected
for disturbance in each sampled scenario. Disturbance
severity is sampled uniformly from [0.5, 1.0], and the
edge-cost multiplier is 1 + 0.30 × severity.

Each uncertainty budget has two sampled scenarios and
a no-disturbance scenario.

## Two-stage optimisation

The first stage selects a nominal route. The second stage
evaluates scenario-dependent recourse routes. The
formulation uses binary route variables, flow-conservation
constraints, route-change variables and a worst-case
recourse-cost variable.

The implemented experiment uses a finite set of sampled
scenarios. It should therefore be described as a
finite-scenario robust optimisation approximation, not
as an exact solution over the full uncertainty set.

## Collision validation

The saved collision-validation records assess route
segments against the static buffered obstacles in the
two-dimensional environment.

This is geometric validation only. It does not establish
3D flight safety, dynamic-obstacle avoidance, vehicle
dynamics or real-world flight performance.

## Reproducibility

See `reproduction_instructions.md`. The saved outputs
should be interpreted together with the experiment
configuration and original optimisation source code.
