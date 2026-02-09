---
tags:
  - MAE376
due: 2026-02-08
submitted: T
src:
---
## 1. $\dot{x} +\frac{1}{3}x=\cos 2t;\quad x(0)=1$
$$p(t)=\frac{1}{3};\quad g(t)=\cos 2t$$
$$\mu(t)=e^{\int p(t) \, dt }=e^{t/3}$$
$$x(t)=\frac{\int \mu(t)g(t) \, dt }{\mu(t)}=\frac{\int e^{t/3}\cos 2t \, dt }{e^{t/3}}$$
$$u=e^{t/3};\quad du=\frac{e^{t/3}}{3}dt$$
$$dv=\cos 2t dt;\quad v=\frac{1}{2}\sin 2t$$
$$\int e^{t/3}\cos 2t \, dt =\frac{1}{2}e^{t/3}\sin 2t-\int \frac{1}{2}\sin 2t \cdot \frac{e^{t/3}}{3}\, dt $$
$$\int e^{t/3}\cos 2t \, dt =\frac{1}{2}e^{t/3}\sin 2t-\frac{1}{6}\left[ -\frac{1}{2}e^{t/3}\cos 2t-\int -\frac{1}{2}\cos 2t\cdot  \frac{e^{t/3}}{3} \, dt  \right]$$
$$\int e^{t/3}\cos 2t \, dt =\frac{1}{2}e^{t/3}\sin 2t+\frac{1}{12}e^{t/3}\cos 2t-\frac{1}{36} \int \cos 2t\cdot  e^{t/3}\, dt  $$
$$\int e^{t/3}\cos 2t \, dt =\frac{36}{37}\left[ \frac{1}{2}e^{t/3}\sin 2t+\frac{1}{12}e^{t/3}\cos 2t \right]$$
$$\int e^{t/3}\cos 2t \, dt =\frac{18}{37}e^{t/3}\sin 2t+ \frac{3}{37}e^{t/3}\cos 2t+C$$
$$x(t)=\frac{18}{37}\sin 2t + \frac{3}{37} \cos 2t+C$$
$$\frac{18}{37}\sin 0+\frac{3}{37}\cos 0+C=1$$
$$C=1-\frac{3}{37}=\frac{34}{37}$$
$$x(t)=\frac{18}{37}\sin 2t+ \frac{3}{37}\cos 2t + \frac{34}{37}$$

`<div style="page-break-after: always;"></div>
## 2. $\frac{1}{2} \dot{x}+tx=\frac{1}{2}t;\quad x(0)= \frac{1}{3}$
$$\dot{x}+2tx=t$$
$$p(t)=2t;\quad \mu(t)=e^{\int 2t \, dt }=e^{t^2}$$
$$x(t)=\frac{\int e^{t^2}\cdot t \, dt }{e^{t^2}}$$
$$u=e^{t^2};\quad du=2te^{t^2}dt$$
$$\int te^{t^2} \, dt= \int \frac{1}{2} \, du=\frac{1}{2}u=\frac{e^{t^2}}{2} +C$$
$$x(t)=\frac{1}{2}+C$$
$$\frac{1}{2}+C=\frac{1}{3}\to C=-\frac{1}{6}$$
$$x(t)=\frac{1}{3}$$

`<div style="page-break-after: always;"></div>
## 3. $(t-1) \dot{u}+tu=2t;\quad u(0)=1$

$$\dot{u}+\frac{t}{t-1}u=\frac{2t}{t-1}$$
$$\mu(t)=e^{\int t/(t-1) \, dt }=e^{\int 1-t^{-1} \, dt }=e^{t+\ln|t-1|}=|t-1|e^{t}$$
$$u=\frac{\int |t-1|e^{t}\cdot 2t \, dt }{|t-1|e^{t}}=\frac{2e^{t}(t^2-3t+3)+C}{(t-1)e^{t}}$$
$$u=2t-4+C$$
$$-4+C=1\to C=5$$
$$u(t)=2t+1$$

`<div style="page-break-after: always;"></div>
## 4. $\dot{ u}=(1-u) \cos t;\quad u(0)=\frac{1}{2}$

$$\dot{u}+\cos t\,u=\cos t$$
$$\mu(t)=e^{\int \cos t \, dt }=e^{\sin t}$$
$$u(t)=\frac{\int e^{\sin t}\cos t \, dt }{e^{\sin t}}$$
$$u=e^{\sin t};\quad du=e^{\sin t}\cos t\,dt$$
$$\int e^{\sin t}\cos t \, dt=\int  \, du=u  $$
$$u(t)=\frac{e^{\sin t}+C}{e^{\sin t}}=1+Ce^{-\sin t}$$
$$1+Ce^{-\sin 0}=\frac{1}{2}\to C=-\frac{1}{2}$$
$$u(t)=1-\frac{1}{2}e^{-\sin t}$$

`<div style="page-break-after: always;"></div>

## 5. $\ddot{x}+4 \dot{x}+4x=e^{-t};\quad x(0)=1;\quad \dot{x}(0)=1$

$$r^2+4r+4=0$$
$$(r+2)^2=0$$
$$r_{1}=r_{2}=-2$$
$$x_{c}=C_{1}e^{-2t}+C_{2}te^{-2t}$$
$$x_{p}=Ae^{-t};\quad x'=-Ae^{-t};\quad x''=Ae^{-t}$$
$$Ae^{-t}-4Ae^{-t}+4Ae^{-t}=e^{-t}$$
$$Ae^{-t}=e^{-t}\to A=1$$
$$x=C_{1}e^{-2t}+C_{2}te^{-2t}+e^{-t}$$
$$C_{1}+1=1\to C_{1}=0$$
$$x'=-2C_{2}te^{-2t}+C_{2}e^{-2t}+e^{-t}$$
$$C_{2}+1=1\to C_{2}=0$$
$$x(t)=e^{-t}$$

`<div style="page-break-after: always;"></div>
## 6. $\ddot{x}+4x=t;\quad x(0)=0;\quad \dot{x}(0)=1$
$$r^2+4=0$$
$$r^2=-4$$
$$r=\pm 2i$$
$$x_{c}=C_{1}\cos 2t+C_{2}\sin 2t$$
$$x_{p}=A+Bt;\quad x'=B;\quad x''=0$$
$$4A+4Bt=t$$
$$A=0;\quad B=\frac{1}{4}$$
$$x_{p}=\frac{t}{4}$$
$$x(t)=C_{1}\cos 2t+C_{2} \sin 2t+ \frac{t}{4}$$
$$C_{1}+0+0=0\to C_{1}=0$$
$$\dot{x}=2C_{2}\cos 2t+\frac{1}{4}$$
$$2C_{2}+\frac{1}{4}=1\to C_{2}=\frac{3}{8}$$
$$x(t)=\frac{3}{8}\sin 2t+\frac{t}{4}$$

`<div style="page-break-after: always;"></div>
## 7. $\ddot{x}+x=\sin t;\quad x(0)=1;\quad \dot{x}(0)=0$
$$r^2+1=0$$
$$r=\pm i$$
$$x_{c}=C_{1}\cos t+C_{2}\sin t$$
$$x_{p}=At\sin t+Bt\cos t$$
$$x_{p}'=At\cos t+A\sin t-Bt\sin t+B\cos t$$
$$x_{p}''=-At\sin t+A\cos t+A\cos t-Bt\cos t-B\sin t-B\sin t$$
$$x_{p}''=-At\sin t+2A\cos t-Bt\cos t-2B\sin t$$
$$2A\cos t-2B\sin t=\sin t$$
$$A=0;\quad B=-\frac{1}{2}$$
$$x_{p}=-\frac{1}{2}t\cos t$$
$$x(t)=C_{1}\cos t+C_{2}\sin t-\frac{1}{2}t\cos t$$
$$x(0)=C_{1}=1$$
$$x'(t)=-\sin t+C_{2}\cos t+\frac{1}{2}t\sin t-\frac{1}{2}\cos t$$
$$x'(0)=C_{2}-\frac{1}{2}=0\to C_{2}=\frac{1}{2}$$
$$x(t)=\cos t+\frac{1}{2}\sin t-\frac{1}{2}t\cos t$$

`<div style="page-break-after: always;"></div>
## 8. $\ddot{x}+ 4\dot{x}+3x=2e^{-3t};\quad x(0)=0;\quad \dot{x}(0)=-1$
$$r^2+4r+3=0$$
$$(r+3)(r+1)=0$$
$$r_{1}=-3;\quad r_{2}=-1$$
$$x_{c}=C_{1}e^{-3t}+C_{2}e^{-t}$$
$$x_{p}=Ate^{-3t};\quad x_{p}'=-3Ate^{-3t}+Ae^{-3t}$$
$$x_{p}''=9Ate^{-3t}-2Ae^{-3t}$$
$$9Ate^{-3t}-2Ae^{-3t}-12Ate^{-3t}+4Ae^{-3t}+3Ate^{-3t}=2e^{-3t}$$
$$2Ae^{-3t}=2e^{-3t}\to A=1$$
$$x_{p}=te^{-3t}$$
$$x(t)=C_{1}e^{-3t}+C_{2}e^{-t}+te^{-3t}$$
$$C_{1}+C_{2}=0\to C_{1}=-C_{2}$$
$$x'(t)=-3C_{1}e^{-3t}-C_{2}e^{-t}-3te^{-3t}+e^{-3t}$$
$$-3C_{1}-C_{2}+1=-1$$
$$2C_{2}=-2\to C_{2}=-1\to C_{1}=1$$
$$x(t)=e^{-3t}-e^{-t}+te^{-3t}$$

`<div style="page-break-after: always;"></div>
## 9. $6\ddot{u}+7 \dot{u}+2u=65\cos t;\quad u(0)=0;\quad \dot{u}(0)=5$
$$6r^2+7r+2=0$$
$$r=\frac{-7\pm\sqrt{ 49-48 }}{12}$$
$$r_{1}=-\frac{2}{3};\quad r_{2}=-\frac{1}{2}$$
$$u_{c}=C_{1}e^{-2t/3}+C_{2}e^{-t/2}$$
$$u_{p}=A\cos t+B\sin t$$
$$u_{p}'=-A\sin t+B\cos t$$
$$u_{p}''=-A\cos t-B\sin t$$
$$-6A\cos t-6B\sin t-7A\sin t+7B\cos t+2A\cos t+2B\sin t=65\cos t$$
$$7B-4A=65$$
$$-4B-7A=0\to A=-\frac{4}{7}B$$
$$7B-4\left( -\frac{4}{7}B \right)=65$$
$$B\left( \frac{65}{7} \right)=65\to B=7\to A=-4$$
$$u_{p}=-4\cos t+7\sin t$$
$$u(t)=C_{1}e^{-2t/3}+C_{2}e^{-t/2}-4\cos t+7\sin t$$
$$u(0)=C_{1}+C_{2}-4=0\to C_{1}=4-C_{2}$$
$$u'(t)=-\frac{2}{3}C_{1}e^{-2t/3}-\frac{1}{2}C_{2}e^{-t/2}+4\sin t+7\cos t$$
$$u'(0)=-\frac{2}{3}C_{1}-\frac{1}{2}C_{2}+7=5$$
$$-\frac{2}{3}(4-C_{2})-\frac{1}{2}C_{2}=2$$
$$-\frac{8}{3}+\frac{1}{6}C_{2}=2\to C_{2}=6\cdot \frac{14}{3}=28$$
$$C_{1}=4-28=-24$$
$$u(t)=-24e^{-2t/3}+28e^{-t/2}-4\cos t+7\sin t$$

`<div style="page-break-after: always;"></div>
## 10. $4 \ddot{u}+4 \dot{u}+5u=0;\quad u(0)=0;\quad \dot{u}(0)=1$
$$4r^2+4r+5=0$$
$$r=\frac{-4\pm\sqrt{ 16-80 }}{8}=\frac{-4\pm 8i}{8}=-\frac{1}{2}\pm i$$
$$u_{c}=C_{1}e^{-t/2}\cos t+C_{2}e^{-t/2}\sin t$$
$$u(0)=C_{1}=0$$
$$u'(t)=-\frac{1}{2}C_{2}e^{-t/2}\sin t +C_{2}e^{-t/2}\cos t$$
$$u'(0)=C_{2}=1$$
$$u(t)=e^{-t/2}\sin t$$


