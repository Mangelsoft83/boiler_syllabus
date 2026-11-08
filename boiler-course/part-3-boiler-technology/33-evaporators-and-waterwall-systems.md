# 33. 33. Evaporators and Waterwall Systems

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **33. evaporators and waterwall systems**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 33. Evaporators and Waterwall Systems](../../assets/chapter-33.svg)

*Figure: Water and steam energy balance. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Sensible heating, boiling and superheating

![Sensible heating, boiling and superheating](../../assets/topic-curves/33-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** At constant pressure, temperature stays approximately constant during pure-water evaporation. Actual saturation temperature varies with pressure.

## Process principles

Waterwalls absorb furnace heat and generate steam. Two-phase flow and metal temperature depend on pressure, circulation and heat flux. A simplified model may track bulk enthalpy and a wall temperature state.

## Key engineering relationship

Q̇ = ṁ(h_out−h_in) in steady state; C_wall dT_wall/dt = Q̇_in−Q̇_out.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Connect furnace radiation to wall metal, then to circulating fluid.

## Worked or practical exercise

Simulate waterwall outlet enthalpy after a 10% heat-flux step.

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
