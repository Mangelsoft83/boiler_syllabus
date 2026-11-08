# 16. Boiler Efficiency and Heat Balances

> **Status:** Draft — not yet reviewed. Content may contain errors or omissions.

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\

## What you will learn

- Explain the main physical function and important operating behavior of **16. boiler efficiency and heat balances**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 16. Boiler Efficiency and Heat Balances](../assets/chapter-37.svg)

*Figure: Convection, conduction and thermal storage. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Oxygen versus excess-air ratio

![Oxygen versus excess-air ratio](../assets/topic-curves/37-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Qualitative trend only: the exact dry O₂ relationship depends on fuel composition and combustion products; use species balances for calculations.

## Process principles

Boiler efficiency compares useful heat delivered to working fluid against fuel energy input. Direct and indirect methods must use consistent fuel basis, boundaries and measurement conditions. Stack, radiation and unburned-fuel losses matter.

## Key engineering relationship

η_boiler,direct = useful steam-side heat / (ṁ_fuel LHV).

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Report energy residual and efficiency independently to catch model errors.

## Worked or practical exercise

Calculate direct efficiency from fuel flow, LHV, steam flow and enthalpy rise.

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
