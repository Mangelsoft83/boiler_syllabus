# 46. 46. Combustion Air and Flue Gas Systems

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **46. combustion air and flue gas systems**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 46. Combustion Air and Flue Gas Systems](../../assets/chapter-46.svg)

*Figure: Fuel and air to thermal energy. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Fan and duct operating point

![Fan and duct operating point](../../assets/topic-curves/46-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** The fan curve intersects the duct resistance curve at the operating point; gas density affects dimensional pressure and power.

## Process principles

Forced-draft and induced-draft fans establish combustion air and flue-gas flow. Dampers, air preheaters, ducts and stack draft determine furnace pressure and available oxygen.

## Key engineering relationship

ṁ_air,actual = λ ṁ_air,stoich for a defined fuel rate and air basis.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Couple fan pressure curves, duct resistance and furnace gas inventory.

## Worked or practical exercise

Simulate a fan-speed change and inspect air flow and furnace pressure.

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
