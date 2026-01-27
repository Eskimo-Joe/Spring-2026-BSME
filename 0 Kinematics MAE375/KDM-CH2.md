---
tags:
  - MAE375
---


intro
email prof thru canvas

Lab: 20%
Quiz: 30%
Midterm: 25%
Final: 25%
Lecture Quiz: 10% (extra credit)
HW: 0%

quizzes and exams are open notes, no electronics

2.1
---

DOF: minimum number of independent parameters needed to uniquely define position of a system in space at any instant of time

a rigid body planar motion has maximum 3DOFs
a rigid body in 3D space has a maximum 6DOFs

2.2 types of motion
---
- pure translation
	- generally rectilinear
	- all points in body have same displacement, velocity, and acceleration
- pure rotation
	- the point that does not move is called center of rotation
	- all points in body have same angular displacement, angular velocity, and angular acceleration
- complex motion
	- mix of pure translation and pure rotation

2.3 links, joints, and kinematic chains
---
![[Pasted image 20260121172252.png]]

![[Pasted image 20260121172353.png]]

![[Pasted image 20260121173551.png]]

![[Pasted image 20260121174432.png]]

- ground: fixed
- crank: full revolutions
- rocker: oscillatory motion
- coupler: complex motion


![[Pasted image 20260121174516.png]]

only covers closed mechanisms in this class

![[Pasted image 20260121175223.png]]

![[Pasted image 20260121175233.png]]

$$M=3L-2J-3G$$
since $G$ is usually 1, equation simplifies to
$$M=3(L-1)-2J$$
when considering half joints, use 
$$M=3(L-1)-2J_{1}-J_{2}$$
![[Pasted image 20260121182039.png]]
count from 2, as the ground link should be 1 even if undrawn
remember that if more than 2 links meet at a node, it is multiple joints 

![[Pasted image 20260121182944.png]]

![[Pasted image 20260121183549.png]]

![[Pasted image 20260121183612.png]]

![[Pasted image 20260121183715.png]]

![[Pasted image 20260121183845.png]]

![[Pasted image 20260121183912.png]]

![[Pasted image 20260121183940.png]]

![[Pasted image 20260121184033.png]]

links are named with numbers, start with 2 as ground is always 1
lengths are lowercase letters from joint to joint
joints are named capital letters
grounded joints are name 0X where X is a number of link it grounds
X-axis is defined by the two grounded joints, Y is orthogonal

CCW is + and CW is -

examples...

![[Pasted image 20260121185435.png]]

![[Pasted image 20260121185536.png]]

## 01-26

![[Pasted image 20260121185603.png]]

![[Pasted image 20260126171533.png]]

![[Pasted image 20260126171539.png]]

![[Pasted image 20260126171544.png]]

![[Pasted image 20260126171549.png]]![[Pasted image 20260126171604.png]]

![[Pasted image 20260126171619.png]]

can be broken down into two four-bar mechanisms


![[Pasted image 20260126171625.png]]

![[Pasted image 20260126171641.png]]

![[Pasted image 20260126172344.png]]
no relative motion between three left links

![[Pasted image 20260126172406.png]]
R - revolute joint, only rotation is allowed
P - (prismatic) one linear pivot

![[Pasted image 20260126172653.png]]

![[Pasted image 20260126173315.png]]

![[Pasted image 20260126173323.png]]








