# 21. 21. Electric Motors, Drives and Variable Speed Control

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **21. electric motors, drives and variable speed control**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 21. Electric Motors, Drives and Variable Speed Control](../../assets/chapter-21.svg)

*Figure: Closed-loop process control. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Dynamic response and time constant

![Dynamic response and time constant](../../assets/topic-curves/21-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** A first-order response is a useful introductory approximation; real process systems can have transport delays, integrators and nonlinearities.

## Process principles

Motors and drives convert electrical power into shaft torque. Variable-frequency drives adjust pump or fan speed. Acceleration limits and rotational inertia affect transient flow and power.

## Key engineering relationship

J dω/dt = T_motor − T_load; P_shaft = Tω.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Represent speed ramp, minimum/maximum speed and optional rotational inertia.

## Worked or practical exercise

Simulate a pump ramp from 50% to 100% speed.

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
