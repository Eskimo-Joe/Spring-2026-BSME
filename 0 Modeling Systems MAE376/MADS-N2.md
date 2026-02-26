---
tags:
  - MAE376
---

example of a dynamic system
car suspension
uses a fourth order ODE to relate the input (bumps on road) to the output (vertical displacement of cabin)

Transfer function, changes sysstems uising laplace
LTI: linear time invariance system

$$x(t)\to y(t)$$
$$X(s)\to Y(s)$$
$$L[x(t)]=X(s)$$
The ratio of the laplace transform of the output (response function) to the Laplace transform of the input (driving function) assuming initial conditions are zero
Transfer function:
$$H(s)=\frac{L[\text{output}]}{L[\text{input}]}=\frac{Y(s)}{X(s)}$$
convolution in time property: 
$$h_{1}(t)*h_{2}(t)\to H_{1}(s)H_{2}(s)$$
Laplace is easier than convolution function! 
$$\frac{Y(s)}{X(s)}=\frac{b_{0}s^m+b_{1}s^{m-1}\dots}{a_{0}s^n+a_{1}s^{n-1}\dots}$$
cross multiples for simplicity

review laplace
$$L[f(t)]=F(s)=\int _{0}^\infty f(t)e^{-st} \, dt $$
table of formulas
![[lt.jpg|600]]

$$L[1]=\int _{0}^\infty e^{-st}\, dt =\frac{1}{-s}e^{-st}|_{0}^\infty=[0]-\frac{1}{-s}=\frac{1}{s}$$
$$L[e^{at}]=\int _{0}^\infty e^{at}e^{-st} \, dt=\int _{0}^\infty e^{(a-s)t} \, dt=\frac{e^{(a-s)t}}{a-s} |^\infty_{0}=\frac{1}{s-a} $$
$$L[\cos t]=\int _{0}^\infty \cos t e^{-st} \, dt=? $$
$$e^{iz}=\cos z+i\sin z$$
$$L[e^{iat}]=L[\cos at+ i\sin at]$$
$$L[e^{iat}]=\frac{1}{s-ai}\cdot \frac{s+ai}{s^2+a^2}=\frac{s+ai}{s^2+a^2}$$
$$L[\cos at]=\frac{s}{s^2+a^2}$$
$$L[\sin at]=\frac{a}{s^2+a^2}$$

integration by parts
$$\int u \, dv=uv-\int v \, du  $$
$$L[t]=\int_{0}^\infty te^{-st}\,dt$$
$$u=t;\quad du=dt$$
$$dv=e^{-st}dt;\quad v=-\frac{e^{-st}}{s}$$
$$L[t]=-\frac{t}{s}e^{-st}-\int -\frac{e^{-st}}{s} \, dt $$
$$=-\frac{t}{s}e^{-st}+\frac{1}{s}\left[ -\frac{e^{-st}}{s} \right] |_{0}^\infty=\dots=\frac{1}{s^2}$$

$$L[t^4]=\frac{4!}{s^{n+1}}=\frac{24}{s^5}$$
euler equations
$$g(t)=e^{at}f(t)$$
$$G(s)=F(s-a)$$
$$L[e^{-t}\cos t]=\frac{s+1}{(s+1)^2+1}=\frac{s+1}{s^2+2s+2}$$
also inverse laplace transforms 

Transfer functions are a property of the system irrelevant to the input

transfer functions include necessary units, and does not provide any information concerning the physical structure of the system
if the transfer function of a system is known, the output or response can be studied for various forms of input with a view toward understanding the nature of the system
if the transfer function of a system is unknown, it may be established experimentally by introducing known inputs and studying the output of the system. Once established, a transfer function gives a full description of the dynamic characteristics of the system, as distinct from its physical description

exam next week: laplace, complex numbers, ODEs


## 02-10

review laplace
MATLAB code: laplace()

laplace of derivatives and integrals
$$L\{\dot{x}(t)\}=s\cdot X(s)-x(0)$$
$$L\left\{ \int x(t) \, dx  \right\}=\frac{1}{s}\cdot X(s)$$

special functions
step function:
$$L\{u_{n}(t)\}=\frac{1}{s}$$
unit ramp function:
$$L\{u_{r}(t)\}=\frac{1}{s^2}$$
unit impulse function
missed

recall 
use laplace to change between time domain and s-domain

$$\ddot{x}+3 \dot{x}+2x=1$$
$$r^2+3r+2=0$$
$$(r+1)(r+2)=0$$
$$r_{1}=-1;\quad r_{2}=-2$$
$$x_{c}=C_{1}e^{-t}+C_{2}e^{-2t}$$
$$x_{p}=Ax+B$$
$$x_{p}'=A;\quad x_{p}''=0$$
$$3A+2Ax+2B=1$$
$$A=0;\quad B=\frac{1}{2}$$
$$x_{p}=\frac{1}{2}$$
$$x(t)=C_{1}e^{-t}+C_{2}e^{-2t}+\frac{1}{2}$$
$$x(0)=1;\quad \dot{x}(0)=0$$
$$x(0)=C_{1}+C_{2}+\frac{1}{2}=1$$
$$\dot{x}(t)=-C_{1}e^{-t}-2C_{2}e^{-2t}$$
$$\dot{x}(0)=-C_{1}-2C_{2}=0\to C_{1}=-2C_{2}$$
$$-2C_{2}+C_{2}=\frac{1}{2}\to C_{2}=-\frac{1}{2}$$
$$C_{1}=1$$
$$x(t)=e^{-t}-\frac{1}{2}e^{-2t}+\frac{1}{2}$$
$$L\{x(t)\}=X(s)=\frac{1}{s+1}-\frac{1}{2s+4}+\frac{1}{2s}$$
$$L\{\ddot{x}+3 \dot{x}+2x \}=L\{1\}$$
$$s^2X(s)-sx(0)-\dot{x}(0)+3[sX(s)-x(0)]+2X(s)=\frac{1}{s}$$
$$X(s)[s^2+3s+2]-3-s=\frac{1}{s}$$
$$X(s)=\frac{\frac{1}{s}+s+3}{s^2+3s+2}$$
solve with partial fraction decomposition
case 1: simple roots
case 2: repeated roots
case 3: complex roots

three roots:
$$X(s)=\frac{s^2+3s+1}{s(s+1)(s+2)}=\frac{A}{s}+\frac{B}{s+1}+\frac{C}{s+2}$$
$$A(s+1)(s+2)+Bs(s+2)+Cs(s+1)=s^2+3s+1$$
$$As^2+3As+2A+Bs^2+2Bs+Cs^2+Cs$$
$$A+B+C=1$$
$$3A+2B+C=3$$
$$2A=1$$
$$A=\frac{1}{2}$$
$$2B+C=\frac{3}{2}$$
$$B+C=\frac{1}{2}$$

MATLAB residue function for partial fraction decomp

Final value theorem
as $t\to \infty$ $x\to x_{ss}$

$$x_{ss}=\lim_{ s \to \infty } X(s)$$
$$X(s)=\frac{1}{s^2+4};\quad x_{ss}=0$$

inverse laplace
$$L^{-1}\left\{ \frac{1}{s+1} \right\}=e^{-t}$$

unit step function

$$L^{-1}\{\frac{2e^{-3s}}{2^2-4}\}=u_{3}(t)\sinh{2t}$$


$$L\{3u(t-2) \}=\frac{3}{s}L\{u_{2}(t)\}=\frac{3e^{-2s}}{s}$$
$$L^{-1}\left\{ \frac{e^{3s}}{s}  \right\}=u(t+3)$$


solve for this as hw
$$L^{-1}\{\frac{s^2+s+1}{s^3+s}\}$$



