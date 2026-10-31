# LITHOS / SAMOREPLIKA

## *Earth development program for modular plastic robot kits before the Moon*

**From a home-made part to a verified field upgrade**

![][image1]

**Concept owner: Robert Petrušić**  
**Technical planning version 0.1 \- 4 August 2026**  
**Scope: game platform, home fabrication, modular robots, lawful field testing, abandoned mines and partial functional self-expansion.**

| Core definition<br>This is not a claim of complete self-replication. The first credible target is functional self-expansion: the system designs, fabricates, verifies and installs an increasing share of non-critical plastic parts, while motors, batteries, bearings, sensors and control electronics continue to be supplied from outside. |
| :---- |

# **1\. What should be built first**

**The first product is not a lunar mining robot. The first product is a closed development loop that converts a real field problem into a verified physical improvement. The minimum loop is: map the test area, define the task, design one replaceable part, make it at home, verify it on the bench, reproduce it under controlled conditions, install it on the robot, run a field test and measure whether performance improved.**

| Element | First practical version | Purpose |
| :---- | :---- | :---- |
| LITHOS game | Web or desktop interface with a voxel map, missions, part library and test results. | Turns real engineering into visible progress and preserves version history. |
| Plastic robot kit | One lightweight scout and one small cargo/tool rover with common interfaces. | Allows upgrades without redesigning the entire machine. |
| Home production | FDM printing of guards, brackets, wheel elements, cable guides and lightweight structural modules. | Enables distributed participation and rapid iteration. |
| Test arena | Enclosed sand-and-stone course with slopes, rubble, a dark tunnel and known hidden objects. | Provides repeatable tests before deployment to a real site. |
| Outdoor site | Authorized quarry, waste-rock area or surface industrial site before an abandoned mine. | Adds real dust, range, terrain and logistics at lower risk. |
| Mine pilot | Robot-only work at the entrance and within an engineer-inspected section of an abandoned mine. | Tests the system in its target environment without using people as test instruments. |

# **2\. Two possible architectures**

## **A. Distributed network of home kits**

* Participants download locked CAD templates, make parts at home and perform a defined test.  
* Only parts with a complete record of material, settings and results may be taken to the field site.  
* The central site maintains approved versions and installs them on standardized robotic platforms.  
* Advantage: a large number of attempts and rapid public participation.  
* Weakness: inconsistent printer, material and measurement quality.

## **B. On-site microfactory**

* Participants design remotely, but all field parts are produced on a controlled printer farm near the site.  
* Material, drying, orientation, dimensional inspection and batch marking are standardized.  
* Advantage: more reliable parts and simpler qualification.  
* Weakness: a larger initial burden on the central organization and less immediacy for home users.

| Recommended start: controlled hybrid<br>Home printing is used for prototypes, fit checks and early experiments. Every part that enters a real mine is reproduced on a controlled printer under a locked procedure. This retains the game and broad participation without treating an attractive home print as a field-qualified component. |
| :---- |

# **3\. The first robot family**

Do not begin by building ten machines. Start with two mobile robots and one fixed access node. Every interface, cable and safety state must be documented before new classes are added.

| Designation / name | Role | Initial configuration | First missions |
| :---- | :---- | :---- | :---- |
| P-01 Plastic Pioneer | Light scout and cable/sensor carrier. | Four-wheel or compact tracked base; printed body panels; metal motor mounts; sealed electronics cassette. | Route mapping, marker placement, crack inspection, camera carriage and light tether towing. |
| L-100 Scarab Lite | Slow tool rover and traction-test platform. | Rugged tracks with front/rear flippers; standard tool plate; replaceable printed guards. | Moving loose material, testing wheels/tracks, scraping and sampling. |
| G-01 LITHOS Gateway | Power, communications, data logging and emergency stop. | Fixed protected enclosure with radio, local computer, cameras, power supply and wired safety circuit. | Record every test, enforce geofencing, perform local stopping and store maps. |

## **3.1 What may be plastic in the first version**

* External body panels, guards, covers and replaceable wear skids.  
* Sensor brackets, camera housings, cable guides and connector guards.  
* Battery and electronics trays retained by metal pins or straps.  
* Experimental wheel and track elements whose failure cannot release a heavy load.  
* Low-load tool adapters, clearly separated from cutting and impact mechanisms.  
* Standard cargo boxes and lightweight sample containers.

## **3.2 What should not be printed as a critical field part**

* Primary lifting points, highly loaded shafts, pressure vessels, battery cells and fire barriers.  
* High-speed gears, heavily loaded bearings and safety brakes.  
* Load-bearing parts whose failure could trap a person or release a suspended load.  
* Parts intended for explosive atmospheres without independent certification of the complete assembly.

# **4\. The LITHOS game: a real engineering loop**

The game must reward demonstrated physical improvement, not an attractive render or an unsupported claim. A participant must see the same object in four linked forms: the real robot, its digital twin, the replaceable part and the test history.

**1\. Survey: the robot or operator uploads a terrain scan, failure record or work request.**

**2\. Mission generation: the system converts the problem into a constrained task, such as reducing wheel sinkage or protecting a camera from dust.**

**3\. Design: the player changes only the permitted design zone while critical volumes and interfaces remain locked.**

**4\. Automated check: dimensions, mass, part collisions, fastener access and basic printability are checked.**

**5\. Home coupon: a small material specimen or interface gauge is produced before the full part.**

**6\. Home prototype: the part is fabricated and tested according to the mission card.**

**7\. Evidence: mass, measurements, print settings, photographs and the failure description are uploaded.**

**8\. Controlled fabrication: the accepted version is reproduced at the site.**

**9\. Installation: an authorized technician or service robot installs the part according to the procedure.**

**10\. Field test: the robot completes a predefined route while the Gateway records results and faults.**

**11\. Status: the part is rejected, revised, approved for limited use or qualified for a defined operating envelope.**

**12\. Progression: successful parts unlock harder tasks and broader design authority.**

![][image2]

## **4.1 Player progression**

| Level | Player authority | Physical consequence |
| :---- | :---- | :---- |
| 0 \- Observer | Reviews maps, watches tests and flags possible problems. | No machine control or part approval. |
| 1 \- Modifier | Changes protective and cosmetic parts within locked interfaces. | Home prototypes only. |
| 2 \- Builder | Designs low-load functional parts and completes test cards. | Part may proceed to controlled on-site fabrication. |
| 3 \- Field designer | Changes traction, cable, sensor and cargo elements within defined limits. | Limited field test after engineering review. |
| 4 \- System designer | Proposes new interfaces and robotic modules. | Requires simulation, independent review and staged verification. |
| 5 \- Mission architect | Builds linked tasks for multiple robots and the microfactory. | Never bypasses the local safety controller. |

# **5\. Part design and release system**

Every physical part receives a permanent identity. A file name is not enough. The system must know who designed it, which machine and material produced it, where it was installed, how many cycles it survived and why it failed.

| Required record | Example |
| :---- | :---- |
| Part ID | P01-CAM-GUARD-003-R2 |
| Robot and interface | Plastic Pioneer / front sensor rail / interface v1 |
| Function | Protect the camera from a direct rock strike without blocking the field of view. |
| Material and process | Polymer type, nozzle, layer height, orientation, infill, drying and post-processing. |
| Mass and dimensions | Measured after fabrication, not copied from CAD. |
| Operating envelope | Maximum speed, slope, temperature, impact, load and mission duration. |
| Installation procedure | Tools, fasteners, torque, retention, cable routing and inspection points. |
| Status | Experimental / limited field use / qualified / withdrawn. |
| Failure record | Crack, deformation, wear, thermal damage, dust ingress and recovery action. |

## **5.1 Path from home to the field site**

**1\. Download the exact interface template and keep-out volume.**

**2\. Change one main function per revision; do not redesign the entire robot to solve a local problem.**

**3\. Print an interface gauge and a material coupon.**

**4\. Print the prototype and record the complete fabrication recipe.**

**5\. Perform fit, static-load and repeated-cycle tests at home.**

**6\. Upload the evidence; the part remains experimental until reviewed.**

**7\. Reproduce the accepted version on a controlled printer near the site.**

**8\. Measure the part and physically mark it with its ID and revision.**

**9\. Install it according to the procedure and photograph the completed assembly.**

**10\. Run a limited field mission and inspect the part immediately afterward.**

**11\. Publish failures. A hidden failure destroys the value of the system.**

# **6\. Functional self-expansion scale**

| Stage | What the system produces | What still comes from outside | Proof |
| :---- | :---- | :---- | :---- |
| S0 \- Repairable kit | Replaceable printed panels, brackets and guards. | All mechanics, electronics and energy storage. | Ten replacements without damage to the base interface. |
| S1 \- Distributed parts | Home-designed low-load parts reproduced at the site. | Controlled material, motors, sensors, bearings and fasteners. | The same revision from multiple printers remains within tolerance. |
| S2 \- Local plastic feedstock | Selected parts made from locally recycled and tested polymer. | Precision assemblies and electronics. | Material-batch testing and cycle comparison with virgin material. |
| S3 \- Robot-assisted production | Robots load material, collect parts and take them to inspection. | Printer, supervision and critical tools. | Repeated human-free cycles with safe recovery from faults. |
| S4 \- Robot-assisted assembly | One robot holds the part while another robot or fixture installs it. | Human approval and complex servicing. | Correct installation, verification and retreat after poor fit. |
| S5 \- Fleet growth | The site makes enough non-critical structure for an additional robot around imported precision modules. | Motors, cells, computers, bearings and certified safety assemblies. | A second robot performs a mission with most non-critical structure produced locally. |

| Do not use the term 'self-replicating robot' in the early stages<br>The accurate term is functional self-expansion. A system that prints a body but imports every motor, bearing, cell and processor is not a complete self-replicator. It is still highly valuable: it reduces logistics, accelerates repair and converts local material into useful structure. |
| :---- |

# **7\. Test sequence before an abandoned mine**

| Gate | Location | Activities | Pass condition |
| :---- | :---- | :---- | :---- |
| T0 \- Bench | Home / workshop | Fit, measurements, static loading, cable movement and electrical protection. | No part collisions; documented measurements; safe failure mode. |
| T1 \- Enclosed arena | Sand and rubble | Traction, slope, obstacles, darkness, dust, communication loss and recovery. | Repeatable mission and safe stopping after deliberate faults. |
| T2 \- Controlled outdoor site | Private site, quarry or industrial surface area | Range, weather, real dust, communication shadowing and logistics. | Robot returns or is recovered without exposing people to unstable terrain. |
| T3 \- Mine entrance | Authorized abandoned mine | Remote visual survey, gases, loose rock and radio communication. | No entry beyond the inspected boundary; reliable return and recovery. |
| T4 \- Robot-only underground | Engineer-inspected route | Mapping, relays, sampling, cables and tool testing. | Local controller stops on hazard; complete map and recovery route. |
| T5 \- Repeated operation | Same controlled mine section | Maintenance intervals, part replacement, contamination and production tasks. | Known service life, known spare consumption and no unresolved critical failure. |

## **7.1 Safety boundary**

* An abandoned mine is not entered merely because a robot can enter it. Ownership, structural stability, atmosphere, access and the recovery plan must be resolved before testing.  
* The first mine campaign is robot-only. People remain outside the hazard zone.  
* Explosive blasting is outside the first program. Initial work consists of mapping, moving loose material, scraping, low-energy drilling and sampling.  
* For the first underground tests, use a physical safety tether or independent recovery line even when radio communication is available.  
* The robot must stop locally after loss of communication; remote players never receive unrestricted direct control of hazardous tools.  
* Every test has a maximum duration, energy reserve, return point and recovery procedure.

# **8\. Site installation sequence**

**1\. Obtain written approval from the site owner and define the test boundary.**

**2\. Complete an external engineering and safety survey before the robots arrive.**

**3\. Install the G-01 Gateway outside the hazard zone with independent power, data recording and emergency stop.**

**4\. Install the first wired camera and basic environmental sensors at the entrance.**

**5\. Send Plastic Pioneer in on a short safety tether and verify recovery after complete radio loss.**

**6\. Build the first digital twin from cameras and ranging sensors and clearly mark low-confidence zones.**

**7\. Install passive route markers and the first relay node.**

**8\. Send Scarab Lite only after the route and recovery corridor have been confirmed.**

**9\. Install only one major new upgrade per mission so its effect can be measured.**

**10\. Inspect the robot in a dirty service zone before returning it to the clean workshop.**

**11\. Isolate, photograph and identify failed parts before repair.**

**12\. After every deployment, update the map, mission status and part record.**

# **9\. First game missions**

| Mission | Design task | Measured result |
| :---- | :---- | :---- |
| M01 \- Camera guard | Protect the camera without reducing the useful field of view. | Impact survived, dust on lens, image obstruction and mass. |
| M02 \- Cable guide | Prevent the safety tether from snagging while reversing. | Number of snags, bend radius and percentage of completed returns. |
| M03 \- Soft-ground element | Reduce wheel or track sinkage. | Sink depth, slip, energy per metre and wear. |
| M04 \- Sample box | Carry and release a specified mass without loss or contamination. | Retained mass, latch reliability and installation time. |
| M05 \- Relay mount | Place a small relay or visual marker at a specified point. | Position error, stability and communication improvement. |
| M06 \- Service tray | Allow rapid electronics removal without exposing connectors to dust. | Removal time, connector cleanliness and cycle count. |
| M07 \- Scraper guard | Prevent a rock from blocking the tool interface. | Number of blockages, material moved and damage after repeated use. |
| M08 \- Recovery hook | Recover a disabled robot without human entry. | Capture success, towing force and secondary damage. |

# **10\. The first 90 days**

![][image3]

| Period | Concrete result | Exit condition |
| :---- | :---- | :---- |
| Weeks 1-2 | Lock common interfaces, part IDs, safety states and the first eight missions. | A part can be designed without changing protected chassis geometry. |
| Weeks 2-4 | Build the LITHOS map viewer, mission cards, revision system and test database. | One digital mission moves from problem definition to recorded result. |
| Weeks 3-6 | Build P-01, Scarab Lite and G-01 plus the first home-print package. | Both robots move slowly, stop safely and accept replaceable modules. |
| Weeks 5-8 | Build an enclosed arena and conduct deliberate fault tests. | Communication loss, blocked drive and low battery produce defined safe states. |
| Weeks 7-10 | Close at least three design-fabricate-install-test loops. | A measurable comparison exists between the original and new part. |
| Weeks 9-12 | Move to an authorized outdoor industrial site or quarry. | Communication, recovery, dust and servicing remain controlled. |
| After day 90 | Prepare a campaign at the entrance of an abandoned mine. | Permission, engineering survey, gas monitoring, recovery and emergency plan are resolved. |

# **11\. What counts as success**

* A new participant can understand the interface and submit a valid low-risk part without private verbal instruction.  
* The same approved part can be produced on two printers and still fit correctly.  
* At least one field failure is safely recorded, explained and converted into a better revision.  
* A robot can lose communication and enter a safe state without dependence on a remote game server.  
* A disabled robot can be recovered without a person entering the hazard zone.  
* Part life, material batch, printer, installation and mission remain traceable.  
* The system produces an additional useful robot or major module with most non-critical structure made locally around imported precision assemblies.  
* The field program produces measurable data that directly improves Genesis/LITHOS and later lunar machines.

## **11.1 Stop conditions**

* Unknown gas, water, collapse, rock movement or loss of the recovery route.  
* Damaged battery, overheating, smoke, uncontrolled charging or exposed conductors.  
* Repeated communication loss without reliable local stopping and physical recovery.  
* A part cannot be linked to its material, print settings or installation record.  
* Pressure to continue because the game, deadline or audience expects a result.  
* A request to bypass the site owner, safety review or local robot controller.

# **12\. Immediate next actions**

**1\. Name the Earth program LITHOS / SAMOREPLIKA and define it as functional self-expansion, not complete replication.**

**2\. Lock the first configuration: Plastic Pioneer, Scarab Lite and Gateway.**

**3\. Select one universal mechanical interface: a flat tool plate with a fixed hole grid, locating features and a protected connector zone.**

**4\. Write missions M01-M08 before detailed robot design.**

**5\. Build an approximately one-square-metre test field and a short dark tunnel box.**

**6\. Create a database of IDs, revisions, materials, printers and tests.**

**7\. Limit the first public CAD task to a camera guard and cable guide.**

**8\. Require controlled reprinting before installation at a real field site.**

**9\. Close three complete design loops before seeking a mine.**

**10\. Use an authorized quarry or surface industrial area as the first outdoor site.**

**11\. Prepare the abandoned-mine package only after the outdoor system succeeds.**

| First decisive demonstration<br>A home user designs a new safety-tether guide. The part passes an interface gauge, is reproduced at the site, installed on Plastic Pioneer, reduces snagging on a repeatable rubble-and-tunnel route, survives the specified number of cycles, and both successful and failed data are published. That single closed loop is more valuable than a large unverified presentation of a 'self-replicating mine'. |
| :---- |

# **Appendix A \- Minimum mission card**

| Field | Required content |
| :---- | :---- |
| Problem | One measurable field problem and the baseline result. |
| Permitted interface | Exact mounting geometry and protected keep-out volume. |
| Design constraints | Mass, dimensions, material, fasteners, cable clearance and failure mode. |
| Home test | Steps, tools, load, cycle count and mandatory evidence. |
| Field test | Route, speed, duration, hazard boundary, stop criteria and recovery. |
| Metric | One primary and no more than three secondary metrics. |
| Acceptance | Numerical pass, limited-use or rejection condition. |
| Publication | CAD, revision, print recipe, measurements, photographs and failures. |

# **Appendix B \- Core engineering rules**

* Common interfaces, specialized machines.  
* Low speed and good measurement before high power.  
* A local safe state independent of the cloud and game platform.  
* Change only one variable per test whenever possible.  
* Controlled reproduction of every field part.  
* During development, only robots enter the mine.  
* Published failures are a mandatory game resource.  
* Partial local production remains valuable even when precision components are imported.

[image1]: assets/image1.png

[image2]: assets/image1.png

[image3]: assets/image3.png