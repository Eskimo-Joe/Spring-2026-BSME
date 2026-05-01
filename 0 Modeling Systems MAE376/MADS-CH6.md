

review of electrical circuits

17 minutes late

missed first example

example 6.4 pg 278

for node method:
$$i_{L}-i_{R}-i_{C}=0$$
$$\frac{1}{L}\int (v_{a}-v_{o}) \, dt- \frac{v_{o}}{R}-C \frac{d}{dt}(v_{o})=0 $$
solve by taking derivative with respect to time
$$\frac{1}{L}(v_{a}-v_{o})-\frac{\dot{v}_{o}}{R}-C \ddot{v}_{o}=0$$
take laplace
$$\frac{1}{L}(V_{a}-V_{o})-\frac{1}{R}(sV_{o})-C(s^2V_{o})=0$$
$$\frac{1}{L}V_{a}=\left( Cs^2+\frac{s}{R}+\frac{1}{L} \right)V_{o}$$
$$\frac{V_{o}}{V_{a}}=\frac{1}{L\left( Cs^2+\frac{s}{R}+\frac{1}{L} \right)}$$

for loop method:
$$-v_{a}+v_{L}+v_{R}=0\quad -v_{R}+v_{C}=0$$

example 6.7: same problem but state-space equation

$$i_{L}=x_{1}\quad v_{c}=x_{2}$$
$$\dot{x}_{1}=\frac{d}{dt}i_{L}=\frac{1}{L}v_{L}=\frac{1}{L}(v_{a}-x_{2})$$
$$\dot{x}_{2}=\frac{d}{dt}v_{c}=\frac{1}{C}i_{C}=\frac{1}{C}(i_{L}-i_{R})=\frac{1}{C}(x_{1}-i_{R})=\frac{1}{C}\left( x_{1}-\frac{x_{2}}{R} \right)$$
$$\dot{x}_{1}=\frac{1}{L}(u-x_{2})\quad \dot{x}_{2}=\frac{1}{C}\left( x_{1}-\frac{x_{2}}{R} \right)$$
$$\begin{bmatrix}
\dot{x}_{1} \\
\dot{x}_{2} 
\end{bmatrix}=\begin{bmatrix}
0 & -\frac{1}{L} \\
\frac{1}{C} & -\frac{1}{CR}
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}+\begin{bmatrix}
\frac{1}{L} \\
0 
\end{bmatrix}u$$
$$y=Cx+Du$$
$$v_{o}=\begin{bmatrix}
0 & 1
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}+\begin{bmatrix}
0
\end{bmatrix}v_{a}$$
$$\frac{L^{-1}\{Y\}}{L^{-1}\{u\}}=C(sI-A)^{-1}B+D$$




