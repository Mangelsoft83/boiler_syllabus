# 6. Measurement Instruments and Sensors

> **Status:** Draft — not yet reviewed. Content may contain errors or omissions.

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\

## What you will learn

- Explain the main physical function and important operating behavior of **6. measurement instruments and sensors**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 6. Measurement Instruments and Sensors](../assets/chapter-15.svg)

*Figure: From physical state to measured signal. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Inherent valve characteristics

![Inherent valve characteristics](../assets/topic-curves/15-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** These are inherent characteristics at constant differential pressure; installed characteristics change with the hydraulic system.

## Process principles

Pressure transmitters, thermocouples/RTDs, differential-pressure flowmeters and level instruments have different physical principles. Measurements may include lag, noise, bias, range limits and filtering.

## Key engineering relationship

First-order sensor: τ dy/dt = x − y; orifice flow is approximately proportional to √Δp under fixed fluid conditions.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Keep true process variables separate from measured signals.

## Worked or practical exercise

Apply a step to a temperature sensor with a 10 s time constant and plot its output.

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
