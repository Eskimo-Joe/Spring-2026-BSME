---
tags:
  - MAE375
---

graphical linkage synthesis

types of problems:
1. path generation
	1. focus on the path the output point follows
2. function generation
	1. only focus on correlation between input and output motion
3. motion generation
	1. focus on movement of a line between two or more states

motion defects
1. Toggle position
	1. limit on the input motion
	2. link 3 and 4 are collinear meaning the crank (link 2) cannot turn anymore
2. Stationary position
	1. limit on the output motion
	2. link 2 and 3 are collinear, meaning the output is at its furthest point

transmission angle ($\mu$) - the acute angle between link 3 and 4

**Function Generation**
1. none-quick return

![[Pasted image 20260126174855.png]]
equal time - it takes the same time to move from b1 to b2 as b2 to b1
assuming constant angular momentum from the crank
using $\omega=\frac{\Delta \theta}{\Delta t}$, to get an equal time, an equal angle is required for input and output. Since crank has 360 deg input, allocation 180 degrees to the input and 180 to the output

![[Pasted image 20260126175501.png]]
put O2 on the line from B1 and B2

2. Quick return
(no slide) 
differs from none-quick return bc it does not use equal time
Time Ratio: $T_{R}= \frac{\alpha}{\beta}=\frac{\alpha}{360-\alpha}$
because $\alpha+\beta=360$
$\alpha$ and $\beta$ are the two sections of the crank's circle of motion

$\gamma=|180-\alpha|=|180-\beta|$
draw a line from O2 to B1
draw a line from O2 to B2
$\gamma$ is the angle between the two lines

the length of link 2 $L_{2}=\frac{B_{1}B_{2}}{2}$
length of link 3 $L_{3}=A_{1}B_{1}=A_{2}B_{2}$
where A is where the respective line intersects with the crank motion

two points can lie on infinite circles
the center of the circle can exist on a bisecting line between the two points

three points can generate one circle by doing two bisecting lines between two pairs of points

**Motion Generation**
![[Pasted image 20260126182615.png]]
two choices:
- assume the line CD is on the rocker
- assume the line CD is on the coupler
remember rocker moves oscillatory and coupler moves complexly

so if first assumption is used, assume the motion of CD is about O4

![[Pasted image 20260126183007.png]]

![[Pasted image 20260126183202.png]]



![[Pasted image 20260126183717.png]]
add two linkages to rocker-rocker to drive it with a motor

![[Pasted image 20260126184001.png]]

---








