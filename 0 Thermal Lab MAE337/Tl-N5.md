
[Sign in to your account](https://csulb.instructure.com/courses/116797/files/28964186?module_item_id=6991749)

Lab 3 due Mar 25

Final will be easy, cheat sheet both sides

gas turbine (brayton cycle) experiment next week

our turbine is for producing thrust more so than power generation
brayton cycle:
1. Compressor
2. Combustion
3. Turbine exhausting air

use tables for air properties (A-17)
NIST has air tables with more fine increments
"air properties web books"

measure pressure and temp at all five points:
1. compression
2. before combustion
3. after combustion
4. in turbine
5. exhaust

$$w_{in}=w_{c}=h_{2}-h_{1}$$
$$w_{out}=w_{t}=h_{3}-h_{4}$$
$$q_{in}=q_{fuel}=h_{3}-h_{2}$$
we are neglecting the efficiency of combustion and turbine

$$w_{cycle}=w_{t}-w_{c}$$
$$\eta_{cycle}=\frac{w_{cycle}}{q_{in,fuel}}$$
if efficiency is negative round it to zero
it is highly likely because the turbine work can be less than the compressor work

$$\eta_{total}=\frac{KE_{exhaust}}{q_{in,fuel}}$$
$$1\frac{Btu}{lbm}\to 25,037  \frac{ft^2}{s^2}$$
$$KE=\frac{V^2}{2}\text{@ point 5}$$

$$\eta_{Brayton}=1-\frac{1}{r_{p}^{\frac{\gamma-1}{\gamma}}}$$
$r_{p}$ - pressure ratio
$\gamma=k$

analysis of the compressor
how to measure the compressors efficiency?

draws an h-s diagram with two constant pressure lines
An ideal brayton cycle considers compression an isentropic cycle..
but real compression increases the entropy

the ideal compression goes $1\to 2s$
real compression goes $1\to 2$

$h_{2}$ will be higher than $h_{2s}$, meaning the real compressor is using more work than an ideal one
$$\eta_{compressor}=\frac{h_{2s}-h_{1}}{h_{2}-h_{1}}$$

turbine analysis
draws another h-s diagram with constant pressure lines for P3 and P4

an ideal turbine is isentropic from $3\to 4s$
a real turbine increases in entropy from $3-4$

$$\eta_{turbine}=\frac{h_{3}-h_{4}}{h_{3}-h_{4s}}$$

can use cold-air std for isentropic assumptions only
$$\gamma=1.4;\quad c_{p}=0.24 \frac{Btu}{lbm\cdot ^{\circ}F};\quad c_{v}=0.17$$
use this equation to solve for $T_{2s}$ and $T_{4s}$
$$\left( \frac{T_{f}}{T_{i}} \right)=\left( \frac{P_{f}}{P_{i}} \right)^{\frac{\gamma-1}{\gamma}}$$

then plug in $T_{2s}$ and $P_{2}$ to find $h_{2s}$ in air tables
same for $h_{4s}$

thrust value will be measured
$$F_{thrust}=\frac{\dot{m}_{air}\times V_{5}}{32.174}$$
$$g=32.174 \frac{ft}{s^2}$$
$$\dot{m}_{air}=\frac{Volume}{time}\times \rho_{5}$$
$$\frac{Volume}{time}=\dot{V}=A_{c_{5}}\cdot V_{5}$$
$$A_{c_{5}}=3.88 in^2$$
reduce thrust equation:
$$F_{thrust}=\frac{(3.88in^2)\rho_{5}(V_{5})^2}{32.174}$$
We will measure thrust force and solve for velocity

mach number (ratio of velocity to local speed of sound):
$$M=\frac{V_{5}}{\sqrt{ \gamma Rg_{c}T_{5} }}$$
$$\gamma = k = 1.4$$
$$R = \text{gas constant}$$
$$g_{c} = \text{gravity constant}=32.174$$

Thrust Specific Fuel Consumption (TSFC):
$$TSFC=\frac{\dot{m}_{fuel}}{F_{thrust}}=\frac{\left[ \frac{mass}{time} \right]}{\text{force}}=\frac{mass}{force\times time}$$
(specific) kinetic energy:
$$KE=\frac{V_{5}^2}{2}$$

efficiency:
$$\eta_{total}=\frac{KE}{q_{in}}=\frac{\left[ \frac{Energy}{mass} \right]}{\left[ \frac{energy}{mass} \right]}$$

another thing to analyze:
How quickly the fuel is being combusted within the combustion chamber

$$\dot{m}_{fuel}=\dot{V}_{fuel}\times \rho_{fuel}$$
$$\dot{m}_{fuel}\times LHV_{fuel}=\dot{Q}_{in,fuel}$$
$$\frac{\dot{H}_{comb}}{\dot{Q}_{in}}=\eta_{comb}$$


will do multiple runs at different speeds
ideally the highest efficiency will occur at the max throttle


