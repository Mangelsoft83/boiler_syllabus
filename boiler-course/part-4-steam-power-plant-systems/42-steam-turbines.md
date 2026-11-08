# 42. 42. Steam Turbines

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **42. steam turbines**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 42. Steam Turbines](../../assets/chapter-42.svg)

*Figure: Water and steam energy balance. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Engineering characteristic: Idealized turbine expansion and enthalpy drop

![Idealized turbine expansion and enthalpy drop](../../assets/engineering-curves/42-turbine-expansion.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

Illustrative enthalpy paths only (not a thermodynamic h-s plot). Shaft power is approximately ṁ(hin − hout) times mechanical efficiency; actual enthalpy drop depends on inlet/outlet states and turbine efficiency.


## Additional engineering illustration — Performance versus load

![Performance versus load](../../assets/topic-curves/42-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Illustrative trend only, not a plant efficiency prediction. Calculate actual performance using mass and energy balances.

## Process principles

Steam turbines convert steam enthalpy drop into shaft work. Isentropic efficiency compares actual expansion with ideal expansion to the same exhaust pressure. Wet exhaust steam may constrain operation.

## Key engineering relationship

Ẇ_turb ≈ ṁ(h_in−h_out); η_is = (h_in−h_out)/(h_in−h_out,s).

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Represent pressure-dependent steam flow, efficiency and shaft inertia where needed.

## Worked or practical exercise

Compute turbine power from a specified mass flow and enthalpy drop.

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
