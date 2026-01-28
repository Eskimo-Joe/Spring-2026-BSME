---
tags:
  - MAE376
---

class can be considered Control systems 1, since control systems is a dense class. 

start by modeling systems by writing transfer functions

will cover mechanical, electrical, and thermal systems

phys 152 is a newly added prerequisite

"easier than dynamics"
review of mathematics

she does cool research with soft robotics

only 1 midterm exam

late assignments penalized 20% per day

Lecture

what is a dynamics system?
a system that changes over time
examples:
- solar system
- the atmosphere
- the economy
- the human body
- ecology
- cancer growth
- spread of epidemics
- chemical reactions
- the electrical power grid
- the internet

mathematical modeling of mechanical and electrical systems
examples, spring damping system 
$$m \dot{\dot{x}}+c \dot{x}+kx=F$$


took quiz


## 01-27

before we model and analyze systems we first understand mathematical models

- to understand behavior of systems, math models are required
- math models are equations that describe the system
- typically uses differential equations
- a

**building mechanical blocks (translational)**
the mathematical model of a machine mounted on the ground can be interpreted as a spring-mass dampener system

for rotational, it uses a different equation:
$$J \frac{d^2\theta}{dt^2}\dots$$

electrical system building blocks are capacitance, resistance, and inductance

fluid systems can be hydraulic or pneumatic
physical system $\to$ model schematic (simplified) $\to$ equivalent electrical circuit 

thermal systems
physical system $\to$ model schematic (simplified) $\to$ equivalent electrical circuit

**intro to ODE**

- recall basic definitions
	- order
	- linearity
	- initial conditions
	- solution
- classifying
- a

diff eq: an equation where a function is related to its derivative(s)

ordinary ($\frac{dy}{dx}$) - when y is a function of only x
partial ($\frac{ \partial y }{ \partial x }$) - when y is a function of multiple variables including x

a linear ODE if the function and its derivates are only to the power of one

this class is mostly linear ODEs, as non-linear ODEs are usually solved numerically and/or computationally

IVP or BVP

first-order ODE is said to be linear

$$\frac{dy}{dx}+p(x)y=g(x)$$
$$\mu(x)=e^{\int p(x) \, dx }$$
$$\mu(x)\left[ \frac{dy}{dx}+p(x)y \right]=\mu(x)g(x)$$
$$\mu(x)p(x)=\mu'(x)$$
$$\mu(x) \frac{dy}{dx}+\mu'(x)y=\mu(x)g(x)$$
using chain rule, solve
$$\frac{d[\mu(x)y(x)]}{dx}=\mu(x)g(x)$$
$$y(x)=\frac{\int \mu(x)g(x) \, dx +C}{\mu(x)}$$

ex
$$y'-y=e^{2x}$$
$$p(x)=-1;\quad \mu(x)=C_{1}e^{-x}$$
$$y(x)=\frac{\int e^{-x}\cdot e^{2x} \, dx }{e^{-x}}=\frac{C_{1}e^{x}+C_{2}}{e^{-x}}$$
$$y(x)=e^{2x}+Ce^{x}$$

ex2
$$xy'+2y=x^2-x;\quad y(1)=\frac{1}{2}$$
$$y'+\frac{2}{x}y=x-1$$
$$p(x)=\frac{2}{x};\quad \mu(x)=e^{\int 2/x \, dx }=e^{2\ln x}=x^2$$
$$y(x)=\frac{\int x^2(x-1) \, dx }{x^2}=\frac{\frac{1}{4}x^4-\frac{1}{3}x^3+C}{x^2}=\frac{1}{4}x^2-\frac{1}{3}x+Cx^{-2}$$
$$y(1)=\frac{1}{2}$$
$$\frac{1}{4}-\frac{1}{3}+C=\frac{1}{2}\to C=\frac{1}{2}+\frac{1}{3}-\frac{1}{4}= \frac{7}{12}$$
$$y(x)=\frac{1}{4}x^2-\frac{1}{3}x+\frac{7}{12}x^{-2}$$

2nd order ODEs can be homogenous and non-homogenous
homogenous is when the equation is equal to zero

homo
- real roots, complex roots, repeated roots
non-homo
- undetermined coefficients method

can make a note cheat sheet for ODE solutions, but practice is advised

when independent variable is time, dot is used instead of '

usually solve homogenous version of nonhomo first





