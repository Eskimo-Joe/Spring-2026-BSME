
Lecture about next lab, ICE

there are analysis of Otto and Diesel cycles, but experiment is only on Otto cycle

review of Otto cycle for ICEs

When piston is at highest point, Top Dead Center (TDC)
when piston is at lowest point, Bottom Dead Center (BDC)

four stroke engines have four strokes per cycle, combusting once per cycle
1. intake
2. compression
3. combustion
4. exhaust

two crankshaft rotations in one cycle

we want to analyze the ICE as a steady-state heat engine, so we can model the ICE differently as analysis

Pretend the combustion occurs at compression at HHV instantaneously
Also assume exhaust and intake air swaps instantaneously

Its a grad school topic to improve thermal models of engines

state 1: intake
state 2: compression
state 3: combustion 
state 4: instant exchange of exhaust and intake

T-s diagram
state 1 is low temp low entropy
isentropic temp increase to state 2
combustion increases temp and entropy to state 3
isentropic expansion, temp lowers
temp and entropy decreases back to state 1 (assume all the combustion heat is exhausted and fresh cool air is supplied)

P-v diagram
Start in lower right corner at BDC and low pressure
Move up-left to state 2
constant volume compression to state 3
isentropic expansion to BDC to state 4
constant-volume decompression back to 1

characteristics of the engine
swept volume - difference from TDC to BDC =
$$\frac{\pi(\text{Bore diam.})^2}{4}\times \text{piston travel}=194in^3$$
inline 6 cylinder engine
$$V_{swept}(\text{per cylinder})=\frac{194in^3}{6}=V_{BDC}-V_{TDC}$$
compression ratio BDC/TDC
$$r_{c}=\frac{V_{BDC}}{V_{TDC}}=8.5$$
$$\eta_{th,ideal}=1-r_{c}^{1-\gamma}$$
$$\gamma=k=\frac{c_{p}}{c_{v}}=1.4$$

constants
$$c_{p,air}=0.24 \frac{Btu}{lbm^{\circ}F}$$
$$c_{v,air}=0.17$$
defined at 25C or 77F
1atm = 14.7psi
"perfect gas"

| Perfect Gas Relations   | P-V                                                        | T-P                                           | T-V                                                            | Q                | $\Delta s$                       |
| ----------------------- | ---------------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------------- | ---------------- | -------------------------------- |
| isochoric (constant v)  |                                                            | $\frac{T_{i}}{T_{f}}=\frac{P_{i}}{P_{f}}$     |                                                                | $mc_{v}\Delta T$ | $mc_{v}\ln{\frac{T_{2}}{T_{1}}}$ |
| isobaric (constant P)   |                                                            |                                               | $\frac{T_{i}}{T_{f}}=\frac{V_{i}}{V_{f}}$                      | $mc_{p}\Delta T$ |                                  |
| isentropic (constant s) | $\frac{P_{i}}{P_{f}}=\left( \frac{V_{f}}{V_{i}} \right)^k$ | $$\frac{T_{i}}{T_{f}}=r_{c}^{\frac{k-1}{k}}$$ | $\frac{T_{i}}{T_{f}}=\left( \frac{V_{f}}{V_{i}} \right)^{k-1}$ |                  |                                  |
Perfect gas: more specific than ideal gas
uses cold air standard assumptions at the conditions defined above

measurements and givens during lab
T_atm
P_atm
P_manifold
V_fuel
density_fuel
LHV
RPM
t
T_H2O_in
T_H2O_out

state 1:
$P_{1}=P_{manifold}$
$T_{1}=T_{atm}$
$V_{1}=V_{BDC}$
we're not concerned with absolute, so $s_{1}=0$

state 2:
$P_{2}\to\frac{P_{1}}{P_{2}}=\left( \frac{V_{2}}{V_{1}} \right)^k\to P_{2}=P_{1}r_{c}^{k}$
$T_{2}=\frac{T_{1}}{\left( \frac{V_{2}}{V_{1}} \right)^{k-1}}$
$V_{2}=V_{TDC}$
$s_{2}=0$

state 3:
$P_{3}=P_{2} \frac{T_{3}}{T_{2}}$
$T_{3}=T_{2}+\frac{\dot{Q}_{in}}{\dot{m}_{air}c_{v,air}}$
$V_{3}=V_{TDC}$
$s_{3}=s_{2}+mc_{v}\ln \frac{T_{3}}{T_{2}}$

how much heat is added from the combustion? 
$$\dot{Q}_{in}= \dot{m}_{fuel}\times LHV$$
LHV is used because the water vapor is not condensing
$$V_{fuel}=300mL$$
$$\rho_{fuel}=0.78 \frac{g}{mL}$$
$$\dot{m}_{fuel}=\frac{V_{fuel}}{t_{run}\rho_{fuel}}$$
how much heat is added by the atm?
$$\dot{Q}_{in}=\dot{m}_{air}c_{v,air}(T_{3}-T_{2})$$
$$\dot{m}_{air}\left[ \frac{g}{s} \right]=\frac{P_{1}V_{1}}{R_{air}T_{1}}\times 6cyl.\times \frac{f}{2}\left( \frac{cycles}{s} \right)$$
$$T_{3}=T_{2}+\frac{\dot{Q}_{in}}{\dot{m}_{air}c_{v,air}}$$
$$P_{3}=P_{2} \frac{T_{3}}{T_{2}}$$
discuss why P3 is so high and the sources of error
attempt to reference it once

state 4:
$P_{4}=\frac{P_{3}}{r_{c}^k}$
$T_{4}=\frac{T_{3}}{\left( \frac{V_{4}}{V_{3}} \right)^{k-1}}=\frac{T_{3}}{r_{c}^{1/(k-1)}}$
$V_{4}=V_{BDC}$
$s_{4}=s_{3}$

$$\frac{P_{3}}{P_{4}}=\left( \frac{V_{4}}{V_{3}} \right)^k$$
$$P_{4}=\frac{P_{3}}{r_{c}^k}$$
$$\frac{T_{3}}{T_{4}}=\left( \frac{V_{4}}{V_{3}} \right)^{k-1}$$
$$T_{4}=\frac{T_{3}}{\left( \frac{V_{4}}{V_{3}} \right)^{k-1}}=\frac{T_{3}}{r_{c}^{1/(k-1)}}$$

now that the four states are fully defined we can analyze the work output of the engine
using a dyno to take measurements

torque:
$$\tau=F\times d$$
$$F_{d}=\text{dynamometer load }[lbs]$$
$$L=\text{torque radius }[ft]=\frac{33}{10\pi}$$
$$n=RPM$$
$$\tau=F_{d}\times L$$
$$BHP[hp]=\frac{2\pi F_{d}Ln}{33000}=\frac{Fn}{5000}$$
plot power vs rpm and torque vs rpm

try three runs to try not to destroy the engine

real efficiency

$$\eta_{th}=\frac{\dot{W}_{out}}{\dot{Q}_{in}}$$
$$745.7W=1hp$$
brake specific fuel consumption (BSFC)
$$BSFC=\frac{\dot{m}_{fuel}}{Power_{out}}\left[ \frac{g_{fuel}}{S\cdot hp} \right]$$
$$\dot{Q}_{out,loss,cooling}=\dot{m}_{\ce{ H_{2}O }}\bar{c}_{p,\ce{ H_{2}O }}(T_{\ce{ H_{2}O },out}-T_{\ce{ H_{2}O },in})$$
$$\dot{Q}_{loss,exhaust}=\dot{m}_{air}\bar{c}_{p,air}(T_{ex}-T_{atm})$$
$$\dot{Q}_{loss,unmeasured}=\dot{Q}_{in}-\dot{W}_{out}-\dot{Q}_{cooling}-\dot{Q}_{exhaust}$$

include in lab report: % of energy at each output
compare ideal efficiency to real efficiency





