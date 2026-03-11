---
layout: default
title: Control Systems Stability Analysis Project
---

**Role:** Project Lead  
**Institution:** Embry-Riddle Aeronautical University  
**Dates:** October 2025 - December 2025

---

## Project Overview

During my spacecraft controls course, I had the opportunity to lead a group of three students in an analytical research project focused on stability characteristics of second-order feedback control systems. The primary objective of the project was to use classical control theory to analyze control system design methods commonly used for spacecraft dynamics & stability applications.

We used a combination of MATLAB transfer function simulation, root locus methods, and classical control theory to model the effects of varying control system parameters. By adjusting the values of proportional gain, undamped natural frequency, and damping ratio, we observed the effect on performance metrics such as settling time, overshoot, and pole location.

The concepts covered throughout the stability analysis project were excluded from the course curriculum, which gave us a good opportunity to conduct external research & hone our technical communication skills. The culmination of our research & design efforts was documented in a technical report provided below:

### [Control Systems Stability Analysis Report (PDF)](assets/control_project.pdf)

---

## My Responsibilities

The project deliverables were split into two main tasks. In task 1, we were given an open-loop transfer function (OLTF) & required to solve for the positive gain value yielding the minimum damping ratio for the system. The resulting parameters were then used to calculate the minimum 2% settling time.

Task 2 focused on root locus behavior & system stability utilizing a graphical approach. We considered two open-loop transfer functions with the same closed-loop pole locations; however, one model also included an open-loop zero. The goal of task 2 was to evaluate the system's transient response characteristics & analyze the difference between the two transfer functions.

As the project lead, my most valuable contributions included conducting hand calculations to solve each deliverable in tasks 1 & 2. I then created a MATLAB program to visualize the root locus plots & verify the accuracy of my hand calculations.

### Task 1 (Closed-Loop Pole Analysis)

Provided below is a walkthrough of the methods I used to calculate the optimal gain for minimal damping & the corresponding 2% settling time for the given OLTF:
<div style="text-align: center;">
    <img src="assets/controls_eqns_1.png" style="width: 60%; max-width: 1000px; height: auto">
    <p><em>OLTF & characteristic equations</em></p>
</div>
Beginning with the OLTF (G(s)) defined by an open-loop zero & poles at s = -1, -3, -9 on the real axis, I considered the system's characteristic equation (C(s)) with the implementation of proportional gain K. Important notes to consider here are the open-loop pole locations & signs of terms in C(s). Both poles lie in the left-side of the s-plane & each term in the characteristic equation has the same sign; these system qualities indicate stability at first glance. 

To obtain expressions for undamped natural frequency & minimum damping ratio in terms of K, I compared the characteristic equation to the standard form of a second order system. Setting the equations equal to each other and matching coefficients for each term yields the following equations in terms of only gain.
<div style="text-align: center;">
    <img src="assets/controls_eqns_2.png" style="width: 60%; max-width: 1000px; height: auto">
    <p><em>Coefficient matching & gain calculation</em></p>
</div>
To solve for the optimal gain value associated with the minimum damping ratio, I defined a function f(K) & set it's derivative equal to zero in order to identify the extrema. Next I used the quadratic equation to solve for K. Of the two solutions, the negative value can be neglected because one of the task 1 requirements was to solve for positive gain that yielded the minimum damping ratio. After determining the optimal proportional gain, I used the value K = 3.333 in the previously derived expressions to obtain minimum damping ratio & undamped natural frequency as seen below.
<div style="text-align: center;">
    <img src="assets/controls_eqns_3.png" style="width: 60%; max-width: 1000px; height: auto">
    <p><em>Damping parameters & transient response metrics</em></p>
</div>
After determining the transfer function's design parameters, I used the values to calculate the overshoot percentage & 2% settling time for the response output. These metrics provide important insight regarding the system's stability & transient response time.

### Task 2 (Root Locus Behavior)

Part 2 of the project focused on root locus behavior of two OLTFs shown below. 


---

## Key Takeaways
