# 32. 32. Furnaces and Combustion Chambers

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **32. furnaces and combustion chambers**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 32. Furnaces and Combustion Chambers](../../assets/chapter-32.svg)

*Figure: Fuel and air to thermal energy. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Oxygen versus excess-air ratio

![Oxygen versus excess-air ratio](../../assets/topic-curves/32-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Qualitative trend only: the exact dry O₂ relationship depends on fuel composition and combustion products; use species balances for calculations.

## Process principles

The furnace provides combustion volume and radiant heat exchange to waterwalls. Gas residence time, mixing, wall emissivity, deposits and air ingress affect performance. Furnace pressure is controlled by draft.

## Key engineering relationship

dU_gas/dt = fuel/air enthalpy + reaction heat − gas outlet enthalpy − wall heat transfer.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Use gas and wall energy inventories with a radiative heat-transfer term.

## Worked or practical exercise

Estimate wall heat absorption as a fraction of total furnace heat release.

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
