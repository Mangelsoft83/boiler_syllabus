# 11. Dynamic Behavior During Startup and Shutdown

> **Status:** Draft — not yet reviewed. Content may contain errors or omissions.

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\

## What you will learn

- Explain the main physical function and important operating behavior of **11. dynamic behavior during startup and shutdown**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 11. Dynamic Behavior During Startup and Shutdown](../assets/chapter-67.svg)

*Figure: Dynamic simulation calculation cycle. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Dynamic response and time constant

![Dynamic response and time constant](../assets/topic-curves/67-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** A first-order response is a useful introductory approximation; real process systems can have transport delays, integrators and nonlinearities.

## Process principles

Startup and shutdown involve warming metal, establishing circulation, pressure buildup and changing steam demand. Thermal inertia causes lags and differential expansion; simplify sequences but respect operating limits.

## Key engineering relationship

C_total dT/dt ≈ Q̇_input−Q̇_output for a lumped warm-up model.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Use ramps, equipment enable states and physical heat capacities.

## Worked or practical exercise

Simulate a cold boiler warm-up with gradually increasing heat input.

**Suggested deliverable:** a calculation sheet or short explanation, a model diagram, and a trend plot of the relevant transient response. Record all assumptions.

## Review questions

1. What physical quantity is stored or transferred by this equipment or process?
2. Which input disturbance is most important for its dynamic response?
3. Which assumptions would fail outside normal operating conditions?

## References to consult

- Equipment manufacturer manuals and characteristic curves where relevant.
- IAPWS-IF97 or verified steam tables for water/steam property calculations.
- Plant P&IDs, process descriptions, operating manuals and heat/mass balances.
- Appropriate engineering standards and plant safety procedures for design or protection topics.
