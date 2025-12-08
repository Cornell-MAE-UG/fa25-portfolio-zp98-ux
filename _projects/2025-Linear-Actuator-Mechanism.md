---
layout: project
title: Linear Actuator Mechanism
description: ENGRD 2020 assignment
technologies: paper and pencil, calculator
image:

---


As part of a class assignment, I was asked to design a mechanism that lifts the maximum possible weight to the maximum possible height, keeping in mind certain parameters. This optimization problem applied what I've learned about frames and mechanisms.


We were given a design space 150 cm long by 50 cm tall, a rigid bar of any length, 3 pin supports (2 needed to be mounted to the ground), and a linear actuator chosen from a catalog.


This is how I solved the problem:

Step 1 (edited):

Set-up: I picked the RSX high force rod-style actuator, because it had the largest max force and stroke length of those available (up to 294 kN and a stroke length of up to 150 cm). I will place two of the pins mounted to the ground and attach the bar to one of them and the actuator to the other. The bar spans the hypotenuse of the design space (158.11 cm long). The actuator will be pinned to the ground at some relatively large distance x = close to 150 cm away so that its moment arm is increased and it can lift a larger weight, although some height will be sacrificed.

*

My design degrees of freedom: two degrees of freedom, the linear actuator extension, placement of the linear actuator along the x-axis.

Assumptions: Bar is rigid, weight attached is a point mass

Calculations: To be able to apply the greatest moment, the linear actuator should start perpendicular to the bar. As the linear actuator extends, it will apply a smaller moment on the bar, and so will the weight, until the linear actuator fully extends. See image: 

*

Conclusions: I chose to use somewhere between Case 1 and Case 2 in my design to strike a balance between maximum height reached and maximum weight lifted. 

*

Step 2:

Maximum deflection in my beam: Assume my beam is rigid, only transverse components to the beam are important (following the prompt's instructions), and beam is simply supported by pin A and the linear actuator. Because of these assumptions, I can say this beam is an overhanging beam with a point load at the end. This loading is described by the equation

δ_max = (sqrt(3) * W * (DC) * (AD)^2)/(27 * E * I)

DC is 15.8 cm and AD is 142.3 cm. In addition to the assumptions above, I will also assume that my beam is made out of steel with a circular cross section, diameter 40 mm. Now I know E = 200 GPa and I = (pi*d^4)/64. Plugging this into the equation above, I get δ_max = 22.8 cm, which is quite large.

Designing a cross-section such that δ_max is < 2% of 158.1 cm aka 3.162 cm, while minimizing cross-section area: I'll choose a Wide-Flange Shape. Assuming I keept the same material and setting δ_max to 0.03162 m, I get that I must be at least 9*10^5 mm^4. (about 7 times larger than before). In the end, a W shape is a bit overkill for meeting this requirement, so I chose the  S 75 x 8.5 shape which has an Ix of 1.04*10^6 mm^4.

*
