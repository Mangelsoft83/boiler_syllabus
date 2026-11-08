# 14. 14. Control Valves and Actuators

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **14. control valves and actuators**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 14. Control Valves and Actuators](../../assets/chapter-14.svg)

*Figure: Pressure drop and valve position. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Engineering characteristic: Control-valve inherent Kv characteristics

![Control-valve inherent Kv characteristics](../../assets/engineering-curves/14-valve-kv-characteristics.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

These are **inherent** characteristics at constant pressure drop, not installed flow characteristics. For water at reference density, Q [m³/h] ≈ Kv √(Δp [bar] / SG). A real valve has a specified minimum controllable Kv, leakage, rangeability, and actuator limits; the equal-percentage idealization shown does not reach zero at shutoff.


## Engineering characteristic: Control-valve flow versus pressure drop

![Control-valve flow versus pressure drop](../../assets/engineering-curves/14-valve-flow-pressure.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

For incompressible, non-cavitating liquid, Q = Kv √(Δp/SG). At fixed opening, flow varies with the square root of pressure drop. Gas, flashing, and cavitating service require different sizing models.


## Additional engineering illustration — Inherent valve characteristics

![Inherent valve characteristics](../../assets/topic-curves/14-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** These are inherent characteristics at constant differential pressure; installed characteristics change with the hydraulic system.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Control valves regulate flow by changing effective flow area. Inherent linear and equal-percentage characteristics differ from installed characteristics once system pressure losses are included. Actuators have stroke time, limits and fail positions.

## Key engineering relationship

For incompressible non-cavitating liquid: Q = Kv√(Δp_bar/SG) in m³/h when using the standard metric Kv convention.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Model characteristic, actuator lag, saturation and actual differential pressure.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Calculate water flow for Kv = 20 and Δp = 0.25 bar; then simulate a valve stroke.

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
