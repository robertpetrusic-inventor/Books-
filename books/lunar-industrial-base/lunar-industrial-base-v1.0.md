**LUNAR INDUSTRIAL BASE AND AUTONOMOUS ROBOTIC INFRASTRUCTURE**

Technical concept for relay spacecraft, surface robots, base construction, resource extraction and Moonforge operations

![][image1]

**Concept architecture: Robert Petrušić**

Technical edition 1.0 \- 4 August 2026

| SCOPE This edition is an engineering reference only. It excludes comic pages, plot, characters and fictional events. Project names retained from earlier concept work are used solely as subsystem labels. All numerical values are preliminary design assumptions unless explicitly sourced. |
| :---- |

# **Document status and interpretation**

This report consolidates a lunar infrastructure concept into a physically grounded system architecture. It describes autonomous relay spacecraft, surface robots, construction equipment, a shielded base, a modular mine and the Moonforge processing complex. It does not claim that the full system exists, that any resource deposit is economically recoverable, or that the illustrated machines have completed lunar qualification.

The architecture deliberately separates three categories. Category A consists of established physical principles and technologies already demonstrated in terrestrial, orbital or lunar-relevant environments. Category B consists of plausible engineering integrations that still require prototypes, environmental tests and mission analysis. Category C consists of long-term options that should remain outside the baseline until mass, energy, reliability and legal analyses close.

| Category | Meaning | Examples in this report |
| ----- | ----- | ----- |
| A \- established basis | Known physics and existing component families; lunar qualification may still be required. | Radio relays, electric propulsion, rover drives, thermal-vacuum hardware, solar arrays, batteries, regolith handling. |
| B \- development concept | A credible system integration with unresolved sizing, reliability or operations. | Moon Hound hopper, AAGS wheels, modular Genesis mine, surface beacon mesh, Moonforge pilot line. |
| C \- long-term option | Potentially useful but not part of the initial mission baseline. | Large-scale satellite salvage for lunar feedstock, high-autonomy self-expansion, broad local manufacture of precision components. |

| CRITICAL TERMINOLOGY Because the Moon has no useful atmosphere, a propeller-driven aircraft cannot fly there. In this report, “satellite drone” means a small autonomous free-flying spacecraft. Surface drones are wheeled, tracked, legged, tethered or ballistic-hopping robots. |
| :---- |

# **Executive summary**

The proposed lunar system is not a single base or a single mining robot. It is a staged network of orbital service spacecraft, communication and navigation relays, surface beacons, prospectors, construction rovers, cargo carriers, processing equipment and eventually shielded human facilities. The architecture is organized around one principle: every imported kilogram should either perform multiple functions or enable the use of local material.

The reference location is the lunar south-polar region, not because every polar site is automatically suitable, but because polar terrain can combine access to water-bearing permanently shadowed regions with nearby areas receiving extended illumination. The base itself should remain on stable, well-mapped terrain outside the coldest shadowed resource zones. Mining robots travel into the hazardous zones; the habitat does not.

The orbital layer begins with direct-to-Earth communication and a small number of Kage Relay service nodes. These autonomous spacecraft provide store-and-forward data, emergency communication, timing and navigation ranging. Silent Lanterns extend the network on the surface. They are fixed or relocatable beacons placed on ridges, at mine entrances and along traverses. Mizuchi tugs move cargo between staging orbits and support stationkeeping. Orbital Reclaim units are a later service and salvage branch, not an initial supply assumption.

The surface layer combines several specialized machines. Moon Hound scouts cross short obstacles by storing energy slowly and releasing it in controlled hops. ASETAMO rovers use adaptive AAGS contact elements to adjust traction and probe the substrate. Genesis mining units divide work among tethered scouts, tracked excavators, heavy tool carriers, cargo Mules and cable-deployment robots. LITHOS is the digital-twin and supervisory layer that turns maps, hazards and work orders into constrained command packets rather than unsafe continuous remote control.

Base construction starts with robotic site preparation. Landing and ascent operations are isolated from the habitat because engine plumes can erode and accelerate regolith. Robots grade routes, stabilize surfaces, deploy power and communications, install imported pressure modules, construct berms and cover critical structures with local regolith. Moonforge initially performs simple work: screening, sintering, casting test coupons, producing shielding material and recovering oxygen or metal-rich residue in small experimental batches. It expands only after measured yields and maintenance demands are known.

![][image2]

*Figure 1\. System-of-systems architecture. The arrows show functional relationships, not final distances or orbital parameters.*

## **Principal recommendations**

* Use a south-polar reference architecture, but select the exact site only after terrain, illumination, thermal, communications, plume and resource surveys are combined.  
* Define the first “satellite drones” as interoperable communication, timing and navigation nodes compatible with the LunaNet framework rather than a proprietary closed constellation.  
* Choose one Moon Hound baseline for early prototyping: a bottom-heavy spherical body with one retractable leaf-spring launcher and minimal exposed mechanisms.  
* Keep the mine and hot processing plant physically separated from the habitat; move samples and certified products across controlled contamination boundaries.  
* Build an energy architecture that can black-start, isolate faults and preserve a protected emergency bus. Treat industrial loads as interruptible.  
* Do not size a production mine from assumed ice concentration. First demonstrate prospecting, excavation, thermal extraction and measurement of net recovered water per unit energy.  
* Qualify components by cycle count and degraded operation, not only by nominal performance. Dust, low temperature, vacuum lubrication and connector wear should dominate the test program.  
* Delay crew arrival until the robotic site has verified power, communication, shelter preparation, spares, rescue access and safe shutdown.

# **Contents**

1\. Mission definition and design rules

2\. Lunar operating environment

3\. Integrated system architecture

4\. Kage Relay and Silent Lantern communications network

5\. Mizuchi orbital logistics and Orbital Reclaim

6\. Surface robotic fleet

7\. Site selection and survey campaign

8\. Base architecture and construction sequence

9\. Genesis mine and LITHOS control layer

10\. Moonforge resource processing and manufacturing

11\. Power, energy storage and thermal control

12\. Human systems, safety and emergency operations

13\. Maintenance, spares and reliability

14\. Development, testing and deployment roadmap

15\. Indicative budgets and operating scenarios

16\. Risk register and mitigation plan

17\. Governance, legal and environmental constraints

18\. Conclusions

Appendices: terminology, interfaces, requirements, test matrix and references

# **1\. Mission definition and design rules**

## **1.1 Mission**

The mission is to establish a robotic industrial foothold that can survey terrain, maintain communications, prepare protected infrastructure, extract small quantities of local resources, manufacture simple non-critical parts and support later human operations. The system must create useful capability before it reaches industrial scale. A pathfinder that only returns accurate resource, wear and power data is successful if it prevents an incorrectly sized mine.

## **1.2 System boundaries**

The baseline includes the lunar surface site, local orbital relays and tugs, Earth control interfaces and the logistics chain required to deliver replacement electronics, seals, lubricants, sensors and precision mechanisms. It does not assume a self-sufficient colony. Precision semiconductors, high-performance bearings, specialized polymers and many medical supplies remain Earth-supplied for a long period.

## **1.3 Design rules**

1. Multi-function without hidden coupling: one part may serve multiple roles only when failure in one role does not silently disable another critical role.  
2. Specialized robots over a single universal machine: common interfaces are standardized, while chassis and tools remain task-specific.  
3. Dust isolation before dust cleaning: keep sensitive components away from raw regolith, then use cleaning methods as a secondary defense.  
4. Fail-safe local autonomy: loss of communication causes a safe hold, retreat or shutdown rather than continued execution of stale commands.  
5. Measured resource accounting: every mining claim is stated as recovered product per kilogram processed and per kilowatt-hour, including rejected material and maintenance.  
6. Modular replacement: exposed actuators, cameras, power electronics and contact elements are replaceable by another robot using accessible fasteners and lifting points.  
7. No crew dependence during build-up: early infrastructure must be installable, testable and maintainable robotically.  
8. Interoperable communications and navigation: service interfaces should align with open lunar standards and allow multiple providers.  
9. Thermal design before packaging: radiators, shadowing, heaters and heat paths are established before enclosing electronics.  
10. Clear distinction between a concept sketch and a requirement: legacy illustration values are not automatically adopted.

## **1.4 Nomenclature**

| Name | Technical meaning in this report |
| ----- | ----- |
| Kage Relay | Autonomous lunar-orbit communication, timing and navigation service node. |
| Silent Lantern | Surface or near-surface relay, hazard beacon and optical/radio navigation landmark. |
| Mizuchi Tug | Autonomous cislunar cargo tug using efficient propulsion and standardized cargo interfaces. |
| Orbital Reclaim Unit | Spacecraft for inspection, stabilization, capture and authorized relocation of inactive objects. |
| Moon Hound | Small distributed lunar scout using short controlled hops or rugged low-gravity mobility. |
| ASETAMO / AAGS | Adaptive rover and active contact system that changes traction geometry and senses the substrate. |
| Genesis / LITHOS | Modular mining fleet and its constrained digital-twin supervisory environment. |
| Lunar Mule | Cargo carrier or standardized logistics frame for containers, tanks, cables and modules. |
| Moonforge | Surface processing plant for regolith, water, oxygen, metals, glass, ceramics and basic manufacturing. |
| Tsukikage base | Working name for the integrated surface outpost; not a fictional organization in this edition. |

# **2\. Lunar operating environment**

## **2.1 Vacuum and gravity**

The Moon has only an extremely tenuous exosphere, so there is no useful aerodynamic lift, convective cooling or ordinary sound transmission. Surface equipment rejects heat primarily through radiation and conduction into controlled structures. Lubricants, polymers, adhesives and insulation must be selected for vacuum compatibility and outgassing. The surface gravitational acceleration is about one-sixth of Earth’s. Lower weight reduces required support force, but mass and inertia remain unchanged; a heavy load is still difficult to accelerate, stop or stabilize. \[E1\]

## **2.2 Thermal environment and illumination**

Equatorial sunlit surfaces can reach roughly 127°C, while darkness can fall near \-173°C. Polar terrain is more complex: low Sun angles create long shadows, nearby illuminated ridges and permanently shadowed regions that can be substantially colder. The reference architecture therefore separates sunlit power generation from resource work in shadow. Cables, relay nodes or mobile energy carriers bridge the two environments. \[E1, E5\]

A lunar day-night cycle is approximately 29.5 Earth days, but polar illumination is governed by local horizon geometry rather than a simple fourteen-day daylight period. Mission planning must use high-resolution terrain and time-dependent lighting simulation. A “peak of eternal light” should never be assumed from a coarse map.

## **2.3 Radiation and micrometeoroids**

Without a dense atmosphere and global magnetic field, equipment and crew are exposed to galactic cosmic rays, solar energetic particles and secondary radiation produced when particles interact with the surface. Electronics require radiation-tolerant architecture, error detection, watchdogs and recoverable storage. Human habitats need a dedicated storm shelter and meters-scale equivalent shielding determined by radiation transport analysis rather than by a generic wall thickness. LRO’s CRaTER instrument and NASA standards provide inputs for such design work. \[E12, E13\]

## **2.4 Regolith and dust**

Lunar regolith is not ordinary soil. Fine particles are angular, abrasive and electrostatically adhesive because they have not been rounded by wind or water. Dust can damage seals, optical surfaces, radiators, suit joints and lungs. NASA’s Electrodynamic Dust Shield demonstrated regolith removal on the lunar surface in 2025, but a single cleaning technology does not eliminate the need for zoning, covers, replaceable seals and low-dust operations. \[E3, E4\]

![][image3]

*Figure 2\. Dust-control zoning. The safest dust is the dust that never crosses a pressure boundary.*

## **2.5 Terrain, lighting and navigation**

Low-angle polar illumination creates glare, long shadows and weak visual texture. Navigation therefore combines stereo cameras, lidar or time-of-flight ranging, inertial sensing, wheel or leg odometry, terrain-relative localization, orbital ranging and fixed surface landmarks. A path should carry a confidence score and an escape route, not only a shortest-distance solution.

## **2.6 Water ice and mineral resources**

Multiple missions have identified hydration and water ice associated with polar permanently shadowed regions. The distribution can be patchy and mixed with regolith; it is not equivalent to a continuous underground ice sheet. Water can support life support, radiation shielding and propellant production, but recoverability depends on concentration, depth, grain size, temperature, excavation method and thermal losses. \[E2, E6\]

Lunar regolith contains a large fraction of oxygen by mass, chemically bound in oxides and glass. ESA laboratory work has demonstrated oxygen extraction from simulants using molten-salt electrolysis, leaving metal-rich material. This is a promising processing route, but the plant requires high temperature, electrical energy, corrosion-resistant materials and long-duration maintenance. \[E7, E8\]

| Environmental driver | Design consequence |
| ----- | ----- |
| Vacuum | No propeller flight; radiative thermal control; vacuum-compatible materials and lubrication. |
| Low gravity | Longer ballistic hops; reduced normal force and traction; unchanged inertia. |
| Extreme temperature | Heaters, insulation, heat pipes, radiator view factors and survival modes. |
| Radiation | Shielding, error correction, redundant control and storm shelter. |
| Abrasive electrostatic dust | Isolation zones, sacrificial covers, electrodynamic cleaning and replaceable seals. |
| Long shadows and glare | Active ranging, fixed beacons, polar lighting simulation and conservative route margins. |
| Uncertain resource grade | Prospecting-first strategy and measured net yield before production sizing. |

# **3\. Integrated system architecture**

The architecture is layered so that each stage produces an independently useful capability. The first layer is communications and navigation. The second is surface reconnaissance and route proving. The third is power and logistics. The fourth is construction and resource demonstration. Human occupancy is a later load added to an already functioning robotic site.

## **3.1 Functional layers**

| Layer | Primary assets | Minimum useful result |
| ----- | ----- | ----- |
| Orbital services | Kage Relay, Mizuchi Tug, authorized reclaim units | Reliable contact, time transfer, navigation measurements and cargo staging. |
| Surface network | Silent Lanterns, base gateway, mine gateway | Local mesh, hazard markers, store-and-forward data and emergency broadcast. |
| Reconnaissance | Moon Hounds, ASETAMO, Voxel Scout | Terrain, void, thermal and resource maps with confidence estimates. |
| Construction | Lunar Mule, Badger, Mole, tethered tools | Stabilized routes, power/data trenches, berms, module placement and shielding. |
| Resource processing | Genesis mine, Moonforge | Measured water/oxygen/material yield and qualified construction feedstock. |
| Human support | Shielded habitat, airlocks, life support, rescue rover | Safe occupancy after robotic verification and pre-positioned spares. |

![][image4]

*Figure 3\. Specialized surface fleet. Standard interfaces allow replacement and cooperation without forcing every machine into the same chassis.*

## **3.2 Data architecture**

Every asset maintains local time, a health state, a map version, an authorized work envelope and a safe state. High-bandwidth imagery can be delayed; emergency state, position, power and fault codes receive priority. The digital twin stores not only geometry but also uncertainty, material provenance, component life and contamination history.

## **3.3 Safe degradation**

A failed relay should reduce data rate, not eliminate command. A failed wheel contact should reduce mobility, not immobilize the rover. A failed processing line should isolate itself and preserve feedstock. A failed industrial bus should not pull down the life-support bus. These requirements must be demonstrated by deliberate fault injection during terrestrial testing.

# **4\. Kage Relay and Silent Lantern communications network**

## **4.1 Definition of the satellite-drone layer**

Kage Relay nodes are small autonomous spacecraft in lunar orbit or cislunar staging locations. Their purpose is not to imitate an atmospheric drone but to provide a reconfigurable service network. Each node can perform stationkeeping, route data, distribute time, broadcast navigation signals, observe space weather and enter a safe orbit after faults.

NASA, ESA and JAXA are developing the LunaNet Interoperability Specification as a network-of-networks framework for lunar communications, position, navigation and timing. The current NASA page identifies Version 5, published in February 2025\. The concept should align with that framework rather than create incompatible proprietary signaling. \[E9\]

![][image5]

*Figure 4\. Reference communications and navigation architecture. Exact orbit count and geometry require coverage simulation.*

## **4.2 Kage Relay node functions**

* Multi-band communications appropriate to direct-to-Earth, crosslink and surface service.  
* Store-and-forward routing for periods when direct contact is blocked.  
* Precise clock distribution and two-way ranging to support surface localization.  
* Navigation message broadcast compatible with the selected lunar service standard.  
* Optical terminal option for high-rate trunk links, with radio retained for acquisition and emergency use.  
* Radiation-tolerant processing, autonomous safe mode and delayed-command execution.  
* Electric propulsion for efficient stationkeeping and controlled disposal or relocation.  
* Onboard conjunction assessment using Earth-provided catalogs and local observations.

## **4.3 Constellation growth**

The first deployment should avoid the cost and complexity of a complete navigation constellation. A staged sequence is preferable. Stage 1 uses direct-to-Earth base terminals and one or two surface ridge relays. Stage 2 adds a small number of orbital nodes to close coverage gaps. Stage 3 adds crosslinks and timing. Stage 4 adds navigation service and commercial or international interoperability. The number and orbit families are selected after coverage, eclipse, link-budget and disposal analysis.

| Stage | Capability | Primary limitation |
| ----- | ----- | ----- |
| 1 \- direct service | Base high-gain terminal, local mesh and ridge beacons. | Terrain blockage and limited far-side/shadow coverage. |
| 2 \- relay service | Store-and-forward through several orbital nodes. | Position still depends heavily on terrain-relative navigation. |
| 3 \- timed network | Crosslinks, synchronized clocks, ranging and emergency broadcast. | Geometry may be insufficient for continuous high-accuracy PNT. |
| 4 \- navigation service | Multiple providers and GNSS-like lunar signals. | Requires standards compliance, calibration and operational governance. |

## **4.4 Silent Lantern surface nodes**

A Silent Lantern is a fixed, relocatable or mobile surface node. It is intentionally simple compared with an orbital relay. A node may include a radio, optical fiducial, flashing coded light, passive retroreflector, local clock, environmental sensors and a small thermal battery. It can mark a safe corridor, a crater rim, a cable junction or the last reliable communication point before a shadowed mine.

Lanterns should be deployable by Moon Hound scouts or ASETAMO rovers. Each node uses a standardized anchoring plate and can operate as a low-data-rate emergency repeater when the main network is unavailable. In permanently shadowed regions, energy comes through cable, replaceable battery, radioisotope heater where legally and technically justified, or periodic robotic exchange. Solar panels alone are not an adequate baseline in permanent shadow.

## **4.5 Link and navigation integrity**

The network must distinguish communication availability from navigation integrity. A strong data link does not guarantee a good position solution. Navigation messages carry health and uncertainty. Surface vehicles compare orbital ranging with local beacons, inertial motion and terrain features. If solutions disagree beyond a threshold, the vehicle slows, stops or retreats.

## **4.6 Cybersecurity and command authority**

A lunar network faces long delays, intermittent links and multiple operators. Commands therefore carry time validity, work-zone limits and cryptographic authorization. A high-level work packet may authorize excavation inside a polygon and set force, power and depth limits, but the local controller remains responsible for collision avoidance and safe stop. Emergency stop paths are simpler and independently authenticated.

## **4.7 Failure modes**

| Failure | Effect | Mitigation |
| ----- | ----- | ----- |
| Relay loss | Coverage gap or reduced data rate. | Crosslinks, direct-to-Earth fallback, store-and-forward and surface mesh. |
| Clock drift | Navigation error. | Multiple clocks, two-way time transfer, integrity flags and local inertial checks. |
| Solar array degradation | Reduced service life. | Load shedding, propulsion reserve, cleanable surfaces and planned replacement. |
| Orbit error | Coverage loss or collision risk. | Autonomous navigation, ground catalog, safe-mode orbit and disposal plan. |
| Compromised command | Unsafe tasking. | Signed commands, expiring permissions, local safety kernel and independent shutdown. |

# **5\. Mizuchi orbital logistics and Orbital Reclaim**

## **5.1 Mizuchi Tug**

The Mizuchi Tug is a reusable autonomous cargo-transfer spacecraft. It does not land in the initial configuration. It accepts standardized cargo frames, tanks or propulsion modules at a staging orbit, performs slow efficient transfers, controls attitude during handover and returns for the next load. Electric propulsion is favored for non-urgent cargo; higher-thrust chemical or storable propulsion may be required for time-critical maneuvers and landing support.

| Subsystem | Baseline function | Design concern |
| ----- | ----- | ----- |
| Cargo interface | Four-point capture frame, power/data umbilical and positive mechanical latches. | Must tolerate misalignment and verify load path. |
| Propulsion | Efficient long-duration transfer and stationkeeping. | Thrust, trip time, plume contamination and power. |
| Guidance | Autonomous rendezvous, proximity operations and abort. | Sensor blinding, uncertain target motion and delayed supervision. |
| Power | Solar arrays, batteries and protected avionics bus. | Eclipse survival and array articulation. |
| Thermal | Radiators, heat pipes and survival heaters. | Variable orientation and hot propulsion components. |
| Serviceability | Replaceable propulsion and avionics modules where feasible. | Orbital robotic access and connector standardization. |

## **5.2 Orbital Reclaim Unit**

The Orbital Reclaim Unit inspects, stabilizes and captures an inactive spacecraft only when ownership, permission and liability are resolved. It first characterizes target rotation and structural condition, then attaches a clamp, net or purpose-built interface, damps motion and moves the object to a safer orbit or controlled processing location. The unit must never create more debris than it removes.

The Lunar Salvage Bridge is a long-term branch that attempts to reuse mass already launched from Earth. Panels, aluminum structures, motors and radiation-shielding mass could be more valuable than raw scrap. However, transferring non-cooperative objects, landing them, removing hazardous batteries and producing certified parts may consume more energy and mission time than launching new material. The concept remains a separate economic trade, not a dependency of the first base. \[D4\]

## **5.3 Salvage triage**

| Class | Treatment |
| ----- | ----- |
| Reusable assembly | Preserve intact: solar panel, motor, tank, radiator, structural beam or flight computer after testing. |
| Material feedstock | Remove contaminants, sort alloy, cut into manageable stock and reserve for non-critical parts. |
| Hazardous item | Isolate batteries, pressurized vessels, propellant residues, toxic materials and pyrotechnics. |
| Unsuitable target | Leave untouched if capture risk, legal ambiguity or energy cost exceeds benefit. |

## **5.4 Legal and operational limit**

Under the Outer Space Treaty, states retain responsibility for national space activities and liability for space objects; outer space is not subject to national appropriation. Resource use and deconfliction remain active governance topics. Any reclaim mission requires authorization from the registering state or owner, a liability plan, debris mitigation and transparent notification. \[E14, E15\]

# **6\. Surface robotic fleet**

## **6.1 Moon Hound role**

Moon Hound is a distributed scout, not the main cargo vehicle. It enters terrain that would force a wheeled rover into a long detour, maps short gaps, confirms landing surfaces, places Lantern beacons and continues as a stationary sensor if mobility is lost. The architecture intentionally tolerates loss of individual low-cost scouts without losing the mission.

## **6.2 Approved micro-hopper direction**

The preferred early direction is a small bottom-heavy spherical or rounded body with one retractable leaf-spring launcher. Solar energy or a small battery drives a low-power motor that slowly tensions the spring. A positive latch carries the stored load. Before release, a brief internal motor “kick” or eccentric mass rotates the body to aim. The spring extends, launches the robot and retracts behind the protective shell. This configuration minimizes exposed mechanisms and uses low gravity to obtain useful range from modest stored energy. \[D1\]

![][image6]

*Figure 5\. Existing Moon Seed Hopper design sketch. Embedded dimensions and component values are legacy placeholders, not adopted requirements.*

## **6.3 Spring-catapult tripod variant**

A three-legged spring-catapult variant provides better static aiming and landing control, but it exposes more joints and creates more dust-sensitive failure points. It remains useful as an Earth test article because forces and latch behavior are easy to instrument. The spherical single-launcher unit is the stronger lunar baseline if it can reliably self-settle and aim.

![][image7]

*Figure 6\. Existing Moon Hound Micro sketch. The diagram illustrates the charge-aim-release-flight-land-reset sequence; numerical performance remains unverified.*

## **6.4 Hex Seed and flywheel variants**

The Hex Seed concept protects cameras inside recessed ports and places the center of mass low. A mobile internal camera can look through different ports. This is mechanically attractive for all-direction sensing, although internal translation and rotation increase complexity. The flywheel hopper stores energy in a high-speed rotor and transfers angular momentum to the shell through controlled braking. It removes an external launcher but introduces high-speed containment, bearing, balance and rotor-failure risks. It should remain a later laboratory comparison until containment energy and vibration are proven.

![][image8]

*Figure 7\. Existing Hex Seed Hopper sketch. The protected sensor-port concept is retained; the quoted hop range is not a verified specification.*

![][image9]

*Figure 8\. Existing flywheel hopper sketch. This is a research alternative, not the baseline, because rotor containment and brake impulse require extensive proof.*

## **6.5 Moon Hound functional sequence**

11. Acquire a local terrain model from multiple viewpoints; reject a target if the landing zone cannot be bounded.  
12. Select a short hop with reserve distance from crater rims, shadow boundaries and communication loss zones.  
13. Orient the body using the internal kick mechanism or external contact with the ground.  
14. Tension the spring slowly and transfer load to a positive latch so the motor is not continuously loaded.  
15. Confirm orientation, latch state, thermal state, battery reserve and target confidence.  
16. Release the launcher. During flight, use only limited attitude correction; the hop remains primarily ballistic.  
17. Land on the rounded shell or compliant contact elements, settle, self-check and re-establish navigation.  
18. Transmit a compact result packet before committing to another hop. If damaged, become a stationary beacon or sensor.

## **6.6 ASETAMO and AAGS**

ASETAMO is a six-wheel rover concept using rocker-bogie suspension and Active Adaptive Grouser System contacts. Individual radial elements extend or retract to change contact area, traction and obstacle engagement. The same elements can inject or sense small vibrations to estimate whether the substrate is compact, loose or potentially hollow. The idea is valuable because one contact system can act as wheel tread, claw, wide foot and sensor. Its weakness is actuator count and dust exposure. \[D2\]

The first AAGS prototype should be one instrumented wheel with four to eight active elements, not a full rover. It is tested on compact plate, angular rock, sand and mixed simulant. Required metrics include sinkage, slip, axle shock, actuator energy, recovery after one jammed element and useful seismic signal-to-noise.

## **6.7 Genesis fleet**

| Machine | Primary role | Power approach | Key risk |
| ----- | ----- | ----- | ----- |
| Voxel Scout | 3D mapping, assay planning and confidence model. | Battery or tether. | Sensor interpretation and dust on optics. |
| L-01 tethered rover | Long-duration work near fixed infrastructure. | High-voltage lightweight tether with local conversion. | Cable snag, abrasion and electrical isolation. |
| L-100 Scarab | Rough-terrain transport and light excavation support. | Battery or tether. | Track wear, flipper joints and entrapment. |
| L-300 Iron Badger | Heavy scraping, breaking and tool carriage. | Cable, battery exchange or mobile power module. | Reaction loads and tool wear. |
| L-400 Centaur/Mule | Containers, tanks, ore and module handling. | Battery exchange or cabled route. | Stability, braking and standardized load restraint. |
| L-050 Mole | Small tunnel, void and collapsed-zone access. | Tether preferred. | Communication loss and retrieval. |
| L-600 Python | Place cables, hoses and sensors through constrained routes. | Tether or small battery. | Buckling, snagging and connector damage. |
| Skip Hoist | Lift bulk material at a fixed excavation. | Stationary high-power winch. | Cable fatigue, bucket swing and anchor loads. |

## **6.8 Lunar Mule**

The Lunar Mule is a logistics function rather than one fixed vehicle shape. Early versions use a low, wide wheeled or tracked chassis with a standard cargo deck and hard points. Later versions may be self-propelled cargo frames that accept AAGS wheel pods. The cargo container carries its own identity, center-of-mass estimate, tie-down state, thermal limits and destination. A Mule does not lift an unknown load until another asset confirms the load path and attachment points.

## **6.9 Common interfaces**

| Interface | Requirement |
| ----- | ----- |
| Mechanical | Four accessible lifting points, towing eye, recovery hard point, common tool plate and no hidden single-use fasteners. |
| Electrical | Protected DC connector, pre-charge, isolation monitoring, load identity and safe disconnect. |
| Data | Deterministic local bus, time sync, health packet and minimal emergency command set. |
| Navigation | Fiducial markers visible to multiple sensor types and known reference surfaces for docking. |
| Service | Replaceable covers, captured fasteners, tool clearance, dust traps outside the seal and manipulable handles. |
| Recovery | Ability to be towed or powered externally after loss of onboard energy. |

# **7\. Site selection and survey campaign**

## **7.1 Reference region**

The south-polar region is the reference because it offers potential access to water ice and terrain with extended illumination. This does not select a specific crater or ridge. The final site must balance landing safety, horizon visibility, direct-to-Earth geometry, resource access, thermal conditions, slopes, boulder density, construction material and protected heritage or science areas. \[E2, E5\]

## **7.2 Functional separation**

![][image10]

*Figure 9\. Reference zoning. Distances are placeholders and must be determined by site-specific plume, traffic, radiation and thermal analysis.*

The landing zone is separated from the habitat, power field and mine gateway. The power ridge favors illumination and radiator view. The base core occupies stable terrain that can accept imported pressure vessels and shielding. Moonforge is separated because high-temperature processing, raw feedstock and gas storage create different hazards. The mine gateway sits at the transition to shadowed or steep terrain and provides power conversion, communication and material transfer.

## **7.3 Survey sequence**

19. Orbital reconnaissance combines topography, illumination, thermal maps, radar, neutron or spectral data and communication geometry.  
20. A lander deploys weatherless-environment monitors: dust, thermal, radiation, surface charging and seismic sensors.  
21. Moon Hounds place short-range beacons and inspect obstacles that are difficult for the main rover.  
22. ASETAMO and Voxel Scout create a traversability and substrate-confidence map.  
23. Shallow drill and trench tests measure mechanical behavior, thermal properties and volatile loss during handling.  
24. A small resource demonstrator processes known weighed samples and closes the mass balance.  
25. Only after the above data are reconciled is the permanent base centerline and mine route frozen.

## **7.4 Site rejection criteria**

* Unacceptable landing slope, boulder field or plume-ejecta path.  
* Communication geometry that creates prolonged single-link dependence.  
* Illumination too intermittent for the planned storage and survival architecture.  
* Resource indicators without accessible, stable excavation terrain.  
* Route requiring repeated traversal of slopes or shadow boundaries beyond vehicle margins.  
* Inability to separate landing, habitat, power, processing and mine operations.  
* Conflict with protected scientific, historical or internationally coordinated activity zones.

# **8\. Base architecture and construction sequence**

![][image11]

*Figure 10\. Recovered exterior concept sketch from earlier lunar design work. It is used only as a visual study; the engineering layout is defined by the zoning diagrams and requirements in this report.*

## **8.1 Initial base form**

The first base uses imported pressure vessels, power electronics, radiators, airlocks and life-support equipment. Local regolith provides shielding, berms, roads and foundations before it is trusted for pressure-bearing structure. This avoids making crew survival depend on a new lunar manufacturing process. Modules are connected by short serviceable tunnels or flexible pressure-rated links with isolation hatches.

## **8.2 Construction equipment**

Construction is performed by a combination of grading blades, bucket or scraper tools, compacting or sintering equipment, cable-laying robots, cranes or gantries, cargo Mules and inspection scouts. A machine that moves regolith should not also open a clean pressure hatch. Dirty and clean manipulators are separated, and tool exchange occurs at a controlled service rack.

## **8.3 Robotic construction sequence**

26. Install communications, local navigation references and the emergency power bus.  
27. Deploy power generation and storage far enough from the landing zone to avoid plume damage.  
28. Survey and mark the construction footprint; establish no-go zones and material stockpiles.  
29. Grade only the routes that are needed. Excessive disturbance creates dust and consumes tool life.  
30. Stabilize the landing pad, primary haul route and module foundations through compaction, sintering, pavers or imported mats.  
31. Place pressure modules and verify alignment, structural support, electrical isolation and leak integrity.  
32. Install thermal, power, data and fluid connections inside protected trenches or covered service corridors.  
33. Construct berms and apply provisional regolith shielding using low-impact placement methods.  
34. Commission the workshop, spares store and robotic service bay before the mine expands.  
35. Increase shielding and redundancy only after settlement, thermal and radiation monitoring confirm performance.

## **8.4 Regolith shielding**

Regolith shielding reduces radiation and micrometeoroid exposure, but its placement adds load, settlement and dust. The report adopts a provisional meters-scale overburden concept for layout purposes; final thickness is a radiation-transport and structural result. Pressure vessels must carry internal pressure independently. The overburden containment system should prevent loose material from loading hatches, radiators, windows and emergency exits.

## **8.5 Surface stabilization**

The sequence should prioritize high-traffic and high-consequence surfaces: landing pad, ascent pad, habitat apron, power-service lanes, mine haul road and precision docking points. Candidate methods include compaction, microwave or solar sintering, pavers, sulfur-free binders, geotextile-like imported meshes or mechanical confinement. Each method is evaluated for energy, dust generation, repairability and contamination, not only compressive strength.

## **8.6 Lava-tube option**

A lava tube or natural void could provide shielding and thermal stability, but it should not be assumed available at the chosen site. A void requires mapping, structural assessment, access construction, communication and emergency egress. The baseline remains a surface outpost with engineered shielding. A verified tube becomes an expansion option, not a prerequisite.

## **8.7 Workshop and service bay**

The workshop is the operational heart of the base. It includes clean and dirty bays, robotic fixtures, metrology, test power, thermal conditioning, spare actuators, seal storage, cable repair, additive manufacturing and quarantine. Every robot must be serviceable without bringing raw regolith into the clean bay. The workshop should be commissioned before production mining because maintenance hours will initially dominate output.

![][image12]

*Figure 11\. Recovered workshop and drill-head concept crop. The final design requires open robotic access, lifting fixtures and replaceable wear modules.*

## **8.8 Habitat configuration**

| Zone | Function | Isolation principle |
| ----- | ----- | ----- |
| Airlock / suitport | Human and tool transfer. | Keep suits outside the main clean volume; independent pressure door. |
| Command and medical | Operations, refuge and treatment. | Protected emergency bus and communications. |
| Habitation | Sleep, food, hygiene and exercise. | Separated from dirty maintenance traffic. |
| Laboratory | Sample handling and science. | Glovebox, controlled atmosphere and provenance tracking. |
| Life support | Air revitalization, water recovery and waste. | Redundant loops and replaceable cartridges. |
| Storm shelter | Solar-particle-event refuge. | Maximum practical shielding and independent consumables. |
| Clean workshop | Electronics, seals and optics. | Positive cleanliness control relative to adjacent zones. |

# **9\. Genesis mine and LITHOS control layer**

## **9.1 Mine objective**

The initial mine is a resource-characterization and process-demonstration site. Its purpose is to determine what can be recovered, at what energy cost, with what equipment wear and contamination. Production targets remain secondary until the mass balance closes. The mine may work two distinct feedstocks: relatively dry regolith for oxygen, metals and construction material, and volatile-bearing polar regolith for water extraction.

![][image13]

*Figure 12\. Genesis mining and processing flow. Assay gates and safe-storage states prevent uncontrolled material movement.*

## **9.2 Prospecting**

Prospecting combines orbital data, surface imaging, neutron or spectroscopic measurements, ground-penetrating radar where appropriate, thermal probes, shallow drilling and weighed sample processing. A resource cell in the digital twin stores location, depth, confidence, physical properties, volatile loss history and assay method. A colorful map is not a reserve statement.

## **9.3 Excavation methods**

Vacuum and low gravity change excavation. Lower vehicle weight reduces traction and reaction force, while angular material increases wear. Tools should use low cutting depth, controlled speed and anchoring or counterforce. Candidate methods include scraper drums, bucket wheels, augers, rippers, percussion, heated probes and cable-supported excavation. The chosen method depends on feedstock and terrain; no single tool is optimal for both hard sintered crust and loose cold regolith.

## **9.4 Tethered power**

Tethered robots are attractive in fixed work zones because they avoid carrying large batteries into cold or high-duty operations. A lightweight high-voltage pair reduces conductor mass, with local conversion at the robot. The tether must be abrasion-resistant, visible to navigation, routed through low-stress guides and recoverable after a robot failure. Isolation monitoring and arc management are mandatory in vacuum.

## **9.5 Haulage**

Short haul routes use Mules, hoppers, covered bins or cable systems. Fixed high-throughput routes can justify a rail, conveyor or skip-hoist system. The Skip Hoist is efficient where material can be pushed to a central loading point and lifted to processing, but its anchor, cable fatigue and bucket dynamics must be tested. Dust containment and sample provenance are more important than speed during the pilot phase.

## **9.6 LITHOS supervisory control**

LITHOS presents the mine as a voxelized digital twin containing geometry, material class, confidence, hazards and allowed operations. Remote participants or planning software propose actions. A simulator checks geometry and safety constraints. A responsible layer approves a limited command packet. The robot then plans local motion and rejects unexpected conditions. This separation prevents an operator with delayed video from directly driving a high-energy tool into an unseen obstacle. \[D3\]

## **9.7 Packet Burst command model**

| Field | Example |
| ----- | ----- |
| Work zone | Polygon or volume in the shared map. |
| Objective | Remove up to a defined mass or expose a defined face. |
| Allowed tools | Specific attachment and operating mode. |
| Limits | Force, torque, depth, temperature, speed, energy and dust threshold. |
| Validity | Start time, expiry time and required map version. |
| Abort conditions | Human detection, localization uncertainty, tether tension, over-temperature, loss of comm or unexpected void. |
| Return data | Mass moved, energy used, wear, imagery, samples and updated confidence. |

## **9.8 Mine safety states**

* Safe hold: tool stopped, load supported and brakes applied.  
* Safe retreat: return along a verified path before energy or thermal margin is exhausted.  
* Safe dump: place material in a defined containment zone rather than carrying an unstable load.  
* Safe isolate: disconnect a faulty processing module and close valves or power contactors.  
* Safe beacon: immobilized robot remains a navigation and sensor node.  
* Safe abandonment: document hazards and prevent other robots from attempting an unsafe recovery.

# **10\. Moonforge resource processing and manufacturing**

## **10.1 Purpose**

Moonforge converts local material into useful products while preserving measurement credibility. The first outputs are not complex machines. They are graded aggregate, sintered pads, shielding blocks, glass or ceramic coupons, recovered water, oxygen test batches and simple cast or printed brackets. Every batch carries material provenance and mechanical test data.

## **10.2 Dry-regolith line**

36. Receive sealed or covered bins from the mine and weigh gross mass.  
37. Sample and archive representative material before processing.  
38. Screen by size and remove oversized rocks for separate crushing or construction use.  
39. Dry and thermally condition the feed while measuring released volatiles.  
40. Divert construction fractions to pavers, sintering or shielding tests.  
41. Process selected material for oxygen extraction or metal-rich residue.  
42. Separate, store and certify gases; cool solids in controlled containers.  
43. Test residue for casting, powder processing, glass or ceramic production.  
44. Record net product, energy, consumables, electrode wear, contamination and rejected mass.

## **10.3 Volatile-bearing line**

Cold volatile-bearing regolith should be captured with minimal heating and transported in insulated sealed containers. The processing chamber heats a weighed batch under controlled pressure. Released gas passes through filters and cold traps. Water is separated from carbon-bearing, sulfur-bearing or other volatile species. The line measures how much water is recovered, how much remains in tailings, how much is lost to surfaces and how much energy is consumed.

## **10.4 Oxygen extraction**

Molten-salt electrolysis is one candidate because it can extract oxygen from solid regolith simulant and leave metal-rich residue. ESA reported laboratory extraction at approximately 950°C and demonstrated high oxygen recovery from simulant, but a lunar plant must solve reactor materials, electrode life, salt handling, gas purification, heat recovery and maintenance under reduced gravity and vacuum. \[E7, E8\]

## **10.5 Construction products**

| Product | Near-term use | Qualification needed |
| ----- | ----- | ----- |
| Screened aggregate | Berms, fill, road base and shielding. | Particle distribution, settlement and dust release. |
| Sintered paver | Traffic lanes, landing-pad tests and equipment pads. | Thermal cycling, cracking, abrasion and repair. |
| Glass / ceramic | Windows outside pressure boundary, insulation, tiles and containers. | Optical, thermal, impact and vacuum behavior. |
| Metal-rich residue | Casting or powder feed for simple brackets and counterweights. | Composition, porosity, fatigue and joining. |
| Recovered oxygen | Process gas, life-support supplement or propellant feed after purification. | Purity, storage, leak control and system certification. |
| Recovered water | Life support, shielding, electrolysis or thermal storage after treatment. | Contaminants, microbiological control and closed mass balance. |

## **10.6 Manufacturing hierarchy**

Manufacturing expands from low-consequence to high-consequence parts. Level 0 produces bulk fill and shielding. Level 1 produces non-structural geometry. Level 2 produces tested structural brackets and tool bodies. Level 3 produces pressure-adjacent or rotating parts only after process control and nondestructive inspection mature. Electronics, high-speed bearings and life-critical seals remain imported until a separate qualified supply chain exists.

## **10.7 Heat integration**

Moonforge is a thermal system as much as a chemical plant. High-temperature reactors, ovens and sintering tools generate heat that may preheat feedstock or support thermal storage. Radiators and shadow shields reject unavoidable waste. Heat paths must be switchable so a failed process does not overheat the base microgrid or nearby cryogenic storage.

# **11\. Power, energy storage and thermal control**

![][image14]

*Figure 13\. Reference microgrid. Industrial loads absorb variability; life support and command remain on protected buses.*

## **11.1 Power sources**

Early operations rely on distributed solar arrays and energy storage placed on terrain with favorable illumination. Arrays should be physically separated into fields so one plume, cable fault or local shadow does not remove all generation. A later fission surface power unit can provide continuous kilowatt-class power and reduce dependence on long-duration storage. NASA has studied 10 kWe and 40 kWe concepts, including remote deployment of a reactor at least a kilometer from users. \[E10\]

## **11.2 Storage**

No single storage technology is ideal. Batteries provide high round-trip efficiency and fast response but degrade with cycle, radiation and temperature. Regenerative fuel cells can store larger amounts for long dark periods but add tanks, pumps and gas management. Thermal storage can preserve heat for survival loads. Mobile battery or fuel-cell Mules can move energy to shadowed work sites. The architecture combines technologies according to duration and criticality.

## **11.3 Distribution**

A segmented high-voltage DC trunk reduces conductor mass for long distances. Local converters create robot, habitat and process voltages. Each branch has isolation monitoring, pre-charge, current limiting, arc detection and remote mechanical disconnect. The emergency bus is physically and electrically separated from industrial converters. The base must demonstrate black start from a cold, unpowered state.

## **11.4 Load priority**

| Priority | Loads | Behavior during shortage |
| ----- | ----- | ----- |
| P0 | Crew refuge, pressure control, critical heaters, command receiver and emergency lighting. | Never automatically shed; independent reserve. |
| P1 | Main life support, medical, core communications, clocks and thermal control. | Reduced mode with protected minimum. |
| P2 | Navigation beacons, workshop preservation and robot recovery. | Scheduled and duty-cycled. |
| P3 | Routine mobility, charging and science. | Deferred when storage margin falls. |
| P4 | Excavation, processing, sintering and nonessential manufacturing. | Interruptible; absorbs surplus generation. |

## **11.5 Thermal control**

In vacuum, radiators need a clear view to cold space and protection from dust, engine plumes and hot terrain. Heat pipes or pumped loops move heat from electronics and processing equipment. Survival heaters prevent batteries, seals and lubricants from falling below qualified temperature. Cryogenic water or propellant storage requires sunshields, low-conductance supports and separation from hot processing.

## **11.6 Energy accounting**

Every resource process records electrical energy, thermal energy, standby energy and recovery efficiency. A plant that produces water but consumes more imported reactant or replacement mass than the water offsets is not yet useful. Energy and maintenance accounting should be visible in the same LITHOS dashboard as production.

# **12\. Human systems, safety and emergency operations**

## **12.1 Crew arrival gate**

Crew arrival is a verified readiness decision, not a symbolic milestone. Before occupancy, the site demonstrates redundant power, pressure integrity, life-support endurance, radiation monitoring, clean communication, navigation, pre-positioned consumables, medical capability, a storm shelter and at least two independent means of reaching the ascent vehicle or refuge.

## **12.2 Dust control for people**

Suitports keep the dustiest parts of the suit outside the main habitat. Samples enter through gloveboxes or sealed transfer containers. Tools are cleaned in stages and inspected before crossing into the clean workshop. Particle counters, filter pressure drop and seal torque provide trend data. A cleaning procedure that visibly removes dust but drives fine particles into seals is unacceptable.

## **12.3 Fire and atmosphere hazards**

The lunar exterior does not support fire, but the pressurized habitat contains oxygen, polymers, batteries and electrical equipment. Fire detection, compartment isolation and low-toxicity materials are essential. Oxygen generation, hydrogen production and high-pressure gas storage are isolated from habitation. Gas inventories are minimized, monitored and automatically isolated after a leak or abnormal temperature.

## **12.4 Radiation emergency**

Space-weather warnings are distributed through Kage Relay and Silent Lantern channels. The crew moves to a storm shelter with the highest practical shielding and independent communications, water and carbon-dioxide removal. Robotic surface operations enter safe states to preserve power and prevent additional faults during the event.

## **12.5 Rescue architecture**

* Two independent communication paths from habitat to Earth or relay service.  
* A pressurized or rapidly configurable rescue rover where mission duration justifies it.  
* Recovery hard points on every crew-rated vehicle and marked safe corridors.  
* Pre-positioned oxygen, water, thermal blankets, medical equipment and portable power.  
* An ascent vehicle or refuge strategy with verified readiness and launch constraints.  
* Robot capability to clear a blocked route, tow a disabled vehicle and inspect an external leak without crew exposure.

## **12.6 Human-machine roles**

Humans set goals, resolve ambiguity, perform scientific judgment and authorize changes to operating envelopes. Robots perform repetitive exposure-intensive tasks, prepare work zones and collect data. The system should not require continuous joystick control from Earth. Nor should autonomy be allowed to modify safety constraints without explicit review.

# **13\. Maintenance, spares and reliability**

## **13.1 Reliability philosophy**

Lunar equipment fails through wear, dust, thermal cycling, radiation, connector degradation, lubrication loss, software errors and handling damage. Reliability therefore depends on architecture as much as component quality. A replaceable actuator that can be changed by a robot may be more valuable than a theoretically longer-life sealed assembly that cannot be serviced.

## **13.2 Line-replaceable units**

| Unit | Replacement approach |
| ----- | ----- |
| Wheel / track module | External lifting points, blind-mate power/data and mechanical lock visible to cameras. |
| AAGS contact element | Replaceable cartridge or sector; failed element locked into safe position. |
| Camera / lidar | Recessed window, dust shield, calibration target and removable sensor pod. |
| Battery module | Thermally conditioned cassette with pre-charge and fire isolation. |
| Power converter | Slide-in sealed module with external disconnect and test port. |
| Tool head | Common mechanical plate, encoded identity and protected hydraulic/electrical coupler. |
| Seal / hatch drive | Captured fasteners, alignment guides and manual or robotic override. |
| Relay avionics | Redundant processing lanes and recoverable software image before physical replacement. |

## **13.3 Spares strategy**

Spare selection is based on failure consequence, probability, commonality and lead time. High-commonality actuators, power modules, cameras, connectors and seals are stocked. Heavy low-complexity structures are candidates for local fabrication. Precision rotating parts, radiation-tolerant electronics and certified pressure components remain imported. A spare without the fixture, procedure and robot access to install it is not a real spare.

## **13.4 Condition monitoring**

Robots trend motor current, gearbox vibration, bearing temperature, seal torque, thermal resistance, insulation resistance, battery impedance, camera contamination and localization residuals. Maintenance is scheduled when degradation is measurable, but hard life limits remain for high-consequence parts. Each repair updates the digital twin and component genealogy.

## **13.5 Dust-tolerant mechanics**

Sliding seals and exposed precision joints are minimized. Mechanisms use labyrinths, sacrificial wipers, compliant covers, coarse clearances where accuracy allows and hard stops that carry impact without loading motors. Components should continue in a reduced mode after partial contamination. Dust tests include angular simulant, vacuum and thermal cycling rather than clean-room cycle tests alone.

# **14\. Development, testing and deployment roadmap**

![][image15]

*Figure 14\. Development roadmap. Each phase is entered only after objective gates are passed.*

## **14.1 Phase 0 \- component evidence**

Build one mechanism at a time: Moon Hound launcher and latch, AAGS wheel sector, tether power converter, dust-resistant connector, scraper tool, sealed sample bin and Lantern beacon. Test cycle life, contamination, vacuum behavior, temperature and failure modes. A mechanism that works once in room air is not ready for a rover.

## **14.2 Phase 1 \- integrated terrestrial analog**

Operate a small fleet in a quarry, cold chamber and regolith testbed. The test site includes a base gateway, mine gateway, beacons, constrained work zones and a LITHOS digital twin. Robots perform route mapping, cable placement, excavation, material transfer and automated recovery. Human controllers experience realistic delay and limited bandwidth.

## **14.3 Phase 2 \- orbital service demonstration**

Demonstrate autonomous rendezvous, crosslink routing, timing transfer, target inspection and controlled capture using a cooperative inert object. The mission must include abort, safe mode and disposal. Satellite reclaim is not attempted with an uncontrolled third-party target in the first flight.

## **14.4 Phase 3 \- lunar pathfinder**

Deploy a small power system, one relay or direct-to-Earth terminal, several Lanterns, Moon Hound scouts, a compact rover, shallow sampling and environmental monitors. The pathfinder returns data on dust, thermal cycles, navigation, latch behavior, spring energy, wheel wear and communication coverage.

## **14.5 Phase 4 \- robotic construction outpost**

Deliver power, cargo Mules, construction tools, service fixtures and an uncrewed pressure module. Robots stabilize routes, install cables, place shielding and commission the workshop. The pressure module is tested unmanned through thermal and leak cycles.

## **14.6 Phase 5 \- pilot mine and Moonforge**

Operate two separate process demonstrations: volatile recovery and dry-regolith oxygen/material processing. The objective is a closed mass, energy and maintenance balance. Production rate is secondary. The site must also show safe tailings placement and contamination control.

## **14.7 Phase 6 \- crew-ready base**

Crew arrives only after the robotic site demonstrates readiness gates and a safe abort plan. Early crew expands science and maintenance but does not become the only way to keep the base functioning. The objective is to reduce human exposure to dust, radiation and heavy construction.

## **14.8 Core verification gates**

| Gate | Evidence |
| ----- | ----- |
| Mobility | Representative terrain traversed with defined slip, energy and recovery margin. |
| Dust | Mechanisms complete target cycles in contaminated thermal-vacuum conditions. |
| Communications | Coverage, latency, store-and-forward and emergency paths demonstrated with failures injected. |
| Autonomy | Safe stop, retreat and recovery demonstrated after sensor, actuator and link faults. |
| Power | Black start, bus isolation, load shedding and survival duration demonstrated. |
| Resource | Input and output mass, purity, energy and consumables independently measured. |
| Construction | Module placement, alignment, connections and shielding performed without crew. |
| Human readiness | Pressure, life support, storm shelter, rescue and contamination controls verified. |

# **15\. Indicative budgets and operating scenarios**

| PLANNING ASSUMPTION The following ranges are not mission commitments. They provide a consistent scale for subsystem trades and must be replaced by a formal mass, power, thermal and trajectory model. |
| :---- |

## **15.1 Power growth envelope**

| Phase | Illustrative generation | Primary loads |
| ----- | ----- | ----- |
| Pathfinder | 5-20 kW peak solar | Relay terminal, heaters, small rover, instruments and short process tests. |
| Construction outpost | 50-150 kW | Heavy mobility, cable deployment, workshop, sintering and module conditioning. |
| Pilot mine | 0.25-1 MW | Excavation, haulage, volatile extraction, oxygen process and thermal management. |
| Industrial base | 1-5 MW and above | Parallel processing, propellant, manufacturing, expanded habitat and logistics. |

Average available power can be far below installed peak because of illumination, shadowing, array temperature, dust, eclipse, storage losses and maintenance. The design should operate safely at a reduced fraction of nameplate power.

## **15.2 Resource throughput envelope**

| Phase | Feedstock target | Purpose |
| ----- | ----- | ----- |
| Resource demo | 10-100 kg/day | Validate sampling, handling and net recovered product. |
| Pilot line | 1-10 t/day | Establish wear, maintenance, heat recovery and quality control. |
| Production line | 10-100 t/day | Support construction, oxygen or water production after reserve confirmation. |

These throughput targets should not be applied to a volatile deposit until the accessible concentration and losses are measured. A high mass-throughput dry-regolith line and a lower-throughput cold volatile line may have completely different equipment.

## **15.3 Illustrative robotic outpost inventory**

| Asset | Illustrative count | Reason |
| ----- | ----- | ----- |
| Orbital relay nodes | 2-4 initial; expandable | Coverage and redundancy without committing to a full constellation. |
| Surface Lanterns | 12-50 | Route markers, shadow gateways and local mesh. |
| Moon Hound scouts | 20-100 | Distributed low-cost reconnaissance and sensor placement. |
| ASETAMO rovers | 2-4 | Route proving, science and recovery redundancy. |
| L-01 tethered units | 4-12 | Long-duration fixed-zone tasks. |
| Scarab / Badger work robots | 4-10 | Excavation, tool carriage and construction. |
| Lunar Mules | 4-12 | Cargo, power modules and material containers. |
| Processing lines | 1 volatile \+ 1 dry pilot | Separate chemistry, thermal and contamination requirements. |
| Service gantries | 2 | One can repair the other and handle modules safely. |

## **15.4 Example 24-hour operating cycle**

| Window | Activity |
| ----- | ----- |
| 00:00-04:00 | Orbital data sync, route update, low-power inspection and battery conditioning. |
| 04:00-10:00 | Excavation and haulage during favorable thermal/power conditions. |
| 10:00-14:00 | Processing line feed, maintenance inspection and sample analysis. |
| 14:00-18:00 | Construction or route stabilization using available surplus generation. |
| 18:00-22:00 | Robot recovery, charging, wear inspection and spare preparation. |
| 22:00-24:00 | Digital-twin reconciliation, command packet approval and safe-state verification. |

Actual lunar operations follow illumination and thermal windows rather than an Earth day. The table illustrates the need to separate production, maintenance and data reconciliation into explicit cycles.

# **16\. Risk register and mitigation plan**

| Risk | Consequence | Primary mitigation | Low-cost proof |
| ----- | ----- | ----- | ----- |
| Dust jams launcher or wheel contacts | Scout or rover immobilized. | Labyrinths, compliant covers, coarse tolerances, replaceable cartridges and degraded mode. | Thousands of cycles in angular simulant under vacuum/thermal cycling. |
| Moon Hound lands unpredictably | Loss into crater or communication shadow. | Short hops, bounded landing zones, bottom-heavy body and pre-hop terrain confidence. | Instrumented drop/hop arena with irregular rock and low-g simulation. |
| Tether snags or arcs | Power loss, robot entrapment or damage. | Guides, tension sensing, isolation monitoring and retrieval path. | Rock-field cable test with deliberate snag and insulation defects. |
| Relay geometry insufficient | Navigation or command gaps. | Coverage simulation, direct-to-Earth fallback, surface beacons and multiple providers. | Hardware-in-loop link and orbit simulator. |
| Solar power interrupted | Thermal or mission loss. | Distributed fields, storage, priority buses and optional fission. | Black-start and multi-day survival test. |
| Resource grade too low | Mine has negative value. | Prospecting-first program and small process demonstrator. | Process known simulant mixtures with blinded assay. |
| Excavator lacks traction | Low productivity and high wear. | Anchors, counterforce, low-depth cuts, tether or cable-supported tools. | Force-controlled excavation in low-normal-force rig. |
| Oxygen reactor corrodes or fouls | Plant outage and contamination. | Replaceable hot zone, material coupons, heat recovery and conservative batch size. | Long-duration hot-salt test with repeated maintenance. |
| Regolith shielding overloads module | Structural damage or blocked exits. | Independent pressure vessel, load-spreading containment and settlement monitoring. | Full-scale section with cyclic loading and emergency removal. |
| Cyber or stale command executes | Unsafe tool motion. | Signed expiring packets, work envelope, local safety kernel and independent stop. | Fault-injection exercise with delay and corrupted commands. |
| Crew arrives before site maturity | Life-critical dependence on unverified systems. | Objective readiness gates and pre-positioned abort capability. | Full-duration analog mission with failures. |
| Salvage creates debris | Orbital hazard and liability. | Cooperative demo first, target permission, abort corridor and containment. | Air-bearing or suspended capture test with tumbling target. |

## **16.1 Highest-value early tests**

45. Moon Hound latch, spring and self-settling body in contaminated thermal-vacuum cycling.  
46. One AAGS wheel sector with a jammed-element test and measured axle shock.  
47. Tethered rover power delivery across a rough route with retrieval after simulated failure.  
48. Closed mass-balance volatile extraction using weighed samples and cold traps.  
49. Robotic replacement of a wheel module, sensor pod and power converter using flight-like access.  
50. Integrated safe-stop demonstration after communication loss, map mismatch and localization uncertainty.  
51. Landing-plume and dust-zone model tied to a physical regolith-ejection test.  
52. Power black start and emergency-bus endurance under sequential faults.

# **17\. Governance, legal and environmental constraints**

## **17.1 International framework**

The Outer Space Treaty establishes peaceful use, freedom of exploration, non-appropriation, state responsibility, liability and avoidance of harmful contamination. The Moon Agreement has a smaller group of parties and addresses lunar resources more specifically. The Artemis Accords provide non-binding principles among signatories, including interoperability, emergency assistance, registration, heritage protection, resource use, deconfliction and orbital-debris mitigation. \[E14, E15\]

## **17.2 Operational deconfliction**

A base should publish location, general activity type, communication channels, landing windows and hazard zones to the extent compatible with safety and commercial confidentiality. Temporary safety zones are based on physical risk such as plume ejecta, high-energy tools, cryogenic release or radio interference. They are not territorial claims.

## **17.3 Heritage and science protection**

Apollo, Luna and other historic sites must be protected from plume, dust and traffic. Scientifically pristine cold traps or volatile deposits may be altered by exhaust and human activity. The site plan should maintain protected reference areas and monitor contamination introduced by landers, processing and habitation.

## **17.4 Resource and material accounting**

Material records identify where feedstock was collected, how it was processed, what contaminants were introduced and where products were used. This supports engineering traceability, environmental monitoring and future legal obligations. A production dashboard without provenance is inadequate.

## **17.5 Orbital debris and end of life**

Every relay, tug and service craft requires an end-of-life plan before launch: controlled relocation, graveyard orbit where appropriate, impact in an approved location or retrieval. A disabled Kage Relay must not become the first target that Orbital Reclaim is forced to rescue.

# **18\. Conclusions**

A realistic lunar industrial base begins as a measurement and maintenance system, not as a city. The first value comes from reliable communication, terrain knowledge, safe routes, power distribution and the ability to repair robots. Mining follows only after the resource and process are measured. Human occupancy follows only after the robotic site can support and rescue people.

The strongest original concepts are the division of work among specialized modular machines, the Moon Hound strategy of slowly storing energy for short low-gravity hops, the AAGS idea of combining traction and substrate sensing, the LITHOS command-packet model and the attempt to connect orbital salvage with lunar material use. Their main weakness is not physical impossibility but integration complexity. The response is to narrow each first prototype, prove its dominant failure mode and keep unsupported performance numbers out of requirements.

The recommended first hardware program is therefore modest: one Moon Hound launcher, one AAGS wheel sector, one tethered work rover, one Lantern beacon, one sealed sample container and one small mass-balance extraction rig. Together they test the central logic of the larger system without requiring a launch vehicle, a habitat or a full mine.

| FINAL ENGINEERING POSITION The system is credible as a staged research and infrastructure architecture. It is not credible as a single-step self-sufficient lunar colony. Its success depends on disciplined interfaces, dust control, power resilience, maintenance access, accurate resource accounting and the willingness to stop expansion when measurements do not support it. |
| :---- |

# **Appendix A \- Subsystem interface summary**

| Interface | Minimum data or hardware |
| ----- | ----- |
| Asset identity | Unique ID, configuration, software version, owner/operator and hazard class. |
| Health packet | Position, time, power, thermal state, faults, autonomy mode and communication quality. |
| Cargo metadata | Mass, center of mass, attachment points, thermal limits, contamination and destination. |
| Tool metadata | Allowed chassis, force/torque limits, power, duty cycle, wear state and safe position. |
| Map object | Geometry, confidence, timestamp, source sensors, hazards and permitted operations. |
| Command packet | Objective, zone, limits, validity, map version, abort conditions and return data. |
| Power coupler | Voltage class, current limit, pre-charge, isolation, latch state and emergency disconnect. |
| Mechanical coupler | Load rating, alignment tolerance, positive lock, visual confirmation and recovery release. |
| Navigation marker | Position estimate, covariance, clock, code identity and health status. |
| Material batch | Source cell, mass, assay, processing history, contamination, test results and final use. |

# **Appendix B \- Preliminary requirements**

| ID | Requirement |
| ----- | ----- |
| SYS-001 | The integrated system shall reach a safe state after loss of Earth communication without relying on a new command. |
| SYS-002 | No single industrial power fault shall remove the emergency habitat and command bus. |
| COM-001 | Relay and surface-network designs shall support interoperable lunar communication and navigation standards selected by the program. |
| COM-002 | Navigation outputs shall include integrity and uncertainty, not only position. |
| ROB-001 | Every mobile asset shall provide an external recovery point and a method for external power or towing. |
| ROB-002 | A failed non-critical actuator shall place itself or be placeable into a mechanically safe condition. |
| HOP-001 | A Moon Hound hop shall be inhibited unless target-zone confidence, orientation, latch state and communication margin meet defined thresholds. |
| HOP-002 | Stored spring or flywheel energy shall have a controlled safing and maintenance-release procedure. |
| MIN-001 | The mine shall measure input mass, product mass, rejected mass and unaccounted loss for every process batch. |
| MIN-002 | A remote planning interface shall not directly bypass local collision, force, thermal or work-zone limits. |
| BAS-001 | Landing and ascent plume hazards shall be physically separated from habitat, power and processing assets. |
| BAS-002 | Pressure vessels shall carry pressure loads independently of local regolith shielding. |
| DUST-001 | Raw regolith shall not enter a crew clean zone without controlled containment and transfer. |
| PWR-001 | The microgrid shall demonstrate black start and sequential isolation of failed branches. |
| MNT-001 | Line-replaceable units shall be accessible with the program robotic manipulator and flight-like tools. |
| CREW-001 | Crew deployment shall require verified shelter, power, communication, life support, rescue and contamination-control gates. |

# **Appendix C \- Earth test matrix**

| Test article | Environment | Primary measurements | Pass direction |
| ----- | ----- | ----- | ----- |
| Moon Hound launcher | Vacuum, thermal cycling, angular simulant | Stored energy, release timing, jam rate, landing shock and self-settling. | Repeatable safe hops and controlled safing after a fault. |
| AAGS wheel sector | Mixed terrain, dust, low-normal-force rig | Slip, sinkage, axle shock, actuator energy and jam tolerance. | Improved mobility with continued operation after one failed element. |
| Tethered rover | Rock field, vacuum electrical chamber | Cable tension, abrasion, arc behavior, retrieval and conversion efficiency. | No unsafe arc; recoverable after snag and power fault. |
| Lantern beacon | Cold chamber, shadowed terrain analog | Link margin, clock drift, optical visibility and battery survival. | Reliable emergency packet and health flag at minimum energy. |
| Sample container | Vacuum, cryogenic and warm transfer | Mass loss, seal leakage, contamination and robotic handling. | Known retained mass and repeatable clean transfer. |
| Volatile extraction rig | Thermal-vacuum with simulant mixtures | Recovered water, residual water, contaminants and energy. | Closed mass balance and reproducible yield. |
| Oxygen reactor coupon rig | High temperature and repeated batches | Corrosion, electrode wear, gas purity and heat recovery. | Maintainable hot zone and stable output trend. |
| Robotic service bay | Dusty analog site | Replacement time, tool access, dropped-object recovery. | Robot replaces critical modules without human entry. |
| Microgrid | Hardware-in-loop fault network | Black start, selectivity, priority bus and storage endurance. | No propagation from industrial fault to emergency bus. |
| LITHOS control | Delayed network and injected map faults | Unsafe command rejection, safe stop and audit trail. | All out-of-envelope commands rejected locally. |

# **Appendix D \- Design image interpretation**

The included visual studies are useful for geometry, mechanism discussion and system identity, but several contain illustrative dimensions, performance values and components that have not been calculated. The report therefore adopts only the following visual principles: protected sensor apertures, bottom-heavy self-settling geometry, slow energy accumulation with rapid release, modular external access, clearly separated base zones and robust low-profile surface vehicles.

| Image principle | Retained | Not retained without proof |
| ----- | ----- | ----- |
| Moon Hound Micro | Charge-aim-release-land sequence and positive spring latch. | Quoted hop distance, endurance and payload. |
| Moon Seed Hopper | Rounded protective shell and single retractable launcher. | Specific mass, energy storage and material selection. |
| Hex Seed Hopper | Recessed sensor ports and bottom-heavy body. | Internal camera mechanism until reliability is demonstrated. |
| Hex-Spin Hopper | All-direction protection and regenerative concept. | High-speed flywheel performance and containment. |
| Lunar base concept | Distributed modules, rover access and visible communications. | Unshielded transparent domes and exact architecture. |
| Workshop concept | Large replaceable drill/tool modules and robotic access. | Human-dependent servicing during early deployment. |

# **Appendix E \- References**

**\[E1\]** NASA Science, “Moon Facts.” Gravity, surface temperatures and lunar environment. [Source](https://science.nasa.gov/moon/facts/)

**\[E2\]** NASA Science, “Moon Water and Ices.” Evidence for water and polar permanently shadowed regions. [Source](https://science.nasa.gov/moon/moon-water-and-ices/)

**\[E3\]** NASA Science, “What Hazards Are Caused by Lunar Regolith?” Dust adhesion, abrasion and health/equipment hazards. [Source](https://science.nasa.gov/biological-physical/what-hazards-are-caused-by-lunar-regolith/)

**\[E4\]** NASA, “NASA’s Dust Shield Successfully Repels Lunar Regolith on Moon,” 2025\. [Source](https://www.nasa.gov/image-article/nasas-dust-shield-successfully-repels-lunar-regolith-on-moon/)

**\[E5\]** NASA, “The Harsh Environment of the Lunar South Pole.” Polar temperature and dust overview. [Source](https://www.nasa.gov/reference/moonbase-environment/)

**\[E6\]** NASA Science, “NASA’s LRO: Lunar Ice Deposits are Widespread,” 2024\. [Source](https://science.nasa.gov/solar-system/moon/nasas-lro-lunar-ice-deposits-are-widespread/)

**\[E7\]** ESA, “Oxygen and metal from lunar regolith,” 2019\. [Source](https://www.esa.int/ESA_Multimedia/Images/2019/10/Oxygen_and_metal_from_lunar_regolith)

**\[E8\]** ESA, “ESA opens oxygen plant \- making air out of moondust,” 2020\. [Source](https://www.esa.int/Enabling_Support/Space_Engineering_Technology/ESA_opens_oxygen_plant_making_air_out_of_moondust)

**\[E9\]** NASA, “LunaNet Interoperability Specification,” current NASA page identifying Version 5\. [Source](https://www.nasa.gov/directorates/somd/space-communications-navigation-program/lunanet-interoperability-specification/)

**\[E10\]** NASA NTRS, “40kW Fission Surface Power System Deployability.” [Source](https://ntrs.nasa.gov/citations/20220012395)

**\[E11\]** NASA, “Lunar Surface Technology.” Dust mitigation, landing plume studies and surface systems. [Source](https://www.nasa.gov/lunar-surface-technology/)

**\[E12\]** NASA Science, LRO Science and Data \- CRaTER lunar radiation measurements. [Source](https://science.nasa.gov/mission/lro/science-and-data/)

**\[E13\]** NASA Spaceflight Human-System Standard, Human Performance radiation requirements. [Source](https://www.nasa.gov/reference/4-0-human-performance/)

**\[E14\]** United Nations, Outer Space overview and treaty principles. [Source](https://www.un.org/en/global-issues/outer-space)

**\[E15\]** NASA, Artemis Accords principles. [Source](https://www.nasa.gov/artemis-accords/)

**\[D1\]** Robert Petrušić concept notes: Moon Hound / Moon Tracker \- mechanical lunar reconnaissance hopper, July 2026\. 

**\[D2\]** Robert Petrušić concept notes: ASETAMO and AAGS \- active seismic-tactile planetary mobility, July 2026\. 

**\[D3\]** Robert Petrušić concept notes: Genesis Protocol and LITHOS \- modular robotic mine and constrained digital control, July 2026\. 

**\[D4\]** Robert Petrušić concept notes: Orbital Reclaim / Lunar Salvage Bridge, July 2026\. 

# **Appendix F \- One-page implementation priority**

| Priority | Build or analyze | Reason |
| ----- | ----- | ----- |
| 1 | Moon Hound single-spring ground prototype | Directly tests the most original low-power mobility principle. |
| 2 | AAGS single wheel sector | Determines whether active contacts justify their complexity. |
| 3 | Lantern beacon and delayed mesh network | Enables later robots and is testable without a launch. |
| 4 | Tethered rover power and retrieval rig | Addresses a key mine-energy problem with accessible hardware. |
| 5 | LITHOS command-packet simulator | Proves safe distributed control before high-energy tools exist. |
| 6 | Closed mass-balance water extraction bench | Prevents unsupported resource-production claims. |
| 7 | Robotic service fixture and common interfaces | Reduces future design divergence and maintenance cost. |
| 8 | Integrated quarry analog demonstration | Combines mapping, beacons, tether, excavation and recovery. |
| 9 | Orbital relay/tug digital mission analysis | Sizes coverage and propulsion before spacecraft design. |
| 10 | Lunar pathfinder proposal | Only after the Earth evidence package is coherent. |

The first program should be judged by the quality of its measured data and failure handling, not by how closely a prototype resembles a final lunar machine. A small instrumented mechanism can remove more uncertainty than a large visual demonstrator.

[image1]: assets/image1.png

[image2]: assets/image2.png

[image3]: assets/image3.png

[image4]: assets/image4.png

[image5]: assets/image5.png

[image6]: assets/image6.png

[image7]: assets/image7.png

[image8]: assets/image8.png

[image9]: assets/image9.png

[image10]: assets/image10.png

[image11]: assets/image1.png

[image12]: assets/image12.png

[image13]: assets/image13.png

[image14]: assets/image14.png

[image15]: assets/image15.png