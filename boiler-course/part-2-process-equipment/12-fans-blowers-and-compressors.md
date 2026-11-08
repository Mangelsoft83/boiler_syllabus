# 12. 12. Fans, Blowers and Compressors

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **12. fans, blowers and compressors**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 12. Fans, Blowers and Compressors](../../assets/chapter-12.svg)

*Figure: Physical inputs, equipment behavior and outputs. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Engineering characteristic: Fan pressure and duct resistance

![Fan pressure and duct resistance](../../assets/engineering-curves/12-fan-pressure-flow.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

Illustrative curves show that the fan operating point occurs where fan pressure rise equals duct pressure loss. Density and speed must be handled consistently.


## Additional engineering illustration — Fan and duct operating point

![Fan and duct operating point](../../assets/topic-curves/12-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** The fan curve intersects the duct resistance curve at the operating point; gas density affects dimensional pressure and power.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Fans move large volumes of low-pressure gas; compressors generate higher pressure ratios. Density varies with temperature and pressure. Fan operating points depend on duct resistance, dampers and speed.

## Key engineering relationship

Δp_system ≈ KQ²; fan affinity approximations at similar conditions: Q∝n, Δp∝n².

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Use gas density and a pressure-rise characteristic rather than fixed flow.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Simulate an induced-draft fan speed step and furnace-pressure response.

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
