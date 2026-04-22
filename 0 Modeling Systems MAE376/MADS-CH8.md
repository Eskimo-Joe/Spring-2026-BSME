

System Response

8.1-8.2

- system response
	- type of response
	- a
	- b

remember solving ODEs with complimentary solution and particular solution

when $g(t)=0$, the complimentary response is called free response or natural response

when $g(t)\ne 0$ the particular solution is included and the response is called forced response

the total response can be decomposed into two parts
1. transient response
	1. Decays to zero when $t\to \infty$
2. steady-state response
	1. Remains as $t\to \infty$

$$x(t)=x_{tr}(t)+x_{ss}(t)$$

example
$$3 \ddot{x}+7 \dot{x}+ 2x=50 \sin t,\quad x(0)=-1,\quad \dot{x}(0)=1$$
$$3r^2+7r+2=0$$
$$r=\frac{-7\pm \sqrt{ 49-24 }}{6}=\frac{-7\pm5}{6}$$
$$r_{1}=-2\quad r_{2}=- \frac{1}{3}$$
$$x_{c}=C_{1}e^{-2t}+C_{2}e^{-t/3}$$
$$x_{p}=A\sin t+B\cos t$$
$$\dot{x}_{p}=A\cos t-B\sin t$$
$$\ddot{x}_{p}=-A\sin t-B\cos t$$
$$-3A\sin t-3B\cos t+7A\cos t-7B \sin t+2A\sin t+2B \cos t=50\sin t$$
$$(-3A-7B+2A)\sin t+(-3B+7A+2B)\cos t =50 \sin t$$
$$7A-B=0\to 7A=B$$
$$-A-7B=50\to -A-49A=50\to A=-1\quad B=-\frac{1}{7}$$
$$x_{p}=-\sin t- \frac{1}{7}\cos t$$
$$x(t)=C_{1}e^{-2t}+C_{2}e^{-t/3}-\sin t- \frac{1}{7} \cos t$$
$$x_{tr}=C_{1}e^{-2t}+C_{2}e^{-t/3}$$
$$x_{ss}=-\sin t - \frac{1}{7}\cos t$$


First-order systems

a linear, firs-order system:
$$\tau \dot{x}+x=f(t)\quad x(0)=x_{0}$$
$\tau$ is the time constant, $\tau>0$

$$\tau (sX-x_{0})+X=F$$
$$(\tau s+1)X - \tau x_{0}=F$$
$$X=\frac{F+\tau x_{0}}{\tau s+1}=\frac{F}{\tau s+1}+\frac{\tau x_{0}}{\tau s+1}$$
$$x=L^{-1}\left\{ \frac{F}{\tau s+1}  \right\}+x_{0}e^{-t/\tau}$$
the first term is response to input or zero-state
the second term is the response to initial excitation

find the zero input response to this ode
$$3 \dot{v}+v=0\quad v(0)=1$$
$$e^{-t/3}$$

if 
$$\tau \dot{x}+x=f(t)$$
use a complimentary solution and find forced response with the zero-state

$$L^{-1}\left\{ \frac{\frac{A}{s}}{\tau s+1}  \right\}=$$
....
$$=A-Ae^{-t/\tau}=A(1-e^{-t/\tau})$$

$\tau$ is the time where the function is 63.2% of the steady state
$x_{ss}$ is where the function converges
it takes $4\tau$ to get to 98.2% of the $x_{ss}$

$$\tau \dot{x}+x=Au(t)\quad x(0)=x_{0}$$
$$x(t)=e^{-t/\tau}+A(1-e^{-t/\tau})$$



example
$$3 \dot{v} +2v=u(t)\quad v(0)=0$$
$$x(t)=e^{-2t/3}+\frac{1}{2}(1-e^{-2t/3})$$


ramp response

$$f(t)=Au_{r}(t)$$
consider it just y=mx
$$F(s)=\frac{A}{s^2}$$
... changes to general form

$$x(t)=A(t-\tau(1-e^{-t/\tau}))$$
the term $-e^{-t/\tau}$ is transient
the 1 which turns into $A\tau$ is steady state

$$x_{ss}=A(t-\tau)$$
the error term finds the difference between ramp input and ramp response 
$$e_{ss}=A\tau$$


next: 8.3 transient response and second order

For assignment 11
8.1: 1, 2, 4, 5, 8, 9, 10, 11, 12


## 4-09

Second order dynamic systems

Mathematical model:
$$\ddot{x}+2\zeta \omega_{n} \dot{x}+\omega^2_{n}x=f(t)$$
$$x(0)=x_{0}\quad \dot{x}(0)= \dot{x}_{0}$$

where $\omega_{n}$ is the undamped natural frequency in $\frac{rad}{s}$
and $\zeta$ is the damping ratio (ratio of actual damping to critical damping)

compare to the equation of motion for a SDOF mechanical system

$$\ddot{x}+\frac{c}{m} \dot{x}+ \frac{k}{m}x=\frac{1}{m}f(t)$$
$$\omega_{n}=\sqrt{ \frac{k}{m} } \frac{radians}{s}\quad \zeta=\frac{c}{2m\omega_{n}}=\frac{c\sqrt{ m }}{2m\sqrt{ k }}=\frac{c}{2\sqrt{ mk }}$$

laplace of the equation
$$s^2X-sx_{0}-\dot{x}_{0}+2\zeta \omega_{n}(sX-x_{0})+\omega^2_{n}X=F$$
...
$$x(t)=L^{-1}\left\{ \frac{(s+2\zeta \omega_{n})x_{0}+\dot{x}_{0}}{s^2+\zeta \omega_{n}s+\omega^2_{n}}  \right\}+L^{-1}\left\{ \frac{1}{s^2+2\zeta \omega_{n}s+\omega_{n}^2}F(s)  \right\}$$

find root of $s^2+2\zeta \omega_{n}s+\omega_{n}^2$
$$s=-\zeta \omega_{n}\pm \omega_{n}\sqrt{ \zeta^2-1 }$$
the roots depend on the value of $\zeta$
Can be two roots, one root, or complex roots
$|\zeta|>1$ is two roots, meaning overdamped
$|\zeta|=1$ is one root, meaning critically damped
$-1<\zeta<1$ is complex roots, meaning underdamped system
if $\zeta=0$, it is an undamped system

damped natural frequency:
$$\omega_{d}=\omega_{n}\sqrt{ 1-\zeta^2 }$$


example
$$\ddot{x}+3 \dot{x}+2x=0$$
$$\omega_{n}=\sqrt{ 2 }$$
$$2\zeta \omega_{n}=3\quad \zeta=\frac{3}{2\sqrt{ 2 }}$$

state-space, 2 variables requires

... convert the ODE to steady-state

impulse response, dirac delta
$$f(t)=A\delta(t)$$
$$F(s)=A$$
laplace on line 125
$$x(t)=L^{-1}\left\{  \frac{(s+\zeta \omega_{n})x_{0}+\dot{x}_{0}+A}{s^2+\zeta \omega_{n}s+\omega^2_{n}} \right\}$$
... if complex roots, use partial fractions like so
$$\frac{A}{s+\zeta \omega_{n}+i\omega_{n}\sqrt{ 1-\zeta^2 }}+\frac{B}{s+\zeta \omega_{n}-i\omega_{n}\sqrt{ 1-\zeta^2 }}$$

pg X in the book

if $\zeta=0$, 
$$x(t)=x_{0}\cos \omega_{n}t+ \frac{\dot{x}_{0}}{\omega_{n}}\sin \omega_{n}t+ \frac{A}{\omega_{n}}\sin \omega_{n}t$$
if $0<\zeta<1$,
$$x(t)=e^{-\zeta \omega_{n}t}[x_{0}\zeta \omega_{n}t+\frac{\zeta \omega_{n}x+\dot{x}_{0}+A}{\omega_{d}}\sin \omega_{n}t]$$

example
$$\ddot{x}+2 \dot{x}+ Kx=10\delta(t)\quad x(0)=0\quad \dot{x}(0)=0$$
$$\omega_{n}=\sqrt{ K }\quad \zeta=\frac{1}{\sqrt{ K }}$$
$$s^2X+2sX+KX=10$$
$$X(s)=\frac{10}{s^2+2s+K}$$


in a step respons... 
$$f(t)=Au(t)\quad F(s)=\frac{A}{s}$$
so
$$X(s)=L^{-1}\{\frac{(s+2\zeta \omega_{n})x_{0}+\dot{x}_{0}}{}\}$$
...

for a 2DOF system, must use four variables and graph the SS only

will use lagrange method instead of eulers method or newtons 2nd law
lagrange uses energy instead of force



## 4-14

going back to chapter 5 to learn the lagrange method of writing equations of motion
page 223

uses energy instead of sum of forces

For a mass-spring system:
$$T+V=\text{Constant}$$
$$\frac{d}{dt}(T+V)=0$$

kinetic energy of a particle
$$T=\frac{1}{2}mv^2$$
rigid body
$$T=\frac{1}{2}mv^2+\frac{1}{2}I_{c}\omega^2$$
potential energy of elasticity
$$V_{e}=\frac{1}{2}kx^2$$
potential energy of gravitational 
$$V_{g}=mgh$$

there is a lagrangian $L=T-V$
Lagrange equation:
$$\frac{d}{dt}\left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\frac{ \partial L }{ \partial q_{i} }=q_{i} $$
q: generalized external force, number of degrees of freedom

$$\frac{d}{dt}\left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\frac{ \partial L }{ \partial q_{i} }=q_{i} $$

$$L=T-V$$
$$L=\frac{1}{2}m\dot{x}^2-\frac{1}{2}kx^2$$
use $\dot{x}$ instead of $v$

$$q_{1}=x\quad \dot{q}_{1}=\dot{x}$$
$$\frac{d}{dt}\left( \frac{ \partial L }{ \partial \dot{q} }  \right)-\frac{ \partial L }{ \partial q_{i} } =q_{i}$$
$$\frac{dL}{dx}=-kx$$
$$\frac{dL}{d\dot{x}}=m\dot{x}$$
$$\frac{d}{dt}(m\dot{x})-kx=x$$
$$m\ddot{x}-kx=0$$
add a damper with
$$\frac{1}{2} c\dot{x}^2$$


2nd example with pendelum

$$L=T-V$$
$$L_{1}=\frac{1}{2}m(L_{1} \dot{\theta}_{1})^2+\frac{1}{2}I\dot{\theta_{1}}^2+mg(L_{1}\cos\theta_{1})$$
$$\frac{dL}{dx}=$$
... adding a second degree of freedom for a double pendelum

$$T_{2}=\frac{1}{2}mL_{2}\dot{\theta}_{2}^2+\frac{1}{2}I \dot{\theta}_{2}^2$$
$$V_{m_{2}}^2=[L_{1}\dot{\theta}_{1}+L_{2}\dot{\theta}_{2}\cos(\theta_{2}-\theta_{1})]^2+[L_{2}\dot{\theta}_{2}^2\sin(\theta_{2}-\theta_{1})]^2$$
or use law of cosines
$$c^2=a^2+b^2+2ab\cos \theta$$
$$U_{2}=-mgh=-mg(L_{2}\cos \theta_{2}+L_{1}\cos \theta_{1})$$
$$\frac{ \partial U }{ \partial \theta_{1} } =mgL_{1}\sin \theta_{1}+mgL_{1}\sin \theta_{1}$$
$$\frac{ \partial U }{ \partial \theta_{2} }=mgL_{2}\sin \theta_{2} $$
$$\frac{ \partial T }{ \partial \theta_{1} } =$$
$$\frac{ \partial T }{ \partial \theta_{2} } =$$

when considering the bar a rigid body, add the respective terms in T and U
$$\frac{1}{2}I_{o}\dot{\theta}^2=\frac{1}{2}m\left( \frac{L}{2}\dot{\theta} \right)^2+\frac{1}{2}I_{c}\dot{\theta}^2$$


example from the book with pulley and spring

sample problem 5.18


## 4-16

bring hw problems for prof to solve on April 28

continue chapter 8 

intro to chapter 9, vibrations
- intro to vibrations
	- free vibe of SDOF (homogeneous ODE)
		- undamped
		- viscously damped
	- forced vibe of SDOF (nonhomogeneous ODE)
		- harmonic excitations (uses sine input)
		- frequency response

neglect gravity because it cancels with the spring force already
where the mass rests is the equilibrium position
$$k\delta=mg$$
no mg in the equation, because we the initial condition is not always the equilibrium position
$$m \ddot{x}+k x=0$$
a mass-spring system will oscillate forever, to make it more accurate we will add a damper 

remember
$$\ddot{x}+ 2\zeta \omega_{n} \dot{x}+\omega^2_{n}x=f(t)$$
$$x(0)=x_{0}\quad \dot{x}(0)=\dot{x}_{0}$$
$\omega_{n}$ - natural frequency
$\zeta$ - damping ratio

$$\omega_{n}=\sqrt{ \frac{k}{m} } \frac{radians}{s}\quad \zeta=\frac{c}{2m\omega_{n}}=\frac{c\sqrt{ m }}{2m\sqrt{ k }}=\frac{c}{2\sqrt{ mk }}$$

$$x(t)=L^{-1}\left\{ \frac{(s+2\zeta \omega_{n})x_{0}+\dot{x}_{0}}{s^2+\zeta \omega_{n}s+\omega^2_{n}}  \right\}+L^{-1}\left\{ \frac{1}{s^2+2\zeta \omega_{n}s+\omega_{n}^2}F(s)  \right\}$$
left term: zero-input response (response to initial conditions)
right term: zero-state response (response to forcing function)

find root of $s^2+2\zeta \omega_{n}s+\omega_{n}^2$
$$s=-\zeta \omega_{n}\pm \omega_{n}\sqrt{ \zeta^2-1 }$$
the roots depend on the value of $\zeta$
Can be two roots, one root, or complex roots
$|\zeta|>1$ is two roots, meaning overdamped
$|\zeta|=1$ is one root, meaning critically damped
$-1<\zeta<1$ is complex roots, meaning underdamped system
if $\zeta=0$, it is an undamped system

review ends
underdamped SDOF equation
$$T=\frac{2\pi}{\omega_{d}}$$
$$x(t)=e^{-\zeta \omega_{n}t}(x_{0}\cos \omega_{d} t +\frac{\zeta \omega_{n}x_{0}+v_{0}}{\omega_{d}}\sin \omega_{d}t)$$

usually dampers are not used in spring-mass system, but damping occurs naturally

experimentation is required to find damping

using the folowing identities the equation above can be simplified
$$\cos\alpha\cos\beta+\sin\alpha\sin \beta=\cos()$$
$$\sin\alpha\cos \beta+\cos \alpha\sin \beta=\sin()$$
divide those two equations to get cotangent

$$x(t)=Ae^{-\zeta \omega_{n}t}\cos(\omega_{d}t-\phi)$$
$$\phi=\tan^{-1}{\frac{\zeta \omega_{n}x_{0}+v_{0}}{\omega_{d}x_{0}}}$$
find $\omega_{d}$ using period
must solve for $\omega_{n}$, $\zeta$, and $A$

take measurement of amplitudes to solve
$$\frac{x_{1}}{x_{2}}=e^{2\pi \zeta/\sqrt{ 1-\zeta^2 }}$$
$$\delta=\ln{\frac{x_{1}}{x_{2}}}=\frac{1}{n} \ln{\frac{x_{n}}{x_{n+1}}}=\frac{2\pi \zeta}{\sqrt{ 1-\zeta^2 }}$$

using the first to measurements is difficult because the first amplitude will have noise, so it is better to use later amplitudes
$$\frac{x_{1}}{x_{2}}=\frac{x_{2}}{x_{3}}=\dots$$

for very small damping ratios, the damping ratio can be simplified:
$$\zeta <<1\quad \zeta \approx \frac{\delta}{2\pi}$$

assumptions
- lumped mass
- stiffness proportional to displacement
- damping proportional to velocity
- linear time invariant
	- behavior of system does not change over time
- 2nd order differential equation

undamped natural frequency: $\omega_{n}=\sqrt{ \frac{k}{m} }$
...

EoM: 
$$m \ddot{x}+kx=0$$
response:
$$x(t)=C\cos(\omega_{n}t-\phi)$$
$$C=\sqrt{ x_{0}^2+\left( \frac{v_{0}}{\omega_{n}} \right)^2 }$$
$$\phi=\tan^{-1}{\frac{\zeta \omega_{n}x_{0}+v_{0}}{\omega_{d}x_{0}}}$$

C and $\phi$ are only dependent on initial conditions
$\omega_{n}$ is only dependent on the characteristics of the system

for a critically damped system
$$x(t)=e^{-\omega_{n}t}(x_{0}+t())$$
...

forced harmonic vibrations
EoM
$$m \ddot{x}+b \dot{x}+kx=F(t)$$
$$F(t)=A\sin\omega t+B\cos \omega t$$
and
$$\ddot{x}+2\zeta \omega_{n} \dot{x}+\omega^2_{n}x=F(t)$$
$$x(t)=\begin{bmatrix}
A & G(j\omega) & \sin \omega t+\phi
\end{bmatrix}$$
...
...

going back to chapter 8.3

the steady-state response to a sinusoidal input is known as the frequency response

$$G(s)=G(j\omega)$$
the right G function is called frequency response function (FRF)
$$G(j\omega)=|G(j\omega)|e^{j\phi}$$
$$|G(j\omega)|=\sqrt{ Re[G(j\omega)]^2+Im[G(j\omega)]^2 }$$
$$\phi=\angle G(j\omega)=\tan^{-1}{\frac{Im[G(j\omega)]}{Re[G(j\omega)]}}$$

given the transfer function
$$G(s)=\frac{X(s)}{F(s)}$$
X is output, F is input
$$f(t)=F_{0}\sin \omega t$$
using laplace of input function and transfer function, the output can be solved

$$x_{ss}(t)=F_{0}|G(j\omega)|\sin (\omega t+\phi)$$

note:
1. the response has the same frequency $\omega$ as the input
2. the amplitude of the response is scaled by $|G(j\omega)|$
3. The phase of the response is shifted by $\angle G(j\omega)$

if the input is cosine the frequency is cosine


frequency response of first-order again


$$\tau \dot{x}+x=f(t)$$
$$G(s)=\frac{1}{\tau s+1}=\frac{1}{j\tau \omega+1}$$
$$\frac{1}{1+j\tau \omega}(\frac{1-j\tau \omega}{1-j\tau \omega})=a+bj$$
now the magnitude and $\phi$ can be used with this form of $G(s)$

and plugged into 
$$x(t)=F_{0} | G(j\omega)|\sin \omega t + \phi$$

$$\dot{x}+2x=3\sin 2t$$
$$\frac{1}{2} \dot{x}+x=\frac{3}{2}\sin 2t$$
$$\tau= \frac{1}{2}\quad F_{0}=\frac{3}{2}\quad \omega=2$$

$$G(s)=\frac{1}{j+1} \frac{1-j}{1-j}=\frac{1-j}{1+j-j-j^2}=\frac{1}{2}-\frac{1}{2}j$$


## 4-21

Q1 of midterm 2 will have similar question on the final
a mechanical system where you write a state-space equation of motion 
See prob question 5 on pg257

problem 5.2 #8

run thru chapter 8
can find the frequency response by taking laplace and set $s=j\omega$

finding $G(j\omega)$ as a vector, either rectangular or polar

first and second order systems..

First Order
Transfer function
FRF: $G(j\omega)=\frac{1}{1+\tau \omega j}$
Mag and phase of FRF
Frequency response 
$$\frac{1}{1+\tau \omega j}\left( \frac{1-\tau \omega j}{1-\tau \omega j} \right)=\frac{1-\tau \omega j}{1+\tau^2\omega^2}$$
$$\frac{1}{1+\tau^2\omega^2}- \frac{\tau \omega}{1+\tau^2 \omega^2}j$$
$$|G|=\sqrt{ \left( \frac{1}{1+\tau^2 \omega^2} \right)^2+\left( -\frac{\tau \omega}{1+\tau^2 \omega^2} \right)^2 }=\sqrt{\frac{\tau^2 \omega^2+1}{1+2\tau^2\omega^2+\tau^4\omega^4} }$$
$$\angle G=-\tan^{-1}{\tau \omega}$$

$$\dot{x}+2x=3\sin 2t$$
$$\frac{1}{2}\dot{x}+x=\frac{3}{2}\sin 2t$$
$$x(t)=F_{0} | G(j\omega)|\sin \omega t + \phi$$
$$G(s)=\frac{1}{\frac{1}{2} s+1}=\frac{1}{j \frac{1}{2}2+1}$$
$$\left( \frac{1}{1+j} \right)\left( \frac{1-j}{1-j} \right)=\frac{1-j}{2}$$
$$\frac{1}{2}-\frac{1}{2}j\quad |G|=\frac{1}{\sqrt{ 2 }}\quad \angle G=-\frac{\pi}{4}$$
$$x(t)=\frac{3}{2\sqrt{ 2 }}\sin\left( 2t-\frac{\pi}{4} \right)$$

2nd order systems
FRF: 
$$G(j\omega)=\frac{1}{\omega_{n}^2-\omega^2+2\zeta \omega_{n}\omega j}$$
find the magnitude and phase of the FRF to solve the same equation
$$x_{ss}(t)=F_{0}|G(j\omega)|\sin (\omega t+\phi)$$

ex
$$\ddot{x}+2\dot{x}+4x=0.8\sin t$$
$$\omega_{n}^2=4\quad \zeta=\frac{1}{4}$$
$$F_{0}=0.8\quad \omega=1$$
$$s^2X(s)+2sX(s)+4X(s)=F(s)$$
$$\frac{X(s)}{F(s)}=\frac{1}{s^2+2s+4}$$
$$G(j\omega)=\frac{1}{3+2j}$$
$$|G|=\sqrt{ \left( \frac{3}{13} \right)^2+\left( \frac{2}{13} \right)^2 }$$
$$\angle G=-\tan^{-1} \frac{2}{3}$$
$$x_{ss}(t)=$$
next: ch 8.5


