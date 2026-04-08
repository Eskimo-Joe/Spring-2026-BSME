---
tags:
  - MAE337
due: 2026-04-01
submitted: T
src:
---

![[Pasted image 20260324105342.png]]

![[Pasted image 20260324105408.png]]

`<div style="page-break-after: always;"></div>

## Trial 1: 25% Throttle
$$T_{\ce{ H_{2}O },in}= 22C;\quad T_{\ce{ H_{2}O },out}=49C;\quad W_{\ce{ H_{2}O }}=48lb$$
$$T_{exhaust}=202C;\quad P_{manifold}=17inHg$$
$$F_{dyno}=20lb;\quad n=1411rpm;\quad t=192.65s$$
$$T_{atm}= 70F;\quad P_{atm}=29.98inHg;\quad V_{fuel}= 300mL$$
$$c_{p,air}=0.24 \frac{Btu}{lbm\cdot R};\quad c_{v,air}=0.17 \frac{Btu}{lbm\cdot R};\quad k=1.4$$
$$r_{c}=8.5;\quad \gamma_{Hg}=0.491 \frac{lb}{in^3};\quad \rho_{fuel}=0.78 \frac{g}{ml}$$
$$LHV_{fuel}=11000 \frac{cal}{g}$$

### Fuel flow rate
$$\dot{m}_{fuel}=\frac{\rho V}{t}=\frac{\left( 0.78 \frac{g}{ml} \right)(300ml)}{192.65s}=1.215 \frac{g}{s}$$

### Heat addition from combustion
$$\dot{Q}_{in}=\dot{m}_{fuel}\cdot LHV_{fuel}=1.215 \frac{g}{s}\cdot 11000 \frac{cal}{g}=13365 \frac{cal}{s}$$
$$\dot{Q}_{in}=13365 \frac{cal}{s}\cdot \frac{1Btu}{252.16cal}=52.99 \frac{Btu}{s}$$

`<div style="page-break-after: always;"></div>
### State 1 
$$T_{1} = T_{atm}=70F=529.67R$$
$$P_{1}=P_{manifold}+P_{atm}=17+29.98=46.98inHg$$
$$P_{1}=\gamma h=0.491 \frac{lb}{in^3}\cdot 46.98inHg =23.07psia$$

### Air flow rate
$$R_{air}=53.35 \frac{ft\cdot lbf}{lbm\cdot R}\cdot \frac{12in}{1ft}=640.2 \frac{in\cdot lbf}{lbm\cdot R}$$
$$m_{air,cyl}=\frac{P_{1}V_{1}}{R_{air}T_{1}}=\frac{(23.07psia)(36.64in^3)}{(640.2 \frac{in\cdot lbf}{lbm\cdot R})(529.67R)}=0.00249lbm$$
$$m_{air}=6m_{air,cyl}=0.01496 lbm$$
$$\dot{m}_{air}=m_{air}\cdot \frac{n}{2}=0.015lbm\cdot \frac{1411}{2} \frac{cycles}{min}\cdot \frac{1min}{60s}=0.176 \frac{lbm}{s}$$

### State 2
$$T_{2}=\frac{T_{1}}{\left( \frac{1}{r_{c}} \right)^{k-1}}=\frac{529.67R}{\left( \frac{1}{8.5} \right)^{1.4-1}}=1246.7R$$
$$P_{2}=P_{1}r_{c}^k=23.07psia(8.5)^{1.4}=461.5psia$$

`<div style="page-break-after: always;"></div>
### State 3
$$T_{3} = T_{2}+\Delta T=T_{2}+ \frac{\dot{Q}_{in}}{\dot{m}_{air}c_{v,air}}$$
$$T_{3}=1246.7R+\frac{52.99 \frac{Btu}{s}}{\left( 0.176 \frac{lbm}{s} \right)\left( 0.17 \frac{Btu}{lbm\cdot R} \right)}=3019R$$
$$P_{3}=P_{2} \frac{T_{3}}{T_{2}}=461psia \left( \frac{3019R}{1246.7R} \right)=1117.6psia$$

### State 4
$$T_{4}=\frac{T_{3}}{r_{c}^{k-1}}=\frac{3019R}{8.5^{1.4-1}}=1282.6R$$
$$P_{4}=\frac{P_{3}}{r_{c}^{k}}=\frac{1117.6psia}{8.5^{1.4}}=55.86psia$$

### Ideal heat exchange
$$\dot{Q}_{in,ideal}=\dot{m}_{air}c_{v,air}(T_{3}-T_{2})=0.176 \frac{lbm}{s}\left( 0.17 \frac{Btu}{lbm\cdot R} \right)(3019-1246R)=53 \frac{Btu}{s}$$
$$\dot{Q}_{out,ideal}=\dot{m}_{air}c_{v,air}(T_{4}-T_{1})$$
$$\left( 0.176 \frac{lbm}{s} \right)\left( 0.17 \frac{Btu}{lbm\cdot R} \right)(2887.2-529.7R)=22.51 \frac{Btu}{s}$$

`<div style="page-break-after: always;"></div>
### Ideal Otto Cycle efficiency
$$\eta_{th,ideal}=1-\frac{\dot{Q}_{out}}{\dot{Q}_{in}}=1-\frac{22.51 \frac{Btu}{s}}{53 \frac{Btu}{s}}=57.5\%$$
$$\eta_{th,ideal}=1-r_{c}^{1-k}=57.5\%$$

### Net work output
$$BHP=\frac{Fn}{5000}=\frac{(20lb)(1411rpm)}{5000}=5.644hp$$
$$\dot{W}_{net}=5.644hp\left( \frac{2545Btu}{hr} \right)\left( \frac{1hr}{3600s} \right)=3.99 \frac{Btu}{s}$$

### Heat loss into water
$$\dot{m}_{\ce{ H_{2}O }}=\frac{W}{t}=\frac{48lb}{192.65s}=.249 \frac{lbm}{s}$$
$$\dot{Q}_{\ce{ H_{2}O }}=\dot{m}_{\ce{ H_{2}O }} \bar{c}_{p,\ce{ H_{2}O }}(T_{out}-T_{in})$$
$$\dot{Q}_{\ce{ H_{2}O }}=\left( 0.249 \frac{lbm}{s} \right)\left( 1 \frac{Btu}{lbm\cdot R} \right)(49-22K)\left( \frac{9R}{5K} \right)=12.11 \frac{Btu}{s}$$

### Heat loss into exhaust
$$\dot{Q}_{ex}=\dot{m}_{air}c_{p,air}(T_{ex}-T_{atm})$$
$$\dot{Q}_{ex}=\left( 0.176 \frac{lbm}{s} \right)\left( 0.24 \frac{Btu}{lbm\cdot R} \right)\left( (202C+273.15K)\left( \frac{9R}{5K} \right)-(70+459.67R) \right)$$
$$\dot{Q}_{ex}=13.74 \frac{Btu}{s}$$

`<div style="page-break-after: always;"></div>
### Energy Balance
$$\dot{Q}_{in}=52.99 \frac{Btu}{s}$$
$$\dot{W}_{net}=3.99 \frac{Btu}{s}$$
$$\dot{Q}_{out,\ce{ H_{2}O }}=12.11 \frac{Btu}{s}$$
$$\dot{Q}_{out,exhaust}=13.74 \frac{Btu}{s}$$
$$\dot{Q}_{out,unmeasured}=\dot{Q}_{in}-\dot{W}_{net}-\dot{Q}_{out,\ce{ H_{2}O }}-\dot{Q}_{out,exhaust}=52.99-3.99-12.11-13.74$$
$$\dot{Q}_{out,unmeasured}=23.15 \frac{Btu}{s}$$

### Thermal Efficiency
$$\eta_{th}=\frac{\dot{W}_{net}}{\dot{Q}_{in}}=\frac{3.99 \frac{Btu}{s}}{52.99 \frac{Btu}{s}}=7.53\%$$
