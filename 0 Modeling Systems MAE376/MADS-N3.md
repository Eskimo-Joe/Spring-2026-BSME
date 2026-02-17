
midterm next week

transfer function 

$$H(s)=\frac{L\{\text{output}\}}{L\{\text{input}\}}$$

a linear and time invariant system converts a single input to a single output

a linear system has linear scaling and follows superposition principle

linear scaling: multiplying by a factor applies to input and output
superposition: two systems with single in and out can be added together

time invariant: they do not change with time
$$x(t)\to y(t)$$
is equivalent to 
$$x(t-t_{0})\to y(t-t_{0})$$

block diagrams
summing point is a circle where inputs add to an output
branch point is a parallel out of a function, two destinations of a signal

if output goes back into input, its a feedback signal
H and G would be functions
E is the error which indicates some change should be made

closed-loop transfer functions when its a complete loop from input to output

open loop transfer function:
$$\frac{B}{E}=GH$$
feedforward TF:
$$\frac{C}{E}=G$$
The goal is to solve for the closed loop transfer function using the two equations above by finding the relation between the output C and input R
$$C=GE=G(R-B)=G(R-CH)$$
$$C=GR-GCH$$
$$1=\frac{GR}{C}-GH$$
$$1+GH=\frac{GR}{C}$$
$$C=\frac{GR}{GH+1}$$
$$\frac{C}{R}=\frac{G}{GH+1}$$

circuit example with the input and output being voltages with a resistor in series and a capacitor in parallel

use general ODE to setup
assume initial conditions are zero

$$Ri+\frac{1}{C}\int i \, dt =e_{i}$$
$$\frac{1}{C}\int i \, dt=e_{o} $$


$$E_{i}\left( \frac{1}{R} \right)=I(s)$$
$$I(s)\left( \frac{1}{Cs} \right)=E_{o}$$
the 1/s is added to integrate the current function!

cascaded system is two functions in series
parallel system is two function in parallel that conjoin
feedback (closed-loop) system: we covered this earlier

cascades can be simplified by multiplying the two functions into one
parallel systems simplify by adding
feedback systems can be simplified how we solved already
$$\frac{G}{1+GH}$$


ex

masons rule
$$1+ \sum \text{product of the transfer functions around each loop}$$
^ solves for the denominator of transfer function
the numerator is the product of all Gs 

MATLAB has a series, parallel, and feedback function for solving for transfer functions

numerator is a list with descending powers of s
same with denominator

six step process
move summing to left
move branches to right
combine cascades and parallels
something else
repeat

block diagram table

![Block Diagram Reduction](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQKZwJAAsENRwFg9GcPp6H3HFsIzp2s-YZvSw&s|400)

...

mason's gain rule
...

$$\frac{Y}{C}=\frac{K_{C}G_{1}G_{3}}{1+H}$$
wrong



