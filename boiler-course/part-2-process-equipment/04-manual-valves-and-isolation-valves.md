# 4. Manual Valves and Isolation Valves

> **Status:** Draft — not yet reviewed. Content may contain errors or omissions.

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory simulation.\

## What you will learn

- Explain the main physical function and important operating behavior of **4. manual valves and isolation valves**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 4. Manual Valves and Isolation Valves](../assets/chapter-13.svg)

*Figure: Pressure drop and valve position. The diagram highlights the main input, physical transformation, and output quantities relevant to a first model.*


## Additional engineering illustration — Inherent valve characteristics

![Inherent valve characteristics](../assets/topic-curves/13-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** These are inherent characteristics at constant differential pressure; installed characteristics change with the hydraulic system.

## Process principles

Isolation valves are intended primarily for open/closed service; check, gate, globe, ball and butterfly valves have different pressure-loss and shutoff characteristics. Valve position does not always imply proportional flow.

## Key engineering relationship

Δp = K(θ)ρv²/2, where K depends on opening θ.

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and modeling

Include travel limits, opening time and leakage only when relevant.

## Worked or practical exercise

Compare pressure drop through two fully open valves with different loss coefficients.

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
