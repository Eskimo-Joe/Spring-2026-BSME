---
tags:
  - MAE375
due: 2026-03-25
submitted: T
src:
---
by Joseph Ramirez

## 1

### Part 1

![[Pasted image 20260325102710.png|400]]
The problem is to derive a three-position synthesis and includes the relative locations of the ground joints O2 and O4. 

![[Pasted image 20260325093811.png|400]]
The ground joints and three positions were drawn in SolidWorks. The first step is to find the locations of joint A and B by finding O2', O4',  O2'', and O4''. The relative position from O2 to P2 gives the location of O2' relative to P1.


![[Pasted image 20260325094030.png|400]]
The relative O4 position from P2 is equal to O4' from P1.

![[Pasted image 20260325094159.png|400]]
The relative position of O2 from P3 is equal to O2'' from P1.

![[Pasted image 20260325094311.png|400]]
The relative position of O4 from P3 is equal to O4'' from P1.

![[Pasted image 20260325094430.png|400]]
The construction lines are cleared to show a clear view of the relative ground joints. 

![[Pasted image 20260325094944.png|400]]
The location of joint B during position 1 is found at the intersection of the bisecting the lines connecting O4 to O4' and O4' to O4''. The location of joint A was found similarly at the intersection of the bisecting line O2 to O2' and O2' to O2''. 

![[Pasted image 20260325095233.png|400]]
The construction lines are deleted and the four links of the mechanism are solved in position 1. 

![[Pasted image 20260325100129.png|400]]
The ground and coupler links are drawn with width so a 3D-model can be created. The coupler is a binary link but it is drawn as a quadrilateral to include the P and Q joint which will pass through the three positions given in the problem statement. 

![[Pasted image 20260325100052.png|400]]
The crank and rocker links are drawn to complete the mechanism. The links were then separated into individual part files and the mechanism was reconstructed into an assembly file. 

![[Pasted image 20260325102049.png|400]]
Here is the reconstruction showing link lengths in position 1. 
$$L_{1}=5cm\quad L_{2}=5.6693cm\quad L_{3} = 3.2046cm\quad L_{4}=6.1079cm$$
$$s=3.2046cm\quad l=6.1079cm\quad p=5cm\quad q=5.6693cm$$
$$s+l<p+q\quad \&\quad s=L_{3}$$
Condition: Grashof
Grashof Class: I-3
Grashof Code: GRCR
AKA Double-Rocker

### Part 2

![[Pasted image 20260325101332.png|300]]
Position 1 of the mechanism. 

![[Pasted image 20260325101421.png|300]]
Position 2 of the mechanism. 

![[Pasted image 20260325101630.png|300]]
Position 3 of the mechanism. 

The first step to the dyad synthesis is to find the range of motion of the dyad's output, which will be L2. According to the positions, the range of $\theta_{2}$ is 
$$39.0499^\circ\leq\theta_{2}\leq 91.1779^\circ$$

![[Pasted image 20260325131829.png|400]]
Next, a new joint was created for the dyad to interact with L2. I chose to the distance 4cm arbitrarily to reduce interference between links. 

Before continuing, the timing angles of the dyad must be solved to synthesize the dyad properly. Given a timing ratio of 1:1.7692 we can solve for the timing angles like so:
$$T_{R}=\frac{\alpha}{\beta}=\frac{\alpha}{360-\alpha}=\frac{1}{1.7692}\to  1.7692\alpha=360-\alpha$$
$$\alpha=\frac{360}{2.7692}=130 ^\circ\quad \beta=230^\circ$$
$$\delta=|180^\circ-\alpha|=50^\circ$$

![[Pasted image 20260325132101.png|400]]
The timing angles are used to identify the position of O6, the ground joint of the dyad crank AKA L6. First, a triangle is drawn with vertexes at the L2 joint in its maximum position, its minimum position, and at O6 (which has not been defined). The interior angle of O6 is set equal to $\delta$. As shown above, the construction lines are blue, meaning the position of O6 is not fully defined yet. 

![[Pasted image 20260325132139.png|400]]
The position of O6 is fully defined by choosing the radius of the dyad crank L6. The length 1cm was chosen, meaning the circle defining its motion must be 2cm. The distance from the L2-L5 in position 3 to the arc from L2-L5 in position 1 + $\angle \delta$ must be set equal to the crank diameter to guarantee the limits of L2's motion corresponds to the extents of the crank. If this step is skipped, The O6 position or the crank length would be wrong, resulting in the desired L2 minimum and maximum angles would be wrong and position 1 and 3 would not be the extents of the mechanism. 

![[Pasted image 20260325131724.png|400]]
The crank is drawn as it will be in position 1 (extended condition). 

![[Pasted image 20260325132424.png|400]]
The ground link is extended to include O6 to ground the crank. 

![[Pasted image 20260325134430.png|400]]
The dyad coupler is drawn to join the dyad crank and L2. 

![[Pasted image 20260325134315.png|400]]
The mechanism remembered with the dyad addition in position 1. It is shown that position 1 corresponds to the dyads extended configuration, shown by the $180^\circ$ measurement. 

![[Pasted image 20260325142648.png|400]]
Position 3 of the mechanism is the maximum extent of the range as the dyad crank and dyad coupler overlap. 

![[Pasted image 20260325143328.png|400]]
New Link Lengths:
$$L_{2}=5.6693cm\quad L_{3}=3.2046cm\quad L_{4} = 6.1079cm\quad L_{5}=3.5630cm\quad L_{6}=1cm$$
See $L_{1}$ below:
![[Pasted image 20260325143851.png|300]]

To solve for the grashof condition of the dyad mechanism, the dyad links will be renamed like shown below:
![[Pasted image 20260325144249.png|400]]
$$L_{1}=2.2805cm\quad L_{2}=1cm\quad L_{3}=3.5630cm\quad L_{4}=4cm$$
$$s=L_{2}\quad l=L_{4}\quad p=L_{1}\quad q=L_{3}$$
$$s+l<p+q$$
The dyad is grashof. Code: GCRR 
AKA Crank-rocker

Crank: 1cm
Coupler: 3.563cm
Rocker: 4cm
Ground: 2.2805cm

`<div style="page-break-after: always;"></div>
## 2
![[Pasted image 20260325152802.png|400]]
a)
$$M=3(L-1)-2J=3(4)-2(5.5)=1$$
Mobility is 1. 

b)
$$C=\frac{n(n-1)}{2}=\frac{5(4)}{2}=10$$
There are 10 instantaneous centers. They are $I_{12}$, $I_{13}$, $I_{14}$ $I_{15}$, $I_{23}$, $I_{24}$, $I_{25}$, $I_{34}$, $I_{35}$, and $I_{45}$.
![[Pasted image 20260325172711.png|400]]
Where $O_{2}=(0,0)$
$$I_{12}=O_{2}\quad I_{23}=A\quad I_{34}=D\quad I_{45}=E\quad I_{25}=B$$
$$I_{13}=(0, 73.123)cm\quad I_{14}=(31.657, 0)cm\quad I_{15}=(14.694,19.592)cm$$
$$I_{24}=(\infty,10.16)cm\,\,\,\&\,\,\,(\infty,20.32)cm\quad I_{35}=(22.86,-10.16)cm$$


## 3 
$$\vec{V}_{A}=\omega_{2} \times r_{A}=2k\times(0i+20.32j)=-40.64i \frac{cm}{s}$$
$$| \vec{V}_{A}|=40.64 \frac{cm}{s}\quad \angle \vec{V}_{A}=180^{\circ} $$
$$\vec{V}_{B}=\omega_{2}\times r_{b}=2k\times(7.62i+10.16j)=-20.32i+15.24j \frac{cm}{s}$$
$$| \vec{V}_{B}|=25.4 \frac{cm}{s}\quad \angle \vec{V}_{B}=90+\tan^{-1}{\frac{20.32}{15.24}}=143.13^\circ$$
$$\vec{V}_{D}=\vec{V}_{A}+\omega_{3}\times r_{DA}=-40.64i+\omega_{3}k\times22.86i$$
$$\vec{V}_{D}=-40.64i + 22.86\omega_{3}j \frac{cm}{s}$$
$$\vec{V}_{D}=\vec{V}_{E}+\omega_{4}\times r_{DE}=\vec{V}_{E}+\omega_{4}k\times(0i+10.16j)$$
$$\vec{V}_{D}=\vec{V}_{E}-10.16\omega_{4}i$$
$$\vec{V}_{E}=\vec{V}_{B}+\omega_{5}\times r_{EB}=-20.32i+15.24j + \omega_{5}k\times(15.24i+0j)$$
$$\vec{V}_{E}=-20.32i+(15.24\omega_{5}+15.24)j\, \frac{cm}{s}$$
$$\vec{V}_{D}=\vec{V}_{D}$$
$$-40.64i+22.86\omega_{3}j=-20.32i+15.24(\omega_{5}+1)j -10.16\omega_{4}i$$
$$-40.64=-20.32-10.16\omega_{4}$$
$$\omega_{4}=\frac{-40.64+20.32}{-10.16}=2 \frac{rad}{s}(CCW)$$
$$\vec{V}_{C}=\vec{V}_{B}+\omega_{5}\times r_{CB}=-20.32i+15.24j+\omega_{5}k\times(7.073645i -4.992033j)$$
$$\vec{V}_{C}=-20.32i+15.24j+7.0736\omega_{5}j+4.992\omega_{5}i$$
$$15.24+7.0736\omega_{5}=0$$
$$\omega_{5}=-\frac{15.24}{7.0736}=-2.1545 \frac{rad}{s}(CW)$$
$$\vec{V}_{D}=\vec{V}_{D}$$
$$-40.64i+22.86\omega_{3}j=-20.32i+15.24(\omega_{5}+1)j -10.16\omega_{4}i$$
$$22.86\omega_{3}=15.24(\omega_{5}+1)$$
$$\omega_{3}=\frac{15.24(-2.1545+1)}{22.86}=-0.7697 \frac{rad}{s}(CW)$$
$$\vec{V}_{C}=-20.32i+15.24j+7.0736\omega_{5}j+4.992\omega_{5}i=-31.08i+0j \frac{cm}{s}$$
$$|\vec{V}_{C}|=31.08 \frac{cm}{s}\quad \angle \vec{V}_{C}=180^\circ$$
$$\vec{V}_{D}=-40.64i + 22.86\omega_{3}j \frac{cm}{s}=-40.64i-17.594j \frac{cm}{s}$$
$$|\vec{V}_{D}|=44.285 \frac{cm}{s}\quad \angle \vec{V}_{D}=180+\tan^{-1}{\frac{17.594}{40.64}}=203.41^\circ$$
$$\vec{V}_{E}=-20.32i+(15.24\omega_{5}+15.24)j\, \frac{cm}{s}=-20.32i-17.594j \frac{cm}{s}$$
$$|\vec{V}_{E}|=26.879 \frac{cm}{s}\quad \angle \vec{V}_{E}=180+\tan^{-1}{\frac{17.594}{20.32}}=220.89^\circ$$

Answer:

| $\|\omega_{3}\|=0.7697 \frac{rad}{s}$ | CW                                 |
| ------------------------------------- | ---------------------------------- |
| $\|\omega_{4}\|=2 \frac{rad}{s}$      | CCW                                |
| $\|\omega_{5}\|=2.1545 \frac{rad}{s}$ | CW                                 |
| $\|\vec{V}_{A}\|=40.64 \frac{cm}{s}$  | $\angle \vec{V}_{A}=180^\circ$     |
| $\|\vec{V}_{B}\|=25.4 \frac{cm}{s}$   | $\angle \vec{V}_{B}= 143.13^\circ$ |
| $\|\vec{V}_{E}\|=26.879 \frac{cm}{s}$ | $\angle \vec{V}_{E}=220.89 ^\circ$ |
| $\|\vec{V}_{D}\|=44.285 \frac{cm}{s}$ | $\angle \vec{V}_{D}=203.41 ^\circ$ |
| $\|\vec{V}_{C}\|=31.08 \frac{cm}{s}$  | $\angle \vec{V}_{C}=180 ^\circ$    |

## 4
![[Pasted image 20260325194446.png|500]]

$$\vec{A}_{A}=-\omega_{2}^2r_{AO_{2}}=-4(0i+20.32j)=-81.28j \frac{cm}{s^2}$$
$$\vec{A}_{B}=-\omega_{2}^2r_{BO_{2}}=-4(7.62i+10.16j)=-30.48i-40.64j \frac{cm}{s^2}$$
$$\vec{A}_{D}=\vec{A}_{A}+\alpha_{3}\times r_{DA}-\omega_{3}^2r_{DA}=-81.28j+\alpha_{3}k\times22.86i-.7697^2(22.86i)$$
$$\vec{A}_{D}=-13.541i-81.28j+22.86\alpha_{3}j$$
$$\vec{A}_{E}=\vec{A}_{B}+\alpha_{5}\times r_{EB}-\omega_{5}^2r_{EB}$$
$$\vec{A}_{E}=-30.48i-40.64j+\alpha_{5}k\times 15.24i-2.1545^2(15.24i)$$
$$\vec{A}_{E}=-101.222i+(15.24\alpha_{5}-40.64)j$$
$$\vec{A}_{D}=\vec{A}_{E}+\alpha_{4}\times r_{DE}-\omega_{4}^2r_{DE}$$
$$\vec{A}_{D}=-101.222i+(15.24\alpha_{5}-40.64)j+\alpha_{4}k\times 10.16j-2^2(10.16j)$$
$$\vec{A}_{D}=(-101.222-10.16\alpha_{4})i+(15.24\alpha_{5}-81.28)j$$
$$\vec{A}_{D_{X}}=\vec{A}_{D_{X}}$$
$$-13.541=-101.222-10.16\alpha_{4}\to \alpha_{4}=\frac{-13.541+101.222}{-10.16}=-8.63 \frac{rad}{s^2}$$
$$\vec{A}_{C}=\vec{A}_{B}+\alpha_{5}\times r_{CB}-\omega_{5}^2r_{CB}$$
$$\vec{A}_{C}=-30.48i-40.64j+\alpha_{5}k\times(7.074i-4.992j)-2.1545^2(7.074i-4.992j)$$
$$\vec{A}_{C}=(4.992\alpha_{5}-30.48-32.8349)i+(7.074\alpha_{5}-40.64+23.1724)j$$
$$\vec{A}_{C}=(4.992\alpha_{5}-63.315)i+(7.074\alpha_{5}-17.468)j$$
$$7.074\alpha_{5}-17.468=0\to \alpha_{5}=\frac{17.468}{7.074}=2.469 \frac{rad}{s^2}$$
$$\vec{A}_{D}=(-101.222-10.16\alpha_{4})i+(15.24\alpha_{5}-81.28)j=-13.541i-43.646j \frac{cm}{s^2}$$
$$-81.28+22.86\alpha_{3}=-43.646\to \alpha_{3}=\frac{-43.646+81.28}{22.86}=1.646 \frac{rad}{s^2}$$
$$\vec{A}_{E}=-101.222i+(15.24\alpha_{5}-40.64)j=-101.222i-3.006j \frac{cm}{s^2}$$
$$\vec{A}_{C}=(4.992\alpha_{5}-63.315)i+0j=-50.988 \frac{cm}{s^2}$$
Answer:

| $\|\alpha_{3}\|=1.646 \frac{rad}{s^2}$   | CCW                               |
| ---------------------------------------- | --------------------------------- |
| $\|\alpha_{4}\|= 8.63\frac{rad}{s^2}$    | CW                                |
| $\|\alpha_{5}\|=2.469 \frac{rad}{s^2}$   | CCW                               |
| $\|\vec{A}_{A}\|=81.28 \frac{cm}{s^2}$   | $\angle\vec{A}_{A}=270 ^\circ$    |
| $\|\vec{A}_{B}\|=50.8 \frac{cm}{s^2}$    | $\angle\vec{A}_{B}=233.13^\circ$  |
| $\|\vec{A}_{E}\|=101.267 \frac{cm}{s^2}$ | $\angle\vec{A}_{E}=181.70 ^\circ$ |
| $\|\vec{A}_{D}\|=45.698 \frac{cm}{s^2}$  | $\angle\vec{A}_{D}= 252.76^\circ$ |
| $\|\vec{A}_{C}\|=50.988 \frac{cm}{s^2}$  | $\angle\vec{A}_{C}= 180^\circ$    |



