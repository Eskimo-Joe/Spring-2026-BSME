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
![[lt.jpg|400]]

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




