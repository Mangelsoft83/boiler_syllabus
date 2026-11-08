# 50. 50. Rankine Cycle and Plant Efficiency

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **50. rankine cycle and plant efficiency**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 50. Rankine Cycle and Plant Efficiency](../../assets/chapter-50.svg)

*Figure: Physical inputs, equipment behavior and outputs. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Performance versus load

![Performance versus load](../../assets/topic-curves/50-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** Illustrative trend only, not a plant efficiency prediction. Calculate actual performance using mass and energy balances.

## Process principles

The ideal Rankine cycle sets a reference for real plants. Pump work, turbine efficiency, heat rejection, reheat and regenerative heating determine performance. Distinguish gross, net and boiler efficiencies.

## Key engineering relationship

η_cycle = (Ẇ_turb−Ẇ_pump)/Q̇_boiler; net efficiency also subtracts auxiliaries.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Calculate heat and power balances across the complete cycle.

## Worked or practical exercise

Compare thermal efficiency before and after adding feedwater preheating.

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
