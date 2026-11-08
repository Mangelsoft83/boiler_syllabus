# 7. 7. Heat Transfer: Conduction, Convection and Radiation

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **7. heat transfer: conduction, convection and radiation**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 7. Heat Transfer: Conduction, Convection and Radiation](../../assets/chapter-07.svg)

*Figure: Convection, conduction and thermal storage. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Engineering characteristic: Convection and radiation versus temperature

![Convection and radiation versus temperature](../../assets/engineering-curves/07-heat-transfer-modes.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

Illustrative comparison for area A = 1 m², ambient/surroundings at 20 °C, h = 20 W/(m²·K), emissivity ε = 0.8. Radiation uses absolute temperatures in kelvin. Conduction through the wall adds another thermal resistance.


## Additional engineering illustration — Illustrative temperature profiles

![Illustrative temperature profiles](../../assets/topic-curves/07-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Temperature profiles depend on flow arrangement, phase change, heat capacity rates and thermal resistances. This is a simplified co-current example.

## Process principles

Conduction transfers heat through solids; convection exchanges heat between a surface and fluid; radiation exchanges electromagnetic energy between surfaces. Boiler furnaces are strongly radiative, while economizers are predominantly convective. Metal thermal mass delays outlet-temperature response.

## Key engineering relationship

Q̇_cond = kAΔT/L; Q̇_conv = hA(T_s−T_f); Q̇_rad = εσA(T_s⁴−T_sur⁴) for a simplified large-surroundings case, with T in K.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Create separate gas, metal and water nodes, connected by heat-transfer terms.

## Worked or practical exercise

Compare convection and radiation heat fluxes at a specified wall temperature and emissivity.

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
