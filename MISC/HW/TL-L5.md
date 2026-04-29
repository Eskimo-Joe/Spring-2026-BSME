---
tags:
  - MAE337
due: 2026-04-29
submitted: F
src:
---

## Trial 1
$$P_{low}=-21inHg\left( \frac{0.491psi}{1inHg} \right)+14.7psi=4.39psia$$
$$P_{high}=17inHg\left( \frac{0.491psi}{1inHg} \right)+14.7psi=23.05psia$$

#### P-h Chart

|     | Cycle State         | T (F) | P (psia) | h (Btu/lb) | v (ft^3/lb) | Fluid State       |
| --- | ------------------- | ----- | -------- | ---------- | ----------- | ----------------- |
| 1   | After Evaporation   | 74.2  | 4.386    | 98         | 9           | Saturated Vapor   |
| 2   | Before Compression  | 74.3  | 4.386    | 98         | 9           | Saturated Vapor   |
| 3   | After Compression   | 130.7 | 23.050   | 107        | 1.75        | Superheated Vapor |
| 4   | Before Condensation | 109.6 | 23.050   | 104        | 1.75        | Superheated Vapor |
| 5   | After Condensation  | 81.1  | 23.050   | 23         | 0.01        | Saturated Liquid  |
| 6   | Before Evaporation  | 26.7  | 4.386    | 13         | 0.009       | Saturated Mixture |

`<div style="page-break-after: always;"></div>


#### Mass Flow Rate
$$\dot{V}=13 \frac{mL}{min}\left( \frac{1ft^3}{28316.8 mL} \right)=0.000459cfm$$
$$v=9 \frac{ft^3}{lb}\quad \dot{m}=\frac{\dot{V}}{v}=\frac{0.000459 cfm}{9 \frac{ft^3}{lb}}=0.00000085 \frac{lbm}{s}$$

`<div style="page-break-after: always;"></div>


#### Work and Heat
$$w_{in}=h_{3}-h_{2}=107-98=9 \frac{Btu}{lbm}$$
$$w_{out}=h_{5}-h_{6}=23-10=13 \frac{Btu}{lbm}$$
$$q_{in}=h_{1}-h_{6}=98-13=85 \frac{Btu}{lbm}$$
$$q_{out}=h_{4}-h_{5}=104-23=81 \frac{Btu}{lbm}$$
$$\dot{W}_{in}=w_{in}\dot{m}=\left( 9 \frac{Btu}{lbm} \right)\left( 8.5\times 10^{-7} \frac{lbm}{s} \right)\left( \frac{1055.06J}{1Btu} \right)=0.0081W$$
$$\dot{W}_{out}=w_{out}\dot{m}=\left( 13 \frac{Btu}{lbm} \right)\left( 8.5\times 10^{-7} \frac{lbm}{s} \right)\left( \frac{1055.06J}{1Btu} \right)=0.009W$$
$$\dot{Q}_{in}=q_{in}\dot{m}=\left( 85 \frac{Btu}{lbm} \right)\left( 8.5\times 10^{-7} \frac{lbm}{s} \right)\left( \frac{1055.06J}{1Btu} \right)=0.076W$$
$$\dot{Q}_{out}=w_{out}\dot{m}=\left( 81 \frac{Btu}{lbm} \right)\left( 8.5\times 10^{-7} \frac{lbm}{s} \right)\left( \frac{1055.06J}{1Btu} \right)=0.073W$$

`<div style="page-break-after: always;"></div>

#### Coefficient of Performance
$$COP_{R}=\frac{\dot{Q}_{in}}{\dot{W}_{in}}=\frac{0.076W}{0.0081W}=9.44$$
$$COP_{HP}=\frac{\dot{Q}_{out}}{\dot{W}_{in}}=\frac{0.073W}{0.0081W}=9$$

`<div style="page-break-after: always;"></div>

#### Airflow over Heat Exchangers
$$\dot{m}_{air,evaporator}=\frac{\dot{Q}_{in}}{c_{p,air}(T_{out}-T_{atm})}=\frac{0.076W\left( \frac{1Btu}{1055.06J} \right)}{0.24 \frac{Btu}{lbm-F}(73.7F-73F)}=0.00043 \frac{lbm}{s}$$
$$\dot{m}_{air,evaporator}=0.00043 \frac{lbm}{s}\left( \frac{13.5ft^3}{lbm} \right)\left( \frac{60s}{min} \right)=0.348 cfm$$
$$\dot{m}_{air,condenser}=\frac{\dot{Q}_{out}}{c_{p,air}(T_{out}-T_{atm})}=\frac{0.073W\left( \frac{1Btu}{1055.06J} \right)}{0.24 \frac{Btu}{lbm-F}(74.6F-73F)}=0.00018 \frac{lbm}{s}$$
$$\dot{m}_{air,condenser}=0.00018 \frac{lbm}{s}\left( \frac{13.5ft^3}{lbm} \right)\left( \frac{60s}{min} \right)=0.145 cfm$$



