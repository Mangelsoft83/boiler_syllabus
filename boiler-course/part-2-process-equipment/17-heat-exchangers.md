# 17. Heat Exchangers

> **Audience:** Beginning simulation engineers  
> **Scope:** Flow arrangements, heat balances, flow-dependent heat transfer and simplified PsxCad modeling.  
> **Note:** Examples are illustrative; use validated design data for real equipment.

## 17.1 Purpose and main principles

A heat exchanger transfers energy between a hot and a cold fluid, normally without mixing the streams. Examples in a steam power plant include feedwater heaters, oil coolers, condensers, economizers and air preheaters. The heat duty depends on inlet conditions, flow rates, fluid properties, flow arrangement and heat-transfer conductance **UA**.

For a steady, adiabatic exchanger with negligible external losses:

$$\dot Q = \dot m_h(h_{h,in}-h_{h,out}) = \dot m_c(h_{c,out}-h_{c,in})$$

For constant specific heats, use $\dot Q=\dot m c_p\Delta T$. Here $\dot m$ is mass flow (kg/s), $h$ is specific enthalpy (J/kg), and $\dot Q$ is heat rate (W).

## 17.2 Co-current (parallel) flow

![Parallel-flow arrangement and temperature profiles](../../assets/heat-exchangers/cocurrent.png)

Both streams enter at the **same end** and travel in the **same direction**. The temperature difference is greatest near the inlet and typically shrinks toward the outlet. For sensible heating with no external work, the cold outlet cannot exceed the hot outlet in an ideal co-current exchanger. This arrangement is straightforward but often needs more heat-transfer area than counter-current flow for the same duty.

## 17.3 Counter-current flow

![Counter-current arrangement and temperature profiles](../../assets/heat-exchangers/countercurrent.png)

The streams move in **opposite directions**. A more even temperature difference is maintained along the exchanger, which usually gives a higher log-mean temperature difference (LMTD) for the same terminal temperatures. The cold outlet can be hotter than the hot outlet (but not hotter than the hot inlet), without violating the second law.

**Graph convention:** The horizontal axis in both illustrations follows the *hot-fluid direction*. In counter-current flow the cold fluid travels from right to left; therefore its temperature can decrease when plotted left-to-right, even though it heats up along its own direction of travel.

## 17.4 LMTD and heat duty

For single-phase streams with approximately constant properties:

$$\dot Q=UA\Delta T_{lm},\qquad \Delta T_{lm}=\frac{\Delta T_1-\Delta T_2}{\ln(\Delta T_1/\Delta T_2)}$$

For **co-current** flow: $\Delta T_1=T_{h,in}-T_{c,in}$ and $\Delta T_2=T_{h,out}-T_{c,out}$.

For **counter-current** flow: $\Delta T_1=T_{h,in}-T_{c,out}$ and $\Delta T_2=T_{h,out}-T_{c,in}$.

If $\Delta T_1\approx\Delta T_2$, use their common value to avoid numerical cancellation. Both terminal temperature differences must be physically valid. For multi-pass or crossflow equipment, use a correction factor $F$ when appropriate: $\dot Q=UA F\Delta T_{lm}$. For changing phase or strong property variation, a segmented enthalpy-based model is preferable.

## 17.5 Flow-dependent heat-transfer performance: exponent 0.6

A useful **simplified simulation correlation** is:

$$\boxed{UA=UA_{design}\left(\frac{\dot m}{\dot m_{design}}\right)^{0.6}}$$

![Flow-dependent UA characteristic](../../assets/heat-exchangers/ua-flow-exponent.png)

The exponent **0.6** approximates the effect of changing flow on convection in a limited operating range. It is **not** a universal physical law and is **not directly an efficiency multiplier**. The exchanger effectiveness $\varepsilon=\dot Q/\dot Q_{max}$ also depends on both streams' heat-capacity rates and the flow arrangement.

**Worked example:** If $UA_{design}=100\ \mathrm{kW/K}$ and actual flow is 50% of design, then

$$UA=100(0.5)^{0.6}=65.98\ \mathrm{kW/K}.$$

At 120% design flow, $UA=100(1.2)^{0.6}=111.56\ \mathrm{kW/K}$. Heat duty does **not** necessarily change by the same proportion: changing flow also changes outlet temperatures and $\Delta T_{lm}$.

### Important: two flowing sides

In a real exchanger, the hot-side and cold-side convection resistances can change independently. A more physical approximation is:

$$\frac{1}{UA}=\frac{1}{h_h A_h}+R_{wall}+R_{fouling}+\frac{1}{h_c A_c}$$

with $h_h=h_{h,design}(\dot m_h/\dot m_{h,design})^{0.6}$ and similarly for $h_c$, **only where the chosen correlation is justified**. This resistance model is preferred when both flows vary substantially. For zero flow, natural convection and stored heat may remain; a forced-convection power law alone does not describe this regime.

## 17.6 Dynamic behavior

A steady-state $UA\Delta T$ calculation does not represent stored energy. A dynamic exchanger has fluid holdup and metal thermal inertia. A simple lumped wall model is:

$$C_w\frac{dT_w}{dt}=\dot Q_{hot\rightarrow wall}-\dot Q_{wall\rightarrow cold}-\dot Q_{loss}$$

where $C_w=m_wc_{p,w}$ (J/K). The hot and cold streams also require mass/energy balances when their holdup is significant. For counter-current behavior, discretize the exchanger into several cells and connect the cold-side cells in reverse order.

## 17.7 PsxCad simulation exercise

1. Create two fluid streams with specified inlet temperatures, mass flows and heat capacities.
2. Implement co-current and counter-current variants with the same nominal heat-transfer area/conductance.
3. At design flow, compare calculated outlet temperatures and heat duties.
4. Apply $UA=UA_{design}(\dot m/\dot m_{design})^{0.6}$ for a one-side-dominant demonstration; then try the two-side resistance model.
5. Change one flow from 100% to 50% and trend inlet/outlet temperatures, $UA$, heat duty and energy-balance residual.
6. Add a metal thermal-capacity state; compare instantaneous steady-state behavior with the transient response.
7. Verify that heat lost by the hot stream equals heat gained by the cold stream plus any modeled storage and losses.

**Suggested signals:** `M_HOT`, `M_COLD`, `T_HOT_IN`, `T_COLD_IN`, `T_HOT_OUT`, `T_COLD_OUT`, `UA_DESIGN`, `UA_ACTUAL`, `Q_TRANSFER`, `T_WALL`.

## 17.8 Review questions

1. Why does counter-current flow usually transfer more heat than co-current flow for the same UA and inlet conditions?
2. Why can the cold outlet exceed the hot outlet temperature in counter-current operation?
3. If flow falls to 50% of design, why does heat duty not necessarily fall to 66%?
4. When should a simple LMTD model be replaced by a segmented dynamic model?
5. Which thermal masses explain a delayed outlet-temperature response after a flow change?
