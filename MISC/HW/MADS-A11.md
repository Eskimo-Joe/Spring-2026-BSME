---
tags:
  - MAE376
due: 2026-04-19
submitted: F
src:
---
Assignment 11
by Joseph Ramirez

## 8.1
#3
$$x_{1}(t)=A(1-e^{-3t})$$
$$x_{2}(t)=A(1-e^{-3t/2})$$
Assume $A=1$
![[Pasted image 20260418132552.png|500]]


`<div style="page-break-after: always;"></div>
#6 
$$RA\dot{h}+gh=Rq_{i}(t)\quad h(0)=0$$
$$q_{i}(t)=Bu(t)$$
$$\frac{RA}{g} \dot{h}+h=\frac{RB}{g}\quad \tau=\frac{RA}{g}$$
$$h(t)=\frac{RB}{g}(1-e^{-gt/RA})$$
$$h_{ss}=\frac{RB}{g}$$

#12 
$$\frac{1}{2}\dot{\omega}+5\omega=g(t)\quad g(t)=\frac{5}{2}u_{r}(t)\quad \omega(0)=\frac{2}{3}$$
$$\frac{1}{10}\dot{\omega}+\omega=\frac{1}{2}t$$
$$\tau=\frac{1}{10}\quad A=\frac{1}{2}$$
$$\omega(t)=\frac{2}{3}e^{-10t}+\frac{1}{2}\left[ t-\frac{1}{10}(1-e^{-10t}) \right]$$
$$\omega(t)=\left( \frac{2}{3}+\frac{1}{20} \right)e^{-10t}+\frac{1}{2}t-\frac{1}{20}$$
$$\omega_{ss}=\frac{1}{2}t-\frac{1}{20}$$
$$e_{ss}=\frac{1}{2}t-\left( \frac{1}{2}t-\frac{1}{20} \right)=\frac{1}{20}$$

`<div style="page-break-after: always;"></div>
## 8.2
#2
$$3 \ddot{x}+2 \dot{x}+x=0\quad x(0)=0\quad \dot{x}(0)=\frac{1}{3}$$
a. identify the damping type and find the free response
$$\ddot{x}+ \frac{2}{3} \dot{x}+\frac{1}{3} x=0$$
$$\omega_{n}=\frac{\sqrt{ 3 }}{3}\quad 2\zeta\left( \frac{\sqrt{ 3 }}{3} \right)=\frac{2}{3}$$
$$\zeta=\frac{\sqrt{ 3 }}{3}\approx.577$$
the system is underdamped

$$\omega_{d}=\omega_{n}\sqrt{ 1-\zeta^2 }=\frac{\sqrt{ 3 }}{3}\sqrt{ 1-\frac{1}{3} }=\frac{\sqrt{ 2 }}{3}$$
$$x(t)=e^{- t/3}\left[ \frac{\sqrt{ 2 }}{2}\sin (\frac{\sqrt{ 2 }}{3}t) \right]$$

b. plot the free response by using the initial command

$$\ddot{x}+ \frac{2}{3} \dot{x}+\frac{1}{3} x=0$$
$$x_{1}=x\quad x_{2}=\dot{x}$$
$$\dot{x}_{2}=-\frac{2}{3}x_{2}-\frac{1}{3}x_{1}$$
$$\begin{bmatrix}
\dot{x}_{1} \\
\dot{x}_{2}
\end{bmatrix}=\begin{bmatrix}
0 & 1 \\
-\frac{1}{3} & -\frac{2}{3} 
\end{bmatrix} \begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}$$
![[Pasted image 20260418222610.png|500]]

`<div style="page-break-after: always;"></div>
#4 
$$4 \ddot{x} + 8 \dot{x}+ 3x=0\quad x(0)=1\quad \dot{x}(0)=-1$$

a. identify the damping type and find the free response
$$\ddot{x}+4 \dot{x}+ \frac{3}{8}x=0$$
$$\omega_{n}=\frac{\sqrt{ 3 }}{2\sqrt{ 2 }}=\frac{\sqrt{ 6 }}{4}$$
$$2\zeta\left( \frac{\sqrt{ 6 }}{4} \right)=4\quad \zeta=\frac{4\sqrt{ 6 }}{3}\approx 3.266$$
overdamped system
$$s_{1}=-\zeta \omega_{n}+\omega_{n}\sqrt{ \zeta^2-1 }=-0.096$$
$$s_{2}=-\zeta \omega_{n}-\omega_{n}\sqrt{ \zeta^2-1}=-3.904$$

$$x(t)=\frac{-s_{2}x_{0}-1}{s_{1}-s_{2}}e^{s_{1}t}-\frac{-s_{1}x_{0}-1}{s_{1}-s_{2}}e^{s_{2}t}=0.763e^{-0.096t}+3.442e^{-3.904t}$$

b. plot the free response by using the initial command
$$\ddot{x}+4 \dot{x}+ \frac{3}{8}x=0$$
$$x_{1}=x\quad x_{2}=\dot{x}\quad \dot{x}_{2}=\ddot{x}$$
$$\dot{x}_{2}=-\frac{3}{8}x_{1}-4x_{2}$$
$$\begin{bmatrix}
\dot{x}_{1} \\
\dot{x}_{2}
\end{bmatrix}=\begin{bmatrix}
0 & 1 \\
-\frac{3}{8} & -4
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}$$
![[Pasted image 20260418225855.png|500]]

`<div style="page-break-after: always;"></div>
#7 

$$\ddot{x}+2 \dot{x}+ 2x=10\delta(t)\quad x(0)=0\quad \dot{x}(0)=0$$
$$\omega_{n}=\sqrt{ 2 } \quad \zeta=\frac{1}{\sqrt{ 2 }}$$
$$\omega_{d}=\omega_{n}\sqrt{ 1-\zeta^2 }=1$$
$$s^2X+2sX+2X=10$$
$$X(s)=\frac{10}{s^2+2s+2}=\frac{10}{(s+1)(s+1)}$$
$$x(t)=10e^{-t}\sin t$$
$$x_{ss}=\lim_{ t \to \infty } (10e^{-t}\sin t)=0$$

---

#8 
$$\ddot{x}+\dot{x}+0.89x=\delta(t-1)$$
$$x(0)=0\quad \dot{x}(0)=0$$
$$\omega_{n}=0.943\quad \zeta=0.53$$
$$\omega_{d}=\omega_{n}\sqrt{ 1-\zeta^2 }=0.8$$

$$s^2X(s)-sx(0)-\dot{x}(0)+2\zeta \omega_{n}(sX(s)-x(0))+\omega_{n}^2X(s)=A$$
$$(s^2+2\zeta \omega_{n}s+\omega_{n}^2)X(s)=sx(0)+\dot{x}(0)+2\zeta \omega_{n}x(0)+A$$
$$X(s)=\frac{x(0)(2\zeta \omega_{n}+s)+\dot{x}(0)+A}{s^2+2\zeta \omega_{n}+\omega_{n}^2}$$
$$X(s)=\frac{1}{s^2+1s+0.89}$$
$$X(s)=\frac{1}{\left( s+\frac{1}{2} \right)^2+0.89-0.25}=\frac{1}{(s+0.5)^2+0.64}=\frac{1}{(s+0.5)^2+0.8^2}$$
$$x(t)=\frac{5}{4}L^{-1}\left\{ \frac{0.8}{(s+0.5)^2+0.8^2}  \right\}=\frac{5}{4}e^{-t/2}\sin(0.8t)$$
$$x(t)=\frac{1}{\omega_{d}}e^{-\zeta \omega_{n}t}\sin(\omega_{d}t)$$
$$\omega_{d}=0.8\quad \zeta \omega_{n}=\frac{1}{2}$$
`<div style="page-break-after: always;"></div>

#9 
$$\ddot{x}+4\dot{x}+x=5\delta(t)$$
$$X(s)=\frac{5}{s^2+4s+1}$$
![[Pasted image 20260420000811.png|500]]

`<div style="page-break-after: always;"></div>

#14
$$9\ddot{x}+6\dot{x}+5x=10\delta(t)$$
$$\ddot{x}+\frac{2}{3}\dot{x}+\frac{5}{9}x=10\delta(t)$$
$$x(0)=\frac{1}{2}\quad \dot{x}(0)=0$$
$$\omega_{n}=\frac{\sqrt{ 5 }}{3}\quad 2\zeta\left( \frac{\sqrt{ 5 }}{3} \right)=\frac{2}{3}\quad \zeta=\frac{1}{\sqrt{ 5 }}\approx.447$$
$$\omega_{d}=\omega_{n}\sqrt{ 1-\zeta^2 }=\frac{2}{3}$$
underdamped system:
$$x(t)=e^{-t/3}\left( \frac{1}{2}\cos\left( \frac{2}{3}t \right)+\frac{\frac{1}{2}\cdot \frac{2}{3}+10}{\frac{2}{3}}\sin\left( \frac{2}{3}t \right) \right)$$
$$x(t)=e^{-t/3}\left( \frac{1}{2}\cos\left( \frac{2}{3}t \right)+15.5\sin\left( \frac{2}{3}t \right) \right)$$
![[Pasted image 20260420012122.png|500]]

`<div style="page-break-after: always;"></div>

#21
$$m_{1}\ddot{x}_{1}=-k_{1}x_{1}+k_{2}(x_{2}-x_{1})+b(\dot{x}_{2}-\dot{x}_{1})+f_{1}$$
$$0.7\ddot{x}_{1}+0.6(\dot{x}_{1}-\dot{x}_{2})+5x_{1}+2(x_{1}-x_{2})=5u(t)$$
$$\ddot{x}_{1}+\frac{6}{7}\dot{x}_{1}-\frac{6}{7}\dot{x}_{2}+10x_{1}-\frac{20}{7}x_{2}=\frac{50}{7}u(t)$$

$$\ddot{x}_{2}=k_{2}(x_{1}-x_{2})-b(\dot{x}_{2}-\dot{x}_{1})+f_{2}$$
$$\ddot{x}_{2}+0.6(\dot{x}_{2}-\dot{x}_{1})+2(x_{2}-x_{1})=u(t)$$
$$\ddot{x}_{2}+\frac{3}{5}\dot{x}_{2}-\frac{3}{5}\dot{x}_{1}+2x_{2}-2x_{1}=u(t)$$

$$x_{1}=x_{1}\quad x_{2}=x_{2}\quad x_{3}=\dot{x}_{1}\quad \dot{x}_{3}=\ddot{x}_{1}\quad x_{4}=\dot{x}_{2}\quad \dot{x}_{4}=\ddot{x}_{2}$$
$$\begin{bmatrix}
\dot{x}_{1} \\
\dot{x}_{2} \\
\dot{x}_{3} \\
\dot{x}_{4}
\end{bmatrix}=\begin{bmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
-10 & \frac{20}{7} & \frac{-6}{7} & \frac{6}{7} \\
2 & -2 & \frac{3}{5} & -\frac{3}{5}
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4}
\end{bmatrix}+\begin{bmatrix}
0 \\
0 \\
\frac{50}{7} \\
1
\end{bmatrix}u(t)$$
![[Pasted image 20260420102006.png|500]]

`<div style="page-break-after: always;"></div>
#24
$$m\ddot{x}_{1}=f_{1}-k_{1}x_{1}-b_{1}\dot{x}_{1}+k_{2}(x_{2}-x_{1})+b_{2}(\dot{x}_{2}-\dot{x}_{1})$$
$$\ddot{x}_{1}=f_{1}-20x_{1}+10x_{2}-13\dot{x}_{1}+8\dot{x}_{2}$$
$$\ddot{x}_{1}+13\dot{x}_{1}+20x_{1}-8\dot{x}_{2}-10x_{2}=f_{1}$$
$$0=f_{2}-k_{2}(x_{2}-x_{1})-b_{2}(\dot{x}_{2}-\dot{x}_{1})$$
$$8\dot{x}_{2}+10x_{2}-8\dot{x}_{1}-10x_{1}=f_{2}$$
$$\dot{x}_{2}=\dot{x}_{1}+\frac{5}{4}x_{1}-\frac{5}{4}x_{2}+\frac{1}{8}f_{2}$$

![[Pasted image 20260420104124.png|500]]

`<div style="page-break-after: always;"></div>

#27
$$ 8\ddot{x}+4\dot{x}+5x=\frac{3}{5}e^{-t/3}\sin t\quad x(0)=\frac{2}{3}\quad \dot{x}(0)=0$$
$$0\leq t\leq 15$$
$$\ddot{x}+\frac{1}{2}\dot{x}+\frac{5}{8}x=\frac{3}{40}e^{-t/3}\sin t$$
$$\omega_{n}=\frac{\sqrt{ 5 }}{2\sqrt{ 2 }}\quad \zeta=\frac{\sqrt{ 2 }}{2\sqrt{ 5 }}\approx 0.316$$
$$8r^2+4r+5=0$$
$$r=\frac{-4\pm\sqrt{ 16-160 }}{16}=-\frac{1}{4}\pm \frac{\sqrt{ -144 }}{16}$$
$$r=-\frac{1}{4}\pm \frac{3}{4}i$$

$$s^2X(s)-\frac{2}{3}s+\frac{1}{2}\left( sX(s)-\frac{2}{3} \right)+\frac{5}{8}X(s)=\frac{3}{5}\left( \frac{1}{\left( s+\frac{1}{3} \right)^2+1} \right)$$
$$\left( s^2+\frac{1}{2}s+\frac{5}{8} \right)X(s)-\frac{2}{3}s-\frac{1}{3}=\frac{3}{5}\left( \frac{1}{s^2+\frac{2}{3}s+\frac{10}{9}} \right)$$




#29
#30


