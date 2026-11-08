# 38. 38. Overview of the Steam-Water Cycle

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **38. overview of the steam-water cycle**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 38. Overview of the Steam-Water Cycle](../../assets/chapter-38.svg)

*Figure: Water and steam energy balance. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Flow resistance

![Flow resistance](../../assets/topic-curves/38-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Pressure loss typically grows approximately with the square of flow in turbulent flow; actual behavior depends on geometry and regime.

## Process principles

The Rankine cycle pumps condensate, heats and evaporates feedwater, expands steam through a turbine, then condenses it. Regenerative heating and reheat improve efficiency; auxiliaries consume net power.

## Key engineering relationship

Ẇ_net = Ẇ_turbine − Ẇ_pumps − Ẇ_aux; η_th = Ẇ_net/Q̇_in.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Connect boiler, turbine, condenser and feedwater equipment with consistent pressure/enthalpy ports.

## Worked or practical exercise

Draw a simplified T-s diagram of a steam power cycle.

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
