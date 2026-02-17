---
tags:
  - MAE337
due: 2026-02-18
submitted: F
src:
---

# Sample Calculations: Run 1
## ASTM Volume Standard
$$P_{s}=29.48\text{inHg}\quad T_{s}=60^{\circ}F$$
$$P_{m}=.3\text{in}\ce{ H_{2}O }\quad T_{m}=73.5^{\circ}F\quad V_{m}=.217\text{ft}^3$$
$$P_{s}=29.48\text{inHg}\left( \frac{1\text{in}\ce{ H_{2}O }}{13.6\text{inHg}} \right)(\frac{.03609 \text{psi}}{1\text{in}\ce{ H_{2}O }})+14.696\text{psi}=14.77\text{psia}$$
$$P_{m}=.3\text{in}\ce{ H_{2}O }\left( \frac{.03609\text{psi}}{1\text{in}\ce{ H_{2}O }} \right)+14.696\text{psi}=14.71\text{psia}$$
$$V_{s}=\frac{P_{m}V_{m}T_{s}}{P_{s}T_{m}}=\frac{(14.71\text{psia})(.217\text{ft}^3)(60+459.7 R)}{(14.77\text{psia})(73.5+459.7R)}=.211\text{ft}^3$$

## Specific Heat of Water
$$T_{in}=73.3^{\circ}F\quad T_{out}=83.3^{\circ}F$$
$$h_{f, in}=41.4 \frac{\text{Btu}}{\text{lbm}}\quad h_{f,out}=51.4\frac{\text{Btu}}{\text{lbm}}$$
$$\bar{c}_{p,\ce{ H_{2}O }}=\frac{h_{f,out}-h_{f,in}}{T_{out}-T_{in}}=\frac{51.4\frac{\text{Btu}}{\text{lbm}}-41.4\frac{\text{Btu}}{\text{lbm}}}{83.3R-73.3R}=1.003\frac{\text{Btu}}{\text{lbm}-R}$$

## Correction Factor of Water from Gas Line
$$h_{c}=5\frac{\text{Btu}}{\text{hr-ft}^2\text{F}}\quad A=2.1\text{ft}^2\quad t=\frac{5}{60}\text{hours}=.083\text{hr}$$
$$T_{\text{shell}}=79.3^{\circ}F\quad T_{\text{fuel}}=73.5^{\circ}F$$
$$C_{e}=h_{c}At\Delta T=(5\frac{\text{Btu}}{\text{hr-ft}^2\text{F}})(2.1\text{ft}^2)(.083\text{hr})(79.3-73.5^{\circ}F)=5.104 \text{ Btu}$$

`<div style="page-break-after: always;"></div>

## Correction Factor for Heat at non-standard Temperature

| Substance | $c_{p} \frac{\text{Btu}}{\text{lb-mole}}$ |
| --------- | ----------------------------------------- |
| O2        | 7                                         |
| N2        | 6.984                                     |
| CO2       | 8.88                                      |
| H2O       | 18                                        |
| CH4       | 8.48                                      |

| Fluid      | Temprature ($^{\circ}\text{F}$) |
| ---------- | ------------------------------- |
| exhaust    | 74.7                            |
| fuel       | 73.5                            |
| condensate | 73.5                            |
| standard   | 60                              |
| air        | 73.5                            |

$$C_{t}=[(c_{p,\ce{ H_{2}O }}+c_{p,\ce{ O_{2} }}+11.285c_{p,\ce{ N_{2} }})(T_{\text{exhaust}}-T_{\text{std}})+2c_{p,\ce{ H_{2}O }}(T_{\text{condensate}}-T_{\text{std}})]$$
$$-[(3c_{p,\ce{ O_{2} }}+11.285c_{p,\ce{ N_{2} }})(T_{\text{air}}-T_{\text{std}})+c_{p,\ce{ CH_{4} }}(T_{\text{gas}}-T_{\text{std}})]$$
$$C_{t}=[(18+7+11.285\cdot 6.984 \frac{\text{Btu}}{lb-mole})(74.7-60^{\circ}F)+2\cdot 18\frac{\text{Btu}}{lb-mole}(73.5-60^{\circ}F)]$$
$$-[(3\cdot 7+11.285\cdot 6.984\frac{\text{Btu}}{lb-mole})(73.5-60^{\circ}F)+8.48\frac{\text{Btu}}{lb-mole}(73.5-60^{\circ}F)]$$
$$C_{t}=294.734 \frac{\text{Btu}}{\text{lb-mole}}$$
$$C_{t}=(294.734 \frac{\text{Btu}}{\text{lb-mole}})(\frac{73.5+459.7R}{60+459.7R})(\frac{1\text{lb-mole}}{379.6\text{ft}^3})=0.797 \frac{\text{Btu}}{\text{ft}^3}$$

`<div style="page-break-after: always;"></div>

## Heat Transfer
$$W_{\ce{ H_{2}O }}=(10,470 \text{mL})\left( \frac{1\text{g}}{1\text{mL}} \right)\left( \frac{1\text{kg}}{1000\text{g}} \right)\left( \frac{2.2046\text{lb}}{1\text{kg}} \right)=23.08\text{lb}$$
$$\bar{c}_{p,\ce{ H_{2}O }}=1.003 \frac{\text{Btu}}{\text{lbm-R}}\quad C_{e}=5.104\text{Btu}$$
$$T_{in}=73.3^{\circ}F\quad T_{out}=83.3^{\circ}F$$
$$V_{s}=.211 \text{ft}^3$$

$$Q=\frac{W_{\ce{ H_{2}O }} \bar{c}_{p,\ce{ H_{2}O }}\Delta T-C_{e}}{V_{s}}$$
$$Q=\frac{(23.08\text{lb})(1.003 \frac{\text{Btu}}{\text{lbm-R}})(83.3-73.3R)-5.104\text{Btu}}{.211\text{ft}^3}=1120.58 \frac{\text{Btu}}{\text{ft}^3}$$


## Higher Heating Value
$$Q=1120.58 \frac{\text{Btu}}{\text{ft}^3} \quad C_{t}=0.797 \frac{\text{Btu}}{\text{ft}^3}$$
$$\text{HHV}_{\text{expected}}=1010 \frac{\text{Btu}}{\text{ft}^3}$$
$$\text{HHV}_{\text{measured}}=Q-C_{t}=1120.58-0.797=1119.8 \frac{\text{Btu}}{\text{ft}^3}$$
$$\text{Error}=\frac{|\text{HHV}_{\text{measured}}-\text{HHV}_{\text{expected}}|}{\text{HHV}_{\text{expected}}}=\frac{|1119.8-1010|}{1010}=10.87\%$$

`<div style="page-break-after: always;"></div>

## Lower Heating Value
$$\text{HHV}_{\text{measured}}=1119.8 \frac{\text{Btu}}{\text{ft}^3}$$
$$h_{fg,\ce{ H_{2}O }}=1059 \frac{\text{Btu}}{\text{lbm}}\quad V_{s}=.211 \text{ft}^3$$
$$\text{m}_{\text{condensate}}=(7.5\text{mL})\left( \frac{1\text{kg}}{1000\text{mL}} \right)\left( \frac{2.2046\text{lbm}}{1\text{kg}} \right)=0.017\text{lbm}$$
$$\text{LHV}_{\text{expected}}=909.4\frac{\text{Btu}}{\text{ft}^3}$$
$$\text{LHV}_{\text{measured}}=\text{HHV}_{\text{measured}}-\frac{h_{fg,\ce{ H_{2}O }}\cdot \text{m}_{\text{condensate}}}{V_{s}}$$
$$\text{LHV}_{\text{measured}}=1119.8\frac{\text{Btu}}{\text{lbm}}-\frac{(1059 \frac{\text{Btu}}{\text{lbm}})(0.017\text{lbm})}{.211 \text{ft}^3}=1036.6\frac{\text{Btu}}{\text{lbm}}$$
$$\text{Error}=\frac{|\text{LHV}_{\text{measured}}-\text{LHV}_{\text{expected}}|}{\text{LHV}_{\text{expected}}}=\frac{|1036.6-909.4|}{909.4}=13.99\%$$

