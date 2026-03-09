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

Within the team, I hold the roles of Lead Environmental Engineer & Requirements Developer. Though I've contributed to design decisions & mission planning across the full scope of the project, some of my primary responsibilities have included:

### Systems Engineering
- **Development & maintenance of system-level requirements across the full work breakdown structure**
<div style="text-align: center;">
    <img src="assets/requirements.jpg" style="width=40%;">
    <p><em>Above is a sample set of high-level requirements I drafted to define characteristics of the CubeSat's payload.</em></p>
</div>
- **Establishing verification methods linking system requirements to quantifiable verification & validation metrics**
- **Drafting end-to-end test plans adhering to NASA compliance documents, supporting the development of a launch-ready spacecraft**

### Environmental Analysis & Thermal Design
- **Conducted trade studies for thermal control & radiation protection subsystems, alongside contributions to various satellite bus trade studies**
<div style="
  position: relative;
  left: 40%;
  right: 60%;
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
    <img src="assets/temperature_table.jpg" style="width: 40%; max-width: 300px; height: auto">
    <p><em>Operational and survivable temperature ranges for primary CubeSat components. (*) Components that limit the critical temperature range (lower limit -> battery, upper limit -> camera).</em></p>
  </div>

  <div style="text-align: center;">
    <img src="assets/STK_sim.jpg" style="width: 40%; max-width: 700px; height: auto">
    <p><em>STK mission environment simulation displaying temperature extremes & coverage of GEO based on optical field of view characteristics.</em></p>
  </div>

</div>

Based on the temperature ranges above, I defined a critical temperature range to keep the CubeSat within at all times throughout the mission life. To ensure functionality in all environments, this range was defined between -10 and +40 degrees Celsius.

Using data gathered from the environmental analyses, I derived thermal control requirements & conducted trade studies to determine optimal components for the CubeSat's thermal control subsystem:

**Passive:**
- A276 Polyurethane Coating (White)
- Multi-Layer Insulation
- Heat Pipes

**Active:**
- Electric Patch Heaters

Due to strict size, weight, power, and cost constraints (SWaP-C), passive control strategies were prioritized to minimize ground commands & points of failure.

- **Analyzing hostile mission environments, potential failure modes, and mitigation strategies to ensure reliable operation throughout the mission lifecycle**

One of the most important aspects of mission planning is accounting for the wide range of failure modes the spacecraft is susceptible to across each mission environment.

To consider the overarching impact of each failure mode, we assigned likelihood & severity values that multiply together to determine the mission criticality score as seen in the table below.
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
    <p><em>STK mission environment simulation displaying temperature extremes & coverage of GEO based on optical field of view characteristics.</em></p>
  </div>

</div>
### Integration Considerations
- **Developing interfacing flowcharts to denote the transfer of commands, data, and power within the spacecraft**
- **3D modeling & assembly of subsystems in CATIA, adhering to CubeSat deployer integration requirements**
- **Evaluating size, weight, power, and cost constraints (SWaP-C) as mission hardware & design considerations evolved**

---

### CAD Model 
<div style="text-align: center;">
    <img src="assets/Cubesat.png" style="width: 40%; max-width: 700px; height: auto">
    <p><em>Here is an assembled CAD model of the CubeSat with exterior panels hidden to showcase the component organization inside the chassis.</em></p>
</div>
---

## Key Takeaways

This project has given me a lot of insight into the importance of managing technical tradeoffs & understanding how design decisions affect system integration in lifecycle mission environments. The reinforcement of working in multidisciplinary teams to cohesively design a spacecraft has sharpened my technical communication skills within the team as well as in presentation settings.

As I begin my career in the aerospace industry, I'm thankful to have had this design project challenge me & provide ample learning opportunities in an industry-level, systems engineering environment.
