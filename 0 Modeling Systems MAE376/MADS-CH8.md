

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




