# 30. 30. Combustion Fundamentals and Calculations

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **30. combustion fundamentals and calculations**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 30. Combustion Fundamentals and Calculations](../../assets/chapter-30.svg)

*Figure: Fuel and air to thermal energy. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*



## Additional engineering illustration — Oxygen versus excess-air ratio

![Oxygen versus excess-air ratio](../../assets/topic-curves/30-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Qualitative trend only: the exact dry O₂ relationship depends on fuel composition and combustion products; use species balances for calculations.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Complete combustion consumes oxygen according to fuel composition. Excess air is supplied beyond stoichiometric demand; flue-gas oxygen is an indirect indicator. Distinguish wet and dry gas composition and LHV versus HHV.

## Key engineering relationship

For C_aH_bO_c: O₂,stoich = a + b/4 − c/2 mol per mol fuel (complete combustion); λ = actual air / stoichiometric air.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Balance species mass flows and reaction heat release before applying heat transfer.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Calculate oxygen demand and CO₂ formation for 1 kmol methane.

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
