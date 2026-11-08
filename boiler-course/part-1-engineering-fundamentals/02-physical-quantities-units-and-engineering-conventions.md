# 2. 2. Physical Quantities, Units and Engineering Conventions

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **2. physical quantities, units and engineering conventions**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 2. Physical Quantities, Units and Engineering Conventions](../../assets/chapter-02.svg)

*Figure: Physical inputs, equipment behavior and outputs. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Additional engineering illustration — Flow resistance

![Flow resistance](../../assets/topic-curves/02-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Pressure loss typically grows approximately with the square of flow in turbulent flow; actual behavior depends on geometry and regime.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Use consistent SI units: kg/s for mass flow, Pa or bar for pressure, K or °C for temperature, J/kg or kJ/kg for enthalpy, and W or MW for power. Absolute and gauge pressure are not interchangeable. Temperature differences in kelvin and Celsius have equal magnitudes.

## Key engineering relationship

p_abs = p_gauge + p_atm; 1 bar = 100000 Pa; 1 MW = 1000 kJ/s.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Document units, sign conventions, normal ranges and reference conditions on every PsxCad signal.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Convert 20 t/h to kg/s and 15 bar(g) to bar(a) assuming 1.01325 bar atmospheric pressure.

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
