# 31. 31. Burners and Combustion Equipment

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **31. burners and combustion equipment**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 31. Burners and Combustion Equipment](../../assets/chapter-31.svg)

*Figure: Fuel and air to thermal energy. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Oxygen versus excess-air ratio

![Oxygen versus excess-air ratio](../../assets/topic-curves/31-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Qualitative trend only: the exact dry O₂ relationship depends on fuel composition and combustion products; use species balances for calculations.

## Process principles

Burners mix fuel and oxidant, stabilize flames and distribute heat. Burner turndown, ignition, flame monitoring and air staging influence operability and emissions. Fuel and air response times need not match.

## Key engineering relationship

Q̇_combustion ≈ η_comb ṁ_fuel LHV.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Use separate fuel and air dynamics and a bounded combustion-efficiency assumption.

## Worked or practical exercise

Simulate a fuel-flow increase with delayed combustion-air response.

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
