---
layout: default
title: Launch Vehicle Design Project
---

**Role:** Systems Integration Engineer  
**Institution:** Embry-Riddle Aeronautical University  
**Dates:** January 2023 - February 2023

---

## Project Overview

The launch vehicle project focused on the integration & conceptual design process for a multi-stage, hybrid-fueled medium-lift launch vehicle. This project took place during my freshman year & was structured as a precursor to the more detailed, in-depth senior design projects. Although it didn't reach the same technical depth as my capstone project, I still found a lot of value in its reinforcement of systems-level thinking & emphasis on iterative workflows to optimize spacecraft design.

The primary objective of this project was to utilize systems engineering principles in the conceptual design process of a multi-stage launch vehicle capable of delivering a 4,750 lb reconnaissance satellite into Low Earth Orbit (LEO). The design process began by selecting an orbital altitude, calculating the required change in velocity (ΔV), and developing a vehicle configuration capable of achieving that performance while meeting structural & propulsion constraints.

Throughout the mission, we used iteration-based tools in MATLAB & Excel to optimize mass distribution between stages, efficient use of propellant to achieve maximum ΔV, and launch trajectory characteristics to ensure safe payload delivery.
<div style="text-align: center;">
    <img src="assets/LVP_conops.jpg" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Launch vehicle project workflow</em></p>
</div>
Displayed above is a flowchart that provides the general procedure we followed throughout the launch vehicle design project. Arrows that loop back to a higher block represent iterations that could have been necessary to optimize performance or address potential issues.

Adhering to a set schedule with milestone updates was another important priority throughout the design process. Below is a Gantt chart that outlines the various work phases & deliverables we supplied over the course of the project.
<div style="text-align: center;">
    <img src="assets/LVP_schedule.jpg" style="width: 100%; max-width: 2000px; height: auto">
    <p><em>Project schedule Gantt chart</em></p>
</div>

---

## My Responsibilities

Our team consisted of 4 students, each with individual roles & responsibilities that contribute to the overarching launch vehicle design. In my role as systems integration engineer, I was responsible for vehicle configuration decisions, internal/structural feasibility, and integration logistics between structural components, engines/fuel tanks, as well as the launch mount.

### Vehicle Configuration

One of my primary roles throughout the project was to define the vehicle architecture & ensure compatible interfacing between the multiple stages. Below is an overview of our final launch vehicle with important components labeled.
<div style="text-align: center;">
    <img src="assets/rocket_diagram.jpg" style="width: 50%; max-width: 750px; height: auto">
    <p><em>Launch vehicle schematic</em></p>
</div>
As seen in the diagram, our final design utilized solid rocket motors for the first stage, with a liquid propulsion system powering the second stage. Each fairing, bulkhead, and propellant tank underwent structural feasibility checks, adhering to industry standard factors of safety (~1.1 - 1.5).

### Stage Optimization

To obtain the finalized architecture shown in the previous figure, we began by using a MATLAB program developed by previous students that optimized the weight distributions between the selected number of stages. The program provided optimized values for structural mass, propellant mass, and total achievable ΔV for each stage based on the following inputs:

- Number of stages (2 or 3)
- Desired specific impulse of each stage
- Total vehicle mass (propellant, structural, and payload)
- Payload mass
- Structural coefficients of each stage

For inputs based on specific engine performance characteristics or non-finalized values, we researched launch vehicles similar to the architecture we had in mind & tweaked the inputs until the achievable ΔV matched our calculated value. The MATLAB stage optimizer was the first of many iteration-focused design tools used to support the design of our launch vehicle.

### Trajectory Spreadsheet & Thrust/Weight Ratios

The next step in the design process was to determine the thrust-to-weight ratios required at each stage to produce the ΔV computed by the stage optimizer. This task was carried out through the iterative use of an Excel spreadsheet shown below. 
<div style="text-align: center;">
    <img src="assets/trajectory_spreadsheet.png" style="width: 100%; max-width: 2000px; height: auto">
    <p><em>Excel trajectory optimization spreadsheet</em></p>
</div>
<div style="text-align: center;">
    <img src="assets/trajectory_plots.png" style="width: 100%; max-width: 2000px; height: auto">
    <p><em>Trajectory plots denoting altitude & angle vs. time</em></p>
</div>
Inputs for the trajectory optimization spreadsheet utilized known values obtained from the stage optimizer, alongside unknown values such as thrust-to-weight ratios, frontal areas (drag coefficient), and pitch-over maneuver altitude. This ambiguity gave us another opportunity to adjust the unknowns & iterate the model until we obtained the desired performance.

The outputs provided by the trajectory spreadsheet gave us critical information for the following launch & orbital insertion parameters:

- Burnout altitude
- Burnout angle
- Final velocity (V_orbital)
- Thrust for each stage
- Burn time for each stage

This information allowed us to finalize what SRMs (Solid Rocket Motors) & liquid fueled boosters we would employ for the launch vehicle. We compared our thrust requirements to flight-proven engines & ultimately decided to use scaled M-24 engines for our first stage with the RL-10A Centaur booster as our liquid-fueled second stage.

### Structural Components

Some of my most important contributions to the team took place in this phase of the launch vehicle project. After determining the required thrust & finalizing the engine selections, it was time to design the structural components.

My responsibilities to ensure structural feasibility included calculating required thickness, choosing material, and determining structural mass of the following components:

- Inter-stage bulkheads
- Motor fairings
- Inter-stage adapter fairings
- Nosecone fairing (payload)
- Propellant tanks

All calculations shown below were conducted with an FOS (factor of safety) of 1.5.

**Fairings**

To determine the minimum wall thickness for each fairing, I considered the compressive loading induced by thrust as the critical stress. At this point in my education, I had not taken any mechanics or structures courses, so my professor provided the necessary equations shown below.
<div style="text-align: center;">
    <img src="assets/wall_thickness_eqn.png" style="width: 60%; max-width: 1000px; height: auto">
    <p><em>Minimum fairing wall thickness equation</em></p>
</div>
I used this equation to determine the thickness of all the launch vehicle fairings. However, a material needed to be chosen to obtain a value for yield strength. I ran the calculation for a few different options before landing on aluminum (6061-T6) as the optimal material for the fairings. The balance between yield stress & low density provided the necessary protection without adding excessive mass to the launch vehicle.

The height-to-diameter ratios for each fairing were dependent upon the SRM diameters, liquid propellant tank sizes, and nozzle sizes. However, in order for the launch vehicle to remain aerodynamically feasible, the following H/D requirements had to be met:

- First stage configuration (entire vehicle height):      7 < H/D < 15
- Second stage configuration (stage 2 + payload stage):   5 < H/D < 13

To ensure I met the requirements, I researched the pros & cons of different nosecone fairing shapes, ultimately choosing an elliptical section to house the satellite. Lastly, to calculate the total mass of the fairings, I used the height, thickness, and material density values.

**Bulkheads**

To calculate the bulkhead thickness at each stage, the primary failure mode to consider was the bending stress developed from the weight of the vehicle supported by each respective bulkhead. The equation shown below for applied stress was used for each bulkhead, adjusting the T/W ratio to accurately reflect each stage.
<div style="text-align: center;">
    <img src="assets/bulkhead_stress_eqn.png" style="width: 60%; max-width: 1000px; height: auto">
    <p><em>Bulkhead applied stress equation</em></p>
</div>
Extracting the thickness from this equation is an iterative process. The equation cannot be algebraically manipulated to solve for bulkhead thickness directly, so I tested different values until the applied stress matched the expected value.

Accounting for the intense loading carried by the bulkheads, I selected stainless steel as the material. As the launch vehicle ascends, it requires less thrust to continue accelerating & loses weight as propellant is burned, so the thickness of each bulkhead decreases with each stage. Similar to the fairings, the bulkhead masses were calculated using the volume determined by thickness/radius & the material density.

**Prepellant Tanks**

Obtaining the mass of the propellant tanks is dependent upon the volume & wall thickness of each tank. At this point in the project, I only knew the total mass of propellant for the second stage from the MATLAB Stage optimizer. In order to calculate the weight of the fuel & oxidizer as well as the necessary tank volumes, I utilized the equations shown below:

The mixture ratio is dependent upon the chosen booster characteristics. The Centaur uses a ratio of 5:1 liquid oxygen to liquid hydrogen. Next, I used the tank volumes to determine the total height of the pill-shaped tanks.

To determine the wall thickness, I needed to calculate the maximum pressure the tanks would endure during launch. This pressure maximum corresponds to the most likely failure mode for pressure vessels, hoop stress. Max pressure is measured as the summation of gas pressure, hydrostatic pressure, and inertial loading caused by worst-case acceleration.

The worst-case acceleration occurs at stage 1 burnout, when the thrust-to-weight ratio is greatest. Using these assumptions, I determined the minimum tank thickness from the following equations:


---

## Key Takeaways

