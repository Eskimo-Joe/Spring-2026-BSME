---
tags:
  - MAE376
due: 2026-03-08
submitted: T
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
$$f_{1}(t)=L^{-1}\{\frac{1}{(s-3)^2}\}=e^{3t}t$$
$$f(t)=u_{10}(t)e^{3t-30}(t-10)$$

1-7
$$F(s)=\frac{e^{-7s}}{s}+\frac{e^{-11s}}{(s-2)^3}$$
$$f(t)=u_{7}(t)f_{1}(t-7)+u_{11}(t)f_{2}(t-11)$$
$$f_{1}(t)=L^{-1}\left\{ \frac{1}{s} \right\}=1$$
$$f_{2}(t)=L^{-1}\left\{ \frac{1}{(s-2)^3} \right\}=\frac{e^{2t}t^2}{2}$$
$$f(t)=u_{7}(t)+\frac{u_{11}(t)e^{2t-22}(t-11)^2}{2}$$

1-8
$$F(s)=\frac{1}{(s+1)(s^2-1)}$$
$$f(t)=\frac{1}{4}e^{t}-\frac{1}{4}e^{-t}-\frac{1}{2}te^{-t}$$

1-9
$$F(s)=\frac{2s+3}{s^2+4s+13}=\frac{2(s+2)}{(s+2)^2+9}-\frac{1}{3}\cdot  \frac{3}{(s+2)^2+9}$$
$$f(t)=2e^{-2t}\cos 3t -\frac{1}{3}e^{-2t}\sin 3t$$

1-10
$$F(s)=\frac{e^{-3s}}{s-2}$$
$$f(t)=u_{3}(t)f_{1}(t-3)$$
$$f_{1}(t)=L^{-1}\left\{ \frac{1}{s-2} \right\}=e^{2t}$$
$$f(t)=u_{3}(t)e^{2t-6}$$

1-11
$$F(s)=\frac{1+e^{-2s}}{s^2+6}=\frac{1}{s^2+6}+\frac{e^{-2s}}{s^2+6}$$
$$f(t)=\frac{1}{\sqrt{ 6 }}(\sin \sqrt{ 6 }t+u_{2}(t)\sin \sqrt{ 6 }(t-2))$$

2-1
$$f(t)=3u_{6}(t)$$
$$F(s)=\frac{3e^{-6s}}{s}$$

2-2
$$g(t)=3+7u_{5}(t)-10u_{8}(t)$$
$$G(s)=\frac{3}{s}+\frac{7e^{-5s}}{s}-\frac{10e^{-8s}}{s}$$

2-3
$$h(t)=6u_{3}(t)\sin(t-3)$$
$$H(s)=\frac{6e^{-3s}}{s^2+1}$$

2-4
$$j(t)=4+5u_{2}(t-2)e^{t-2}$$
$$J(s)=\frac{4}{s}+e^{-2s}L\{5te^{t}\}$$
$$J(s)=\frac{4}{s}+\frac{5e^{-2s}}{(s-1)^2}$$


2-5
$$u(t)=u_{7}(t)(t-7)^3$$
$$U(s)=e^{-7s}L\{t^3 \}$$
$$U(s)=\frac{6e^{-7s}}{s^4}$$

2-6
$$v(t)=5+u_{1}(t)(t-5)$$
$$V(s)=\frac{5}{s}+e^{-s}L\{t-4 \}$$
$$V(s)=\frac{5}{s}+e^{-s}\left( \frac{1}{s^2}-\frac{4}{s} \right)$$

2-7
$$w(t)=2+u_{4}(t)(t^2-2)$$
$$W(s)=\frac{2}{s}+e^{-4s}L\{t^2+8t+14\}$$
$$W(s)=\frac{2}{s}+e^{-4s}\left( \frac{2}{s^3}+\frac{8}{s^2}+\frac{14}{s} \right)$$


3. solve the following IVP problem using Laplace transform
3-1
$$y''-1y'+9y=5t^2;\quad y(0)=2;\quad y'(0)=-1$$
$$s^2Y(s)-sy(0)-y'(0)-sY(s)+y(0)+9Y(s)=\frac{10}{s^3}$$
$$Y(s)(s^2-s+9)-2s+1+2=\frac{10}{s^3}$$
$$Y(s)=\left( \frac{10}{s^3}+2s+3 \right)\cdot \frac{1}{s^2-s+9}$$
$$Y(s)=\frac{2s^4+3s^3+10}{s^5-s^4+9s^3}$$
$$=\frac{2s}{s^2-s+9}+\frac{3}{s^2-s+9}+\frac{10}{s^5-s^4+9s^3}$$
$$=\frac{2s+3}{\left( s-\frac{1}{2} \right)^2+8.75}+\frac{10}{s^5-s^4+9s^3}$$
$$=\frac{2\left( s-\frac{1}{2} \right)}{\left( s-\frac{1}{2} \right)^2+8.75}+\frac{4}{\left( s-\frac{1}{2} \right)^2+8.75}+\frac{10}{s^5-s^4+9s^3}$$
$$y(t)=2e^{t/2}\cos{\sqrt{ 8.75 }t}+\frac{4}{\sqrt{ 8.75 }}e^{t/2}\sin{\sqrt{ 8.75 }t}+L^{-1}\left\{ \frac{10}{s^5-s^4+9s^3} \right\}$$

................... incomplete

3-2
$$y''(t)+4y'(t)=\cos(t)+4t+12;\quad y(0)=0;\quad y'(0)=7$$
$$s^2Y-sy(0)-y'(0)+4sY-4y(0)=\frac{s}{s^2+1}+\frac{4}{s^2}+\frac{12}{s}$$
$$Y(s^2+4s)-7=\frac{s}{s^2+1}+\frac{4}{s^2}+\frac{12}{s}$$
$$Y=\frac{1}{s^2+4s}\left( \frac{s}{s^2+1}+\frac{4}{s^2}+\frac{12}{s} \right)$$
.... incomplete



