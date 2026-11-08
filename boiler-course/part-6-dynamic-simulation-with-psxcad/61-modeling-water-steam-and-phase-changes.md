# 61. 61. Modeling Water, Steam and Phase Changes

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **61. modeling water, steam and phase changes**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 61. Modeling Water, Steam and Phase Changes](../../assets/chapter-61.svg)

*Figure: Water and steam energy balance. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Additional engineering illustration — Sensible heating, boiling and superheating

![Sensible heating, boiling and superheating](../../assets/topic-curves/61-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** At constant pressure, temperature stays approximately constant during pure-water evaporation. Actual saturation temperature varies with pressure.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Steam models require a consistent property basis, often pressure and enthalpy. Crossing the saturation boundary changes temperature behavior because heat can go into evaporation rather than sensible heating.

## Key engineering relationship

u = h−pv; x = (h−h_f)/(h_g−h_f) in the two-phase region.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Call validated water/steam property routines; avoid fixed cp across phase change.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Heat a fixed-flow water stream through saturation and plot temperature and quality.

**Suggested deliverable:** a calculation sheet or short explanation, a PsxCad model diagram, and a trend plot of the relevant transient response. Record all assumptions.

## Review questions

1. What physical quantity is stored or transferred by this equipment or process?
2. Which input disturbance is most important for its dynamic response?
3. Which assumptions would fail outside normal operating conditions?

## References to consult

- Equipment manufacturer manuals and characteristic curves where relevant.
- IAPWS-IF97 or verified steam tables for water/steam property calculations.
- Plant P&IDs, process descriptions, operating manuals and heat/mass balances.
- Appropriate engineering standards and plant safety procedures for design or protection topics.
