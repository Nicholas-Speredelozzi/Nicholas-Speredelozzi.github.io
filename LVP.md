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

---

## My Responsibilities

Our team consisted of 4 students, each with individual roles & responsibilities that contribute to the overarching launch vehicle design. In my role as systems integration engineer, I was responsible for vehicle configuration decisions, internal/structural feasibility, and integration logistics between structural components, engines/fuel tanks, as well as the launch mount.

### Vehicle Configuration

One of my primary roles throughout the project was to define the vehicle architecture & ensure compatible interfacing between the multiple stages. Below is an overview of our final launch vehicle with important components labeled.
<div style="text-align: center;">
    <img src="assets/rocket_diagram.jpg" style="width: 75%; max-width: 1000px; height: auto">
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
    <img src="assets/trajectory_spreadsheet.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Excel trajectory optimization spreadsheet</em></p>
</div>
<div style="text-align: center;">
    <img src="assets/trajectory_plots.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Trajectory plots denoting altitude & angle vs. time</em></p>
</div>
Inputs for the trajectory optimization spreadsheet utilized known values obtained from the stage optimizer, alongside unknown values such as thrust-to-weight ratios, frontal areas (drag coefficient), and pitch-over maneuver altitude. This ambiguity gave us another opportunity to adjust the unknowns & iterate the model until we obtained the desired performance.

The outputs provided by the trajectory spreadsheet gave us critical information for the following launch & orbital insertion parameters:

- Burnout altitude
- Burnout angle
- Final velocity (V_orbital)
- Thrust for each stage
- Burn time for each stage

---

## Key Takeaways

