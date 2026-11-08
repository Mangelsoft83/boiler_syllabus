# 47. 47. Fuel Supply and Preparation Systems

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **47. fuel supply and preparation systems**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 47. Fuel Supply and Preparation Systems](../../assets/chapter-47.svg)

*Figure: Fuel and air to thermal energy. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Fan and duct operating point

![Fan and duct operating point](../../assets/topic-curves/47-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** The fan curve intersects the duct resistance curve at the operating point; gas density affects dimensional pressure and power.

## Process principles

Fuel systems meter and condition fuel before the burner or furnace. Coal mills dry and pulverize fuel; biomass systems manage variable moisture and particle size. Transport and storage introduce time delays.

## Key engineering relationship

ṁ_fuel,out = ṁ_fuel,in − dM_storage/dt.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Use storage inventory and first-order delivery delay for introductory simulations.

## Worked or practical exercise

Model a coal feeder and mill as two delayed fuel-flow stages.

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
