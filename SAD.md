---
layout: default
title: Satellite Rotational Dynamics Programming Project
---

**Role**: Modeling & Simulation Engineer  
**Institution:** Embry-Riddle Aeronautical University  
**Course:** Spacecraft Attitude Dynamics (AE 426)  
**Date:** March 2025 - April 2025  
**Tools:** MATLAB, Microsoft Suite

---

## Project Overview

This project focused on the modeling & simulation of rigid satellite rotational dynamics using MATLAB. The main objective was to analyze how the angular velocity of a spacecraft evolves over time in the absense of external torques, using classical rigid body dynamics.

The satellite was modeled as a system of six fixed components, each with a defined mass & position within a body-fixed reference frame. Treating these components as point masses allowed the satellite's mass properties to be calculated directly from their spatial distribution.

Analysis of the system's dynamics was split into three major steps:

- Determining the center of mass & inertia properties of the satellite
- Evaluating the principal axes & moments of inertia
- Simulating the spacecraft's roational motion using Euler's equations

The final simulation computed the satellite's angular velocity over a 100-second time interval, while verifying the conservation of rotational kinetic energy, which should remain constant in the absence of external torques.

This type of analysis forms the foundation of spacecraft attitude dynamics, where understnading rotational behavior is essential for designing stable satellites & effective attitude control systems.

---

## System Modeling & Mass Properties

The first deliverables for the project were the mass distribution & inertial properties of the satellite.

Each of the six components was defined by:

- Mass
- Position vector with respect to the body-fixed frame's origin

The values were derived using two unique constants defined by the amount of letters in my full name & the sum of digits that make up my birthdate. The resulting mass & position of each component is displayed in the table below.

Treating the components as point masses simplified the calculations required to determine the satellite's key physical properties.

### Center of Mass

The center of mass (COM) was calculated as the mass-weighted average of the positions of the six components. 

In practice, the COM is an essential parameter that influences design implementation of thrusters, sensors, and control actuators that ensure accurate spacecraft attitude determination & control.

### Moment of Inertia Matrix

---

## Key Takeaways

