# 53. 53. Pump, Valve and Flow Control

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **53. pump, valve and flow control**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 53. Pump, Valve and Flow Control](../../assets/chapter-53.svg)

*Figure: Pump head and operating point. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Pump and system operating point

![Pump and system operating point](../../assets/topic-curves/53-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** The intersection of pump and system curves defines the steady operating point. For NPSH and efficiency see the dedicated pump graphs.

## Process principles

Flow control typically adjusts valve position or pump speed. Valve authority, pump head and actuator lag influence response. A pressure disturbance changes flow even when valve opening is fixed.

## Key engineering relationship

Flow through a simple restriction: Q ∝ opening × √Δp as a rough approximation.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Connect a PI controller to a valve actuator and hydraulic network.

## Worked or practical exercise

Test whether flow recovers after a supply-pressure disturbance.

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
