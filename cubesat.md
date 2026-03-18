---
layout: default
title: CubeSat Senior Design
---

**Role:** Environmental Engineer & Requirements Developer  
**Institution:** Embry-Riddle Aeronautical University  
**Course:** AE 427/445 - Spacecraft Preliminary/Detail Design  
**Date:** August 2025 - April 2026  
**Tools:** STK, MATLAB, Ansys Thermal Desktop, CATIA, Microsoft Suite, Systems Engineering Documentation

---

## Engineering Snapshot

**Project Type:** Senior Capstone CubeSat Lifecycle Design Project  

**Key Concepts:**  
Spacecraft systems engineering | Requirements derivation | Failure modes analysis | Environmental mission analysis | End-to-end test planning

**My Contributions:**

- **Developed & maintained SMART requirements** across a full work breakdown structure
- Conducted **system-level trade studies** defining thermal control & satellite bus subsystems under strict **SWaP-C budgets**
- Assessed potential **failure modes & mitigation strategies** in a variety of hostile mission environments
- Evaluated **thermal operating conditions** based on component temperature limits & the orbital environment
- Analyzed **interface control documentation** denoting the flow of power, data, and commands throughout the CubeSat architecture
- Simulated communication ability & **coverage analysis based on selected ground stations**
- Drafted **end-to-end test plans** to support development of a launch-qualified spacecraft

**Key Result:**  
The project reinforces systems engineering practices across the full design lifecycle of a CubeSat. With minimal instructor intervention, our team is expected to adhere to a strict schedule & produce high-quality deliverables.

---

## Project Overview

My capstone project focuses on the conceptual design of a 3U CubeSat intended to perform space situational awareness (SSA) operations in Geosynchronous Earth Orbit (GEO). Our team consists of 8 students, each responsible for a specific engineering discipline within the spacecraft design & integration.  

The primary mission objective is to perform optical SSA on all objects in the geostationary belt, including both operational satellites & orbital debris. To accomplish this, the spacecraft will conduct multi-image, inertial stare observations of GEO objects & identify resident space objects (RSOs) present in each image.  

Using these observations, the CubeSat will estimate the orbital trajectories of detected RSOs & contribute to the development of an SSA catalog of the GEO belt. The mission is designed for a two-year operational lifetime with a total project cost cap of $200,000, including hardware procurement, labor hours, and testing facility usage.

Project development follows a formal systems engineering lifecycle, with four major milestone reviews scheduled between August 2025 and April 2026. To date, the team has successfully completed the Systems Requirements Review (SRR), Preliminary Design Review (PDR), and Critical Design Review (CDR). The final Operational Readiness Review (ORR) is scheduled for completion in the coming months.

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
    <p><em>BUCEES Work Breakdown Structure (WBS)</em></p>
  </div>
  <div style="text-align: center;">
    <img src="assets/conops.png" style="width=40%;">
    <p><em>Concept of Operations (CONOPS) flowchart displaying the primary mission phases from deployment to decommissioning</em></p>
  </div>

</div>
Displayed above are the work breakdown structure & concept of operations for the mission. As true Daytona Beach residents, our team named the spacecraft B.U.C.E.E.S (Breakthrough Utilization of CubeSats for Environmental Examination of Space).

These documents define the overall organizational structure of the project & serve as the framework for developing & tracing system-level requirements across the spacecraft architecture.

---

## My Responsibilities

While I have contributed to design decisions & mission planning across the full scope of the project, my primary roles within the team are Lead Environmental Engineer & Requirements Developer. 

The sections below highlight my key responsibilities & contributions to several major project deliverables.

### Systems Engineering
- **Development & maintenance of system-level requirements across the full work breakdown structure**
<div style="text-align: center;">
    <img src="assets/requirements.jpg" style="width=40%;">
    <p><em>Sample set of payload requirements</em></p>
</div>
The figure above shows a representative set of high-level requirements defining the CubeSat’s payload capabilities & performance targets. These requirements were derived from the project’s Mission Needs Document (MND), which establishes the mission objectives, budget constraints, and external compliance standards the spacecraft must satisfy.

- **Establishing verification methods linking system requirements to SMART verification & validation metrics**

As requirements were developed across each node of the WBS, corresponding verification methods & artifacts were defined to track requirement status. Many requirements originated from the MND & established testing standards such as NASA’s General Environmental Verification Standard (GEVS).

However, defining appropriate verification strategies required coordination throughout the spacecraft architecture. I worked closely with team members responsible for each subsystem to identify the tests, analyses, and inspections necessary to demonstrate compliance.

- **Drafting end-to-end verification test plans aligned with NASA environmental compliance documents to support launch readiness**

### Environmental Analysis & Thermal Design

As the team’s Environmental Engineer, one of my primary responsibilities is analyzing the various hostile environments the spacecraft will encounter & developing mitigation strategies to ensure reliable operation throughout the mission lifecycle.

The following sections summarize several analyses related to space environment risks, spacecraft thermal control, and subsystem trade study development.

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
    <p><em>Operational & survivable temperature ranges for primary CubeSat components (*) Components that limit the critical temperature range (lower limit -> battery, upper limit -> camera)</em></p>
  </div>

  <div style="flex: 2.5; text-align: center;">
    <img src="assets/STK_sim.jpg" style="width: 100%; max-width: 1500px; height: auto">
    <p><em>STK mission environment simulation displaying CubeSat temperature & optical coverage of GEO based on the camera's field of view</em></p>
  </div>

</div>

Based on the component temperature limits shown in the table above, I defined a critical operating temperature range of -10°C to +40°C. The spacecraft's equilibrium must be kept within this range at all times to ensure functionality.

The image on the right shows an STK environmental simulation used to estimate the temperature extremes experienced by the CubeSat over its two-year mission. Using STK’s SEET-Thermal (Space Environmental Effects Tool) model, I defined key spacecraft thermal properties, including radiative surface area, emissivity, absorptivity, and internal heat dissipation.

Applying these parameters to the spacecraft’s GEO orbit allowed STK to generate hourly measurements & temperature extreme statistics for the mission duration:

- Maximum Temperature: +35°C (peak solar flux & power usage)  
- Minimum Temperature: -50°C (extended eclipse with minimal internal heat)  
- Average Temperature: +29°C

While the maximum & average temperatures fall well within the defined critical range, the simulated minimum temperature of -50°C is significantly below the spacecraft’s operational limit. 

Two important factors influence this result. First, the minimum temperature occurs during the CubeSat’s longest eclipse duration, which is approximately 65 minutes. Second, the STK thermal model assumes the spacecraft instantaneously reaches equilibrium temperature, which neglects thermal inertia & physical rate of heat transfer. 

Additional calculations indicate that cooling from the average temperature to the simulated minimum would require more than twice the duration of the longest eclipse. A more realistic estimate suggests a temperature drop of approximately 30–40°C during eclipse.

Even with this more conservative estimate, the spacecraft could approach the lower bound of the operational temperature range. To mitigate this risk, I proposed introducing a pre-eclipse charging phase, allowing the spacecraft battery to reach its full 40 Wh capacity before entering eclipse. This stored energy could then power internal electronics & active thermal control components, maintaining temperatures within the acceptable range.

Using the STK analysis above, I developed thermal control requirements & conducted trade studies to identify appropriate components for the spacecraft’s thermal control subsystem.

**Passive Thermal Control**
- A276 Polyurethane White Coating
- Multi-Layer Insulation (MLI)
- Heat Pipes

**Active Thermal Control**
- Thermostat-Controlled Electric Patch Heaters

Due to strict size, weight, power, and cost (SWaP-C) constraints, passive thermal control methods were prioritized in order to minimize system complexity, required ground commands, and potential points of failure.

- **Analyzing hostile mission environments, potential failure modes, and mitigation strategies**

One of the most important aspects of mission planning is identifying potential spacecraft failure modes & evaluating their impact on mission success.

Each failure scenario was assigned severity (S) & likelihood (L) scores, which were multiplied to generate an overall criticality score (C).
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
The risk matrix on the left provides a classification system for organizing failure modes into Low (0–6), Medium (7–12), and High (13–25) risk categories. The table on the right shows a sample set of failure modes considered during the operational phase of the mission.

For this analysis, launch environments & associated failure modes were excluded. This assumption follows guidance from the Mission Needs Document, which defines the beginning of the analysis period at the insertion into the operational orbit.

### Integration Considerations
- **Developing interfacing flowcharts to define the transfer of commands, data, and power throughout the spacecraft**
<div style="text-align: center;">
    <img src="assets/distribution_diagram.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Distribution/interfacing diagram</em></p>
</div>
Successful integration between spacecraft subsystems is essential to ensure reliable operation throughout the mission lifecycle. The diagram above illustrates the high-level flow of power, data, and command pathways within the CubeSat architecture. 

Some subsystems that continuously exchange information (such as the Electrical Power Subsystem (EPS) & Flight Computer) are simplified to unidirectional arrows for clarity. A ground station node is also included to represent the uplink & downlink communication interfaces between the spacecraft & mission operations center (MOC).

Solar panels generate electrical power from solar radiation, which is routed to the battery for storage. The EPS monitors battery charge levels & distributes regulated power to the spacecraft subsystems as required.

Data pathways are shown in red. Several subsystems collect external data, including RSO imagery from the optical payload & attitude reference data from sensors around the spacecraft. All data is routed to the On-Board Computer (OBC), which processes the information & transmits relevant telemetry through the communication subsystem to ground stations.

Tracking, Telemetry, and Command (TT&C) signals are represented by the yellow pathways. These communication links enable the transfer of spacecraft health telemetry, command updates, and ranging information between the CubeSat and ground operators.


To maintain reliable communication throughout the mission, the spacecraft will utilize four ground stations within NASA’s Near Space Network (NSN). These stations are geographically distributed to provide continuous communication access during the mission.
<div style="text-align: center;">
    <img src="assets/ground_stations.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Ground station locations</em></p>
</div>
Ground station selection was based on several key factors, including communication frequency compatibility, geographic distribution, and operational cost. All selected stations support S-band communication, which is used for both uplink and downlink operations.

The benefits of this geographic distribution are illustrated in the STK coverage analysis below.
<div style="text-align: center;">
    <img src="assets/2D_STK_ground_stations.png" style="width: 85%; max-width: 2000px; height: auto">
    <p><em>2D representation of ground station locations/accessability</em></p>
</div>
The solid yellow access line represents communication visibility between the CubeSat & each ground station. Continuous access lines indicate that the spacecraft maintains constant communication availability, allowing commands & telemetry to be transmitted at any point during the orbit.


The figure below summarizes the communication access time for each ground station throughout the first year of operation.
<div style="text-align: center;">
    <img src="assets/STK_coverage_analysis.png" style="width: 100%; max-width: 2000px; height: auto">
    <p><em>Access times for each selected ground station</em></p>
</div>

- **3D modeling & subsystem integration in CATIA while adhering to CubeSat deployer requirements**
<div style="text-align: center;">
    <img src="assets/Cubesat.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Assembled CAD model</em></p>
</div>
The figure above shows the integrated CubeSat assembly developed in CATIA, including the primary spacecraft bus and payload components. Most subsystem models were obtained directly from component vendors, while several structural elements, such as exterior plates, were designed in-house.

For visualization purposes, the image excludes MLI blankets, one solar panel, and external shielding plates, allowing the internal subsystem layout to remain visible.

The CAD model was also used to determine the spacecraft’s center of mass & moment of inertia properties, which were required for estimating the attitude control torque & power requirements needed to perform spacecraft slews during mission operations.

- **Evaluating size, weight, power, and cost constraints (SWaP-C) as design decisions evolved**

The mission’s total cost cap of $200,000 was defined in the Mission Needs Document (MND). While this value constrained the overall project budget, the allocation of resources across subsystems was determined by the team during the design process.

The spacecraft’s size & mass constraints were driven by the selected deployer. After evaluating multiple options, we selected Cal Poly SLO’s Poly-Picosatellite Orbital Deployer (P-POD) for its flexibility & GEO flight heritage.

The deployer’s CubeSat Design Specification (CDS) establishes limits of 3.405U total volume & 6 kg maximum mass for the spacecraft. The pie charts below illustrate the volume and mass allocation across the major spacecraft subsystems.
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
    <img src="assets/volume_budget.png" style="width=40%;">
    <p><em>Volume budget</em></p>
  </div>

  <div style="text-align: center;">
    <img src="assets/mass_budget.png" style="width=40%;">
    <p><em>Mass budget</em></p>
  </div>

</div>
The spacecraft power budget is driven primarily by the battery capacity selected for the Electrical Power Subsystem. For this reason, EPS trade studies were conducted early in the design process to ensure sufficient available power.

The selected battery provides 40 Wh of energy storage, which defines the total available onboard power. The chart below illustrates how power is distributed among the spacecraft’s major subsystems.
<div style="text-align: center;">
    <img src="assets/power_budget.png" style="width: 75%; max-width: 1750px; height: auto">
    <p><em>Power budget</em></p>
</div>

---

## Key Takeaways
This project has provided valuable experience in **systems engineering, spacecraft design trade studies, and multidisciplinary collaboration**. Working within a team environment reinforced the importance of balancing technical constraints while maintaining system-level integration across the spacecraft architecture.

This project has given me a lot of insight into the importance of managing technical tradeoffs & understanding how design decisions affect system integration in lifecycle mission environments. Working within a multidisciplinary team environment reinforced the importance of balancing technical constraints while maintaining system-level integration across the spacecraft architecture.

The project has also strengthened my ability to communicate technical concepts clearly through design documentation, modeling/simulation analysis, and formal design reviews.

As I begin my career in the aerospace industry, I am grateful for the opportunity to work on a project that directly aligns with the systems engineering processes used in real spacecraft development programs.
