# 52. 52. Control Loops and PID Controllers

> **Audience:** Beginning simulation engineers  
> **Scope:** Process understanding, practical engineering calculations and introductory PsxCad simulation.  
> **Status:** Foundation lesson; values and simplified models must be checked against plant-specific data before use.

## What you will learn

- Explain the main physical function and important operating behavior of **52. control loops and pid controllers**.
- Apply a useful engineering relationship with consistent units and assumptions.
- Identify the state variables, boundary conditions and inputs needed for a simplified dynamic model.


## Process illustration

![Conceptual process diagram for 52. Control Loops and PID Controllers](../../assets/chapter-52.svg)

*Figure: Closed-loop process control. The diagram highlights the main input, physical transformation, and output quantities relevant to a first PsxCad model.*


## Engineering characteristic: Illustrative controlled-process step response

![Illustrative controlled-process step response](../../assets/engineering-curves/52-pid-step.png)

*Illustrative teaching curves, not manufacturer or plant performance data.*

The curve is an example of transient response, not the response of a specified PID tuning. Compare overshoot, settling time and steady-state error when testing PsxCad control loops.


## Additional engineering illustration — Dynamic response and time constant

![Dynamic response and time constant](../../assets/topic-curves/52-engineering-characteristic.svg)

*Illustrative teaching graph, not manufacturer data or a validated plant characteristic.*

**Interpretation:** A first-order response is a useful introductory approximation; real process systems can have transport delays, integrators and nonlinearities.

**PsxCad exercise:** Vary one physical input or model parameter, record the response, and compare the resulting curve with the expected trend. Document the units, boundary conditions, and validity range.

## Process principles

Feedback control compares measured process variable with setpoint. Proportional action responds to error, integral action removes steady offset and derivative action anticipates change but amplifies noise. Saturation can cause integral windup.

## Key engineering relationship

u = Kp[e + (1/Ti)∫e dt + Td de/dt] (one common ideal PID form).

**Engineering note:** Check the units and validity range of this relationship. It is an introductory model or calculation, not a substitute for equipment manufacturer data, validated steam properties or detailed design standards.

## Dynamic behavior and PsxCad model

Implement a PI controller with output limits and anti-windup.

A practical PsxCad exercise should define:

1. **Inputs:** relevant flow, pressure, temperature, enthalpy, heat, command or operating conditions.
2. **Parameters:** physical geometry, efficiency, heat capacity, coefficients, limits and characteristic curves as applicable.
3. **States:** stored mass, stored energy, wall temperature, speed, actuator position or controller integral where applicable.
4. **Outputs:** observable process quantities, calculated duty or power, and diagnostic conservation residuals.
5. **Tests:** nominal steady state, one controlled input change, and checks for physical bounds and conservation.

## Worked or practical exercise

Tune a PI loop for a first-order tank-level process and test a setpoint step.

**Suggested deliverable:** a calculation sheet or short explanation, a PsxCad model diagram, and a trend plot of the relevant transient response. Record all assumptions.

## Review questions

1. What physical quantity is stored or transferred by this equipment or process?
2. Which input disturbance is most important for its dynamic response?
3. Which assumptions would fail outside normal operating conditions?

## References to consult

- Equipment manufacturer manuals and characteristic curves where relevant.
- IAPWS-IF97 or verified steam tables for water/steam property calculations.
- Plant P&IDs, process descriptions, operating manuals and heat/mass balances.
- Appropriate engineering standards and plant safety procedures for design or protection topics.
