---
tags:
  - MAE376
due: 2026-03-08
submitted: F
src: https://csulb.instructure.com/courses/117006/assignments/1712602
---
by Joseph Ramirez

1-1
$$F(s)=\frac{e^{-2s}}{s}+\frac{6e^{-3s}}{s}$$
$$f(t)=u_{2}(t)+6u_{3}(t)$$

1-2
$$F(s)=e^{-3s}\left( \frac{1}{s^2}+\frac{5}{s^3} \right)$$
$$f(t)=u_{3}(t)(t-3) + \frac{5u_{3}(t)(t-3)^2}{2}$$

1-3
$$F(s)=6+\frac{e^{-s}}{s^2+4}$$
$$f(t)=6\delta(t)+\frac{u_{1}\sin(2t-2)}{2}$$

1-4
$$F(s)=\frac{e^{-5s}(s+1)}{(s+1)^2+16}$$
$$F(s)=\frac{e^{-5s}}{(s+1)^2+10}+\frac{s+1}{(s+1)^2+10}$$
$$f(t)=u_{5}(t)f_{1}(t-5)+e^{-t}\cos{\sqrt{ 10 }t}$$
$$f_{1}(t)=L^{-1}\left\{ \frac{1}{(s+1)^2+10} \right\}=\frac{1}{\sqrt{ 10 }}L^{-1}\left\{ \frac{\sqrt{ 10 }}{(s+1)^2+10} \right\}$$
$$f_{1}(t)=\frac{e^{-t}\sin{\sqrt{ 10 }t}}{\sqrt{ 10 }}$$
$$f_{1}(t-5)=\frac{e^{5-t}\sin{(\sqrt{ 10 }(t-5))}}{\sqrt{ 10 }}$$
$$f(t)=\frac{u_{5}(t)}{\sqrt{ 10 }}(e^{-t+5}\sin{\sqrt{ 10 }t})+e^{-t}\cos{\sqrt{ 10 }t}$$

1-5
$$F(s)=\frac{4e^{-2s}}{s-3}+\frac{e^{-5s}}{s+9}$$
$$f(t)=u_{2}(t)f_{1}(t-2)+u_{5}(t)f_{2}(t-5)$$
$$f_{1}(t)=L^{-1}\left\{ \frac{4}{s-3} \right\}=4L^{-1}\left\{ \frac{1}{s-3} \right\}=4e^{3t}$$
$$f_{2}(t)=L^{-1}\left\{ \frac{1}{s+9} \right\}=e^{-9t}$$
$$f(t)=4u_{2}(t)e^{3t-6}+u_{5}(t)e^{-9t+45}$$

1-6
$$F(s)=\frac{e^{-10s}}{(s-3)^2}$$
$$f(t)=u_{10}(t)f_{1}(t-10)$$
$$f_{1}(t)=L^{-1}\{\frac{1}{(s-3)^2}\}$$
$$(s-3)^2=s^2-6s+9=(s-4)(s-2)+1$$



1-7
$$\frac{e^{-7s}}{s}+\frac{e^{-11s}}{(s-2)^3}$$

1-8
$$F(s)=\frac{1}{(s+1)(s^2-1)}$$
$$f(t)=\frac{1}{4}e^{t}-\frac{1}{4}e^{-t}-\frac{1}{2}te^{-t}$$


1-9
$$F(s)=\frac{2s+3}{s^2+4s+13}=\frac{2s}{(s+2)^2+9}+\frac{3}{(s+2)^2+9}$$
$$f(t)=$$


1-10
$$F(s)=\frac{e^{-3s}}{s-2}$$

1-11
$$F(s)=\frac{1+e^{-2s}}{s^2+6}$$


2-1
$$f(t)=3u_{6}(t)$$

2-2
$$g(t)=3+7u_{5}(t)-10u_{8}(t)$$

2-3
$$h(t)=6u_{3}(t)\sin(t-3)$$

2-4
$$j(t)=4+5u_{2}(t-2)e^{t-2}$$

2-5
$$u(t)=u_{7}(t)(t-7)^3$$

2-6
$$v(t)=5+u_{1}(t)(t-5)$$

2-7
$$w(t)=2+u_{4}(t)(t^2-2)$$

3. solve the following IVP problem using Laplace transform
3-1
$$y''-1y'+9y=5t^2;\quad y(0)=2;\quad y'(0)=-1$$

3-2
$$y''(t)+4y'(t)=\cos(t)+4t+12;\quad y(0)=0;\quad y'(0)=7$$




