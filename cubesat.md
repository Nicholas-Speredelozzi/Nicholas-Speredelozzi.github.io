---
layout: default
title: CubeSat Senior Design
---

## CubeSat Senior Design

**Role:** Lead Environmental Engineer & Requirements Developer  
**Institution:** Embry-Riddle Aeronautical University  
**Mission Concept:** Space Situational Awareness in GEO  

---

## Project Overview

My capstone project is focused on the conceptual design of a 3U CubeSat intended to conduct space situational awareness (SSA) operations in Geosynchronous Earth Orbit. Our group is comprised of 8 students, each with a unique role in the design and integration of the spacecraft.  

The primary objective of the mission is to perform optical SSA on all objects in the geostationary belt, to include both active satellites & debris. To accomplish this task, the spacecraft will take multi-image, inertial stare collects of GEO objects and identify resident space objects (RSOs) captured in each image.  

Ultimately, the CubeSat will obtain estimated orbital trajectories of each RSO and create an SSA catalog of the GEO belt. Additionally, the mission lifetime & total cost cap for the project are set at 2 years & $200,000, split between build cost, labor hours, and testing facility usage.  

To track our progress, the project follows a formal systems engineering lifecycle, with four milestone reviews spread from August 2025 to April 2026. So far, we have completed the Systems Requirements Review, Preliminary Design Review, and Critical Design Review, with Operational Readiness Review on the horizon to be completed in the coming months.  

<div style="
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -40vw;
  margin-right: -40vw;
  width: 80vw;
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 30px;
  margin-bottom: 30px;
">
  
  <div style="text-align: center;">
    <img src="assets/wbs.png" style="width=40%;">
    <p><em>Above is the work breakdown structure for our mission. As true Daytona Beach residents, we named our CubeSat B.U.C.E.E.S (Breakthrough Utilization of CubeSats for Environmental Examination of Space).</em></p>
  </div>

  <div style="text-align: center;">
    <img src="assets/conops.png" style="width=40%;">
    <p><em>Here is a high-level concept of operations flowchart displaying the primary mission modes from deployment to decommissioning.</em></p>
  </div>

</div>

---

## My Responsibilities

I've contributed to design decisions & mission planning across the full scope of the project. However, my official roles within the team are Lead Environmental Engineer & Requirements Developer. The sections below include my primary responsibilities & examples of my contributions across a variety of major deliverables.

### Systems Engineering
- **Development & maintenance of system-level requirements across the full work breakdown structure**
<div style="text-align: center;">
    <img src="assets/requirements.jpg" style="width=40%;">
    <p><em>Above is a sample set of requirements I derived to define the CubeSat's payload & performance characteristics.</em></p>
</div>
- **Establishing verification methods linking system requirements to quantifiable verification & validation metrics**
- **Drafting end-to-end test plans adhering to NASA compliance documents, supporting the development of a launch-ready spacecraft**

### Environmental Analysis & Thermal Design
- **Conducted trade studies for thermal control & radiation protection subsystems, alongside contributions to various satellite bus trade studies**
<div style="
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -40vw;
  margin-right: -40vw;
  width: 80vw;
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 30px;
  margin-bottom: 30px;
">
  
  <div style="flex: 1; text-align: center;">
    <img src="assets/temperature_table.jpg" style="width: 100%; max-width: 400px; height: auto">
    <p><em>Operational and survivable temperature ranges for primary CubeSat components. (*) Components that limit the critical temperature range (lower limit -> battery, upper limit -> camera).</em></p>
  </div>

  <div style="flex: 2.5; text-align: center;">
    <img src="assets/STK_sim.jpg" style="width: 100%; max-width: 1500px; height: auto">
    <p><em>STK mission environment simulation displaying CubeSat temperature & optical coverage of GEO based on the camera's field of view.</em></p>
  </div>

</div>

Based on the temperature ranges in the table above, I defined a critical temperature range to keep the CubeSat within at all times throughout the mission life. To ensure functionality in all environments, this range was defined between -10 and +40 degrees Celsius.

The provided snapshot is from an STK environmental analysis I conducted to determine the temperature extremes our CubeSat would be exposed to over the 2-year mission life. Then I employed STK's SEET-Thermal (Space Environmental Effects Tool) model to define the spacecraft's radiative surface area, emmisivity, absorptivity, and internal heat dissipation. Applying this model to our CubeSat's orbit throughout the simulation period allowed me to generate reports that displayed hourly temperature readings, as well as the maximum, minimum, and averages for the full mission:
- Maximum Temperature (Peak Power Usage & Solar Flux): +35 degrees Celsius
- Minimum Temperature (Min Power Usage & Longest Eclipse): -50 degrees Celsius
- Average Temperature (Mean Power Usage & Solar Flux): +29 degrees Celsius

The max and average temperatures from the simulation fall well within the critical range, however, it is worth noting the the minimum temperature is well below the -10 degree operational limit. A few things to consider for this cold case are the length of eclipse (~65 minutes), and the absence of internal heat dissipation. The simulation doesn't account for the rate of heat transfer, it assumes that the eclipse immediately drops the spacecraft to equilibrium temperature (-50). Further calculations implied that dropping from average to minimum temperature would take over double the time of our longest eclipse, it's more reasonable to assume a 30-40 degree temperature drop. 

However, this analysis still results in the CubeSat enduring a temperature swing that brings sensitive components close to the lower limit of the critical range. My solution to minimize associated risks was to introduce a charging phase prior to eclipse that would allow the battery to reach max storage (40 W/Hr) before losing line-of-sight with the sun. This would give us the option to power internal electronics and active thermal control components to keep the spacecraft comfortably within the critical temperature range.

Using the STK data & analysis above, I derived thermal control requirements & conducted trade studies to determine optimal components for the CubeSat's thermal control subsystem:

**Passive:**
- A276 Polyurethane Coating (White)
- Multi-Layer Insulation (MLI)
- Heat Pipes

**Active:**
- Thermostat-Controlled Electric Patch Heaters

Due to strict size, weight, power, and cost constraints (SWaP-C), passive control strategies were prioritized to minimize frequency of ground commands & points of failure.

- **Analyzing hostile mission environments, potential failure modes, and mitigation strategies to ensure reliable operation throughout the mission lifecycle**

One of the most important aspects of mission planning is accounting for the wide range of failure modes the spacecraft is susceptible to across each mission environment. To consider the overarching impact of each failure mode, we assigned likelihood & severity values that multiply together to determine the mission criticality score as seen in the table below.
<div style="
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -40vw;
  margin-right: -40vw;
  width: 80vw;
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 30px;
  margin-bottom: 30px;
">
  
  <div style="text-align: center;">
    <img src="assets/risk_matrix.jpg" style="width=40%;">
    <p><em>Risk matrix</em></p>
  </div>

  <div style="text-align: center;">
    <img src="assets/failure_modes.jpg" style="width=40%;">
    <p><em>Failure modes</em></p>
  </div>

</div>

The risk matrix on the left serves as a legend to organize each failure mode into three levels of risk (Low: 0-6, Medium: 7-12, High: 13-25). The table on the right provides a sample set of failure modes we considered for the operational stage early in the design process. Each failure mode includes S (Severity)/L (Likelihood)/C (Criticality) values, how the failure would affect the CubeSat, and methods to detect or prevent the event.

An important simplification we made for our considered failure modes was to exclude launch environments & any corresponding failure modes. This assumption was made in coherence with our Mission Needs Document, which specifies that our analysis should start upon insertion into our operational orbit.

### Integration Considerations
- **Developing interfacing flowcharts to denote the transfer of commands, data, and power within the spacecraft**
- **3D modeling & assembly of subsystems in CATIA, adhering to CubeSat deployer integration requirements**
<div style="text-align: center;">
    <img src="assets/Cubesat.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Assembled CAD model</em></p>
</div>
Above is an assembled view of the CubeSat in CATIA that displays each major component of the bus/payload. The majority of 3D models were acquired directly from vendors, with exterior plates being designed in-house. The displayed image excludes MLI blankets, a solar panel, and exterior shielding plates in order to provide a clear view of the internal structure of components in the chassis.

- **Evaluating size, weight, power, and cost constraints (SWaP-C) as mission hardware & design considerations evolved**

---

## Key Takeaways

This project has given me a lot of insight into the importance of managing technical tradeoffs & understanding how design decisions affect system integration in lifecycle mission environments. The reinforcement of working in multidisciplinary teams to cohesively design a spacecraft has sharpened my technical communication skills within the team as well as in presentation settings.

As I begin my career in the aerospace industry, I'm thankful to have had this design project challenge me & provide ample learning opportunities in an industry-level, systems engineering environment.
