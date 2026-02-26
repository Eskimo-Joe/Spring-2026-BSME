

mechanical systems

moving parts
physical systems can be static or dynamic

static depends on only current situation without memory
dynamic systems depend on time and have memory

lots of first order ODE

$$\dot{x}=\frac{dx}{dt}=f(x(t),u(t),t)$$

x = state vecot
u = control input vector
basic elements of mechanical systems
three passive, linear components
- a
- b
- c

linear or rotational motion
mass energy sotrage element (spring) - kinetic energy
$$F=m \ddot{x}$$

inertia
$$\text{Torque}=J\alpha=J \ddot{\theta}$$
potential energy
$$F=k(x-x_{0})$$
$$T=k(\theta-\theta_{0})$$
k is spring stiffness 

viscous damper: energy dissipative element
$$F=c \dot{x}$$
$$T=D \dot{\theta}$$
c and D are damping coefficient

free body diagrams

stick to x and its derivatives

$$\sum F=F-kx-c \dot{x}=m \ddot{x}$$
$$m \ddot{x}+c \dot{x}+kx=F$$

friction $$F=m \ddot{x}-c \dot{x}$$


## 02-24

new ppt
modeling suspension system of a car
Newtons 2nd law and rotational equivalent

some review
FBD

$$\sum F=ma=m \ddot{x}$$
$$F-c \dot{x}-kx=m \ddot{x}$$

find transfer function of spring-dampener system

$$m \ddot{x}+c \dot{x}+kx=F$$
$$T=\frac{X(s)}{F(s)}$$
$$m(s^2X(s)-sx(0)-\dot{x}(0))+c(sX(s)-x(0))+kX(s)=F(s)$$
assume initial conditions are zero..
$$X(s)(ms^2+cs+k)=F(s)$$
$$\frac{X(s)}{F(s)}=\frac{1}{ms^2+cs+k}$$

draws feedback system diagram using transfer function and sensor feeback

translational spring
parallel springs:
$$k_{1}x+k_{2}x=F$$
$$(k_{1}+k_{2})x=F$$
$$k_{eq}=k_{1}+k_{2}$$
series springs:
$$k_{1}x_{1}=k_{2}x_{2}=F$$
$$x_{eq}=x_{1}+x_{2}$$
$$\frac{F}{k_{eq}}=\frac{F}{k_{1}}+\frac{F}{k_{2}}$$

example 1:
$$\frac{F}{k_{eq}}=\frac{F}{k_{1}+k_{2}}+\frac{F}{k_{3}}$$
$$F(k_{1}+k_{2})=k_{eq}\left( F+\frac{F(k_{1}+k_{2})}{k_{3}} \right)$$
$$k_{eq}=\frac{F(k_{1}+k_{2})}{F+\frac{F(k_{1}+k_{2})}{k_{3}}}=\frac{k_{1}+k_{2}}{1+ \frac{k_{1}+k_{2}}{k_{3}}}$$
wrong
$$\frac{1}{k_{eq}}=\frac{1}{k_{1}+k_{2}}+\frac{1}{k_{3}}$$

example 2:
$$\frac{F}{k_{eq_{1}}}=\frac{F}{k_{2}}+\frac{F}{k_{3}}$$
$$k_{eq_{1}}=\frac{F}{\frac{F}{k_{2}}+\frac{F}{k_{3}}}=\left( \frac{1}{k_{2}}+\frac{1}{k_{3}} \right)^{-1}$$
$$k_{eq}=k_{1}+\left( \frac{1}{k_{2}}+\frac{1}{k_{3}} \right)^{-1}$$
wrong
$$\frac{1}{k_{eq}}=\frac{1}{k_{1}}+\frac{1}{k_{2}+k_{3}}$$

damper in parallel
$$C_{eq}=C_{1}+C_{2}$$
damper in series
$$C_{eq}=\frac{C_{1}C_{2}}{C_{1}+C_{2}}$$

equation of motion of a simple spring mass system without dampening
$$F-kx=m \ddot{x}$$

example 5
$$F-kx_{1}-B \dot{x}$$
$$F-k(x_{1}-x_{2})=m \ddot{x}$$
$$F-Bx_{2}=m \ddot{x}$$
example



