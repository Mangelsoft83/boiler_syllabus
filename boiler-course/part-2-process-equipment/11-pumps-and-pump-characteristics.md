# 11. 11. Pumps and Pump Characteristics

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **11. pumps and pump characteristics**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 11. Pumps and Pump Characteristics](../../assets/chapter-11.svg)

*Figure: Pump head and operating point. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Engineering characteristic: Pump head and system resistance

![Pump head and system resistance](../../assets/engineering-curves/11-pump-head-system.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

At the operating point, pump head equals the required system head. Here H = 72 − 0.0035Q² and Hsys = 12 + 0.0025Q², with Q in m³/h and H in metres. The intersection is Q = 100 m³/h and H = 37 m. In PsxCad, solve the pressure/flow network using the pump characteristic and system resistance.


## Engineering characteristic: Pump efficiency and NPSH required

![Pump efficiency and NPSH required](../../assets/engineering-curves/11-pump-efficiency-npsh.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

Efficiency is shown on the left axis and NPSH required on the right axis. NPSH available must exceed NPSH required with a suitable margin according to manufacturer guidance. Do not interpret NPSHr as an allowable suction pressure in bar.


## Additional engineering illustration — Pump and system operating point

![Pump and system operating point](../../assets/topic-curves/11-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** The intersection of pump and system curves defines the steady operating point. For NPSH and efficiency see the dedicated pump graphs.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Centrifugal pumps add head; the intersection of pump and system curves determines operating flow. Speed changes shift the curve. NPSH margin helps avoid cavitation. Power depends on flow, head and efficiency.

## Key engineering relationship

H ≈ H0 − aQ² (illustrative curve); P_shaft = ρgQH/η; affinity laws: Q∝n, H∝n², P∝n³ approximately.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Use a head-versus-flow curve and a first-order speed or actuator state.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Plot pump and system curves and estimate the new operating point at reduced speed.

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
