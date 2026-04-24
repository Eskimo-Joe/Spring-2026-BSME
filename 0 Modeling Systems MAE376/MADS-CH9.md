
took a quiz

final will have 2 lagrangian questions
and will have one q from 8.5

state equation of vibe response
$$\dot{x}=Ax+Bu$$
after 2nd order ODEs and cannot be solved like before with large matrices
solution in general form
$$x(t)=e^{at}x_{0}+\int _{0}^te^{a(t-\tau)}bu(\tau) \, d\tau $$
where $a=A$, $b=B$, and $u(\tau)$ is u from above
"scalar form" 
$$e^{at}=\sum_{k=0}^{\infty} \frac{1}{k!}(at)^k $$
replace a with A

for EoM:
$$\dot{x}=\begin{bmatrix}
1 & 0 \\
-1 & -2 
\end{bmatrix}x+ \begin{bmatrix}
1 \\
3 
\end{bmatrix}e^{-t}\quad x_{0}=\begin{pmatrix}
1 \\
0
\end{pmatrix}$$
solve for response

use laplace transform on Ax+Bu
$$sX(s)-x_{0}=AX(s)+BU(s)$$
...
$$L^{-1}\{(sI-A)^{-1}\}=e^{At}$$
$$x(t)=e^{At}x_{0}+\int _{0}^te^{A(t-\tau)}BU(\tau) \, d\tau $$
$$x(t)=\begin{bmatrix}
\frac{1}{2}(3e^{t}-e^{-t}) \\

\end{bmatrix}$$

$$e^{At}=L^{-1}\{(sI-A)^{-1}\}$$
$$sI-A=\begin{bmatrix}
s & 0 \\
0 & s
\end{bmatrix}-\begin{bmatrix}
1 & 0 \\
-1 & -2
\end{bmatrix}=\begin{bmatrix}
s-1 & 0 \\
1 & s+2
\end{bmatrix}$$
$$\det(sI-A)=(s-1)(s+2)$$

$$(sI-A)^{-1}=\begin{bmatrix}
\frac{1}{s-1} & 0 \\
-\frac{1}{(s-1)(s+2)} & \frac{1}{s+2}
\end{bmatrix}$$
$$L^{-1}\{(sI-A)^{-1}\}=\begin{bmatrix}
e^{t} & 0 \\
\frac{1}{3}e^{t}-e^{-t} & 
\end{bmatrix}$$





