

Ch 4 = Position analysis

assume the design is done 

Given four links of different lengths. how to connect them to achieve a position

how many configurations can you build
how many mechanisms can you build

Given: a, b, c, d, and theta 2
Unknowns: theta 3, theta 4

**graphical approach:**
remember origin is at O2 and X-axis goes through O4

Start drawing Link 2 from the origin
	Link 2 has length a, and the coupler joint is named A
	angle respect to X-axis
	Link 3 has length b and the joins with link 4 at joint B
	Link 4 has length c
	ground has length d

Draw a circle of radius b at A
Draw a circle at O4 since theta 4 is unknown with radius c

there will be two intersections of the circle, and they are both potential solutions for joint B
both solutions have corresponding answers for theta 3 and 4
theta is always measured from the x-axis

if there is no intersections, no solution
if one intersection, then one solution

**analytical approach**
uses vectors
trinary links require more vectors

cartesian or polar coordinates is okay

in MATLAB, atan2 and atand2 is better than atan and atand because it accepts arguments and hence has better signage

polar: $\vec{R}=re^{j\theta}$

for lab 4 you need to rotate the coordinate system since O4 is elevated

see photo Feb 2 5:34pm

use vector loop equation
A + B - C - D = 0
remember A B C are crank, coupler, and rocker
D is negative because its ground.

vectors point away from O2 and towards joint B

example
$$R_{2}=ae^{j\theta_{2}}=acos\theta+aj\sin \theta$$
$$R_{3}=be^{j\theta_{3}}=$$
$$R_{4}=ce^{j\theta_{4}}$$
$$R_{1}=de^{j\theta_{1}}=d$$
theta 1 is always set to 0 so R1 is d
$$[a\cos \theta_{2}+aj\sin \theta_{2}]+[b\cos \theta_{3}+bj \sin \theta_{3}]-[c\cos \theta_{4}+cj\sin \theta_{4}]-[d]=0$$
$$[a\cos \theta_{2}+b\cos \theta_{3}-c\cos \theta_{4}-d]+j[a\sin \theta_{2}+b\sin \theta_{3}-c\sin \theta_{4}]=0+0j$$
$$a\cos \theta_{2}+b\cos \theta_{3}-c \cos \theta_{4}-d=0$$
$$a\sin \theta_{2}+b\sin \theta_{3}-c\sin \theta_{4}=0$$
theta 2 is given. use a given equation for 3 or 4
the remaining theta can be solved by plugging back into the above equations

see pg 187 for solutions

$$\theta_{4}=2\tan^{-1}{[\frac{-B\pm \sqrt{ B^2-4AC }}{2A}]}$$
$B^2-4AC<0$ - no solution
$B^2-4AC=0$ - one solution
$B^2-4AC>0$ - two solution

for two solutions, using the + in +/- gives open config
using - gives crossed config where links 1 and 3 cross



## 2-04

new mechanisms
crank-slider
slider-crank

**crank-slider**
two traditional links, one sliding block, one ground
origin at O2
X-axis is parallel to the slider's ground surface
crank (L2) connects to O2
coupler (L3) connects crank to slider
L4 is from slider joint to X-axis, so always parallel to Y 
L2: a L3: b L4: c L1: d

theta 2 is measured from X-axis to L2
theta 3 is measured at joint B (usually joint A for crank-rocker)

position analysis
Given: a, b, c, theta2
unknowns: theta3, d

graphical solution
1. draw L2 with a and theta2
2. draw a circle at A with radius b
3. find points on circle with height c from X-axis
	1. two intersections: 
	2. one intersection: 
	3. no intersections: b is too short

Analytical solution
$$R_{2}-R_{3}-R_{4}-R_{1}=0$$
$$R_{2}=ae^{j\theta_{2}}$$
$$R_{3}=be^{j\theta_{3}}$$
$$R_{4}=cj$$
$$R_{1}=d$$
$$[a\cos\theta_{2}+a\sin \theta_{2}j]-[b\cos \theta_{3}+bj\sin \theta_{3}]-cj-d=0$$
$$a\cos \theta_{2}-b\cos \theta_{3}-d=0$$
$$a\sin \theta_{2}-b\sin \theta_{3}-c=0$$

can solve for theta3 in bottom equation
then plug into top and solve for d

$$\theta_{3}=\sin^{-1}{\frac{a\sin \theta_{2}-c}{b}}$$


**slider-crank**
differs with different unknowns because the slider is now the input
 given: a, b, c, d
 unknowns: theta2, theta3

graphical solution
1. Find joint B using d as x-coordinate and c as y-coordinate
2. draw a circle at O2 with radius a
3. draw a circle at B with radius b

intersections are a solution for joint A

analytical solution
same as before but for two unknowns
$$[a\cos\theta_{2}+a\sin \theta_{2}j]-[b\cos \theta_{3}+bj\sin \theta_{3}]-cj-d=0$$
$$a\cos \theta_{2}-b\cos \theta_{3}-d=0$$
$$a\sin \theta_{2}-b\sin \theta_{3}-c=0$$
see page 195 (5th edition)




