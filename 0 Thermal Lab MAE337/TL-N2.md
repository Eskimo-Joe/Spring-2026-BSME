---
tags:
  - MAE337
---


gas calorimetry lab

get natural gas from the wall
measure pressure and flow of gas into the chamber
burning the gas heats up the chamber and measure change in water temperature

an experimental method of determining how much energy is stored within a fuel

fuel has a higher heating value and lower heating value

HHV and LHV

ideal combustion works like this

$$C_{x}H_{y}+O_{2}\to H_{2}O+CO_{2}$$
its important to distinguish the temperature of the reaction because the water can be either liquid or water

in an ICE the water stays as a vapor because its held at an elevated temperature

LHV: is the energy of the combustion without condensing the water, is stays as a liquid

HHV: requires more energy because the water fully condenses

the difference between LHV and HHV is latent heat of water

Our combustion chamber walls will be lower than the boiling point of water

The fuel produces more energy if held at lower temperatures, but the liquid water is problematic for machinery

dont just measure the water leaving the reaction, but must account for water entering the system and find the difference. 

$$\Delta H=mc_{p}\Delta T$$
but we wont conduct experiment with mass, measure volume
$$HHV=\frac{mc_{p}\Delta T}{v}=\frac{m_{H_{2}O}\bar{c_{p}}}{v_{s}}=\frac{m(T_{2}-T_{1})}{v_{s}}$$

environmental convection: $c_{e}$
thermodynamic convection: $c_{v}$

ASTM Std:
Tatm = 60F
Patm = 30inHg
there is a standard volumetric flow rate too

our experiment will differ from this and we will account for it in calculations

$$\frac{PV}{T}=\frac{P_{std}V_{std}}{T_{std}}$$
$$V_{s}=\frac{P}{P_{std}} \frac{T_{std}}{T}V$$
solve for the standard volumetric flow rate

theres water in the gas line and vapor in the atmosphere

$$P_{gas}=P_{m}-P_{sat@ T gas}$$
$$P_{std}=P_{atm,std}-P_{sat@ Tstd}$$
$$P_{std}=30inHg-0.52inHg=29.48inHg$$
neglecting relative humidity except in air conditioning

$$\bar{c_{p,H_{2}O}}=\frac{h_{f,out}-h_{f,in}}{T_{out}-T_{in}}$$

assume $\rho_{H_{2}O}=1 \frac{g}{cm^3}$

![[Pasted image 20260128135209.png]]

![[Pasted image 20260128135225.png]]

![[Pasted image 20260128135246.png]]

![[Pasted image 20260128135259.png]]

![[Pasted image 20260128140413.png]]


$$HHV=Q-c_{t}$$
$$C_{t}=[n_{p}c_{p,\prod}\Delta T_{p}]-[n_{reaction}c_{p,reaction}\Delta T_{reaction}]$$

generally uses imperial units
expected to convert between units

## 2-04

$$CH_{4}+3\left( O_{2}+\frac{79}{21}N_{2} \right)\to CO_{2}+2H_{2}O(l)+O_{2}+11.283N_{2}$$
left:
$$H_{R@T=exp}=H_{R@T=std}+nC_{p}\Delta T$$
right: 
$$H_{P@T=exp}=H_{P@T=std}+nC_{p}\Delta T$$
$$Q=H_{p@T=\exp}-H_{R@T=\exp}$$
^ replace H values with equations above
$$Q=H_{p}-H_{R}+[nC_{p}\Delta T-nC_{p}\Delta T]$$
$$Q=HHV+[nC_{p}\Delta T_{P}-nC_{p}\Delta T_{R}]$$
$$HHV=Q-[nC_{p}\Delta T_{P}-nC_{p}\Delta T_{R}]$$
$$Q=\frac{n \bar{c_{p}\Delta T+c_{e}}}{v_{s}}+c_{t}$$
$$c_{t}=[(c_{p,CO_{2}}+c_{p,O_{2}}+11.285c_{p,N_{2}})(T_{ex}-T_{std})+(nc_{p,H_{2}O})(T_{cond}-T_{std})]-[(nc_{p,CH_{4}})(T_{fuel}-T_{std})+(nc_{p,O_{2}}+nc_{p,N_{2}})(T_{air}-T_{std})]$$

one rotation is .1 cubic feet



