# OE-EC803A: Internet of Things (IoT) - One-Liners

---

# Chapter 1: Introduction to IoT

1. Internet of Things (IoT) definition → Global network of self-configuring physical and virtual objects.
2. World Wide Web vs. IoT core distinction → WWW connects humans; IoT connects physical and virtual devices.
3. Enchanted Object definition → Everyday physical object enhanced with ambient connectivity and sensors.
4. Localized network focused purely on data collection → Wireless Sensor Network (WSN).
5. Traditional Machine-to-Machine (M2M) communication style → Closed, point-to-point, isolated, and hardware-centric.
6. Direct local device communication model → Device-to-Device (D2D).
7. Direct internet platform connection model → Device-to-Cloud (D2C).
8. IoT Gateway primary function → Performs protocol translation and data routing.
9. ETSI M2M architecture interfaces → dIa (device-app), mIa (network-app), mId (M2M-device).
10. Generic M2M system solution layers → M2M Area Network, Communication Network, M2M Applications.
11. Four stages of IoT information value chain → Sense, Transmit, Store/Analyze, Decide/Act.
12. OGC API standard for querying sensor observations → SOS (Sensor Observation Service).
13. OGC XML schema for sensor parameters → SensorML (Sensor Model Language).
14. Category used for business-to-consumer processes → Personal IoT.
15. Category used by citizens to benefit smart cities → Community IoT.
16. Automatic device communication without human intervention → Machine-to-Machine (M2M).
17. Network of uniquely identifiable embedded computing devices → Internet of Things (IoT).
18. Core components providing physical world awareness → Sensors.
19. Vital elements required by house key computers → Data and services.
20. M2M device domain alternative name → M2M Area Network.
21. Industrial IoT (IIoT) priority focus → Zero-downtime, safety, and mission-critical reliability.

# Chapter 2: Design Principles for Connected Devices

1. Calm Technology primary goal → Blends into the periphery, reducing cognitive fatigue.
2. Calm Technology design rules → Peripheral attention, seamless shift, presence, reach, attention limits.
3. Ambient Technology definition → Devices displaying status information via subtle environmental cues.
4. Ambient Orb designer → David Rose.
5. Ambient Orb feedback mechanism → Frosted sphere changing color using internal LEDs.
6. Ambient Orb main limitation → Low information density (conveys status, not text).
7. Magic as Metaphor concept → Using mythical archetypes to explain wireless operations.
8. Gesture-controlled magical controller device example → Kymera Magic Wand.
9. Critiques of Magic as Metaphor → Expectation mismatch, lack of debugging/error states.
10. Privacy design solution for local devices → Edge processing and data minimization.
11. Web Thinking for Connected Devices definition → Building IoT architectures using standardized HTTP/REST principles.
12. URI role in Web Thinking → Unique address identifier for every physical sensor/actuator.
13. REST command to read sensor state → GET.
14. REST command to trigger actuator action → POST.
15. Physical Mashup definition → Linking different physical devices using standard web APIs.
16. Affordance definition → Physical properties of an object suggesting its usage.
17. Clash of Affordances in IoT → Traditional appearance hiding invisible digital sensor interfaces.
18. Visual signifiers resolving Clash of Affordances → LED rings or textured borders guiding interaction.
19. Graceful degradation design requirement → Device remains functional physically if internet or power fails.
20. Ambient device pulsing when rain is expected → Ambient Umbrella.

# Chapter 3: Internet Principles

1. BLE full form → Bluetooth Low Energy.
2. BLE GATT hierarchy data structures → Profiles, Services, and Characteristics.
3. Classic Bluetooth vs. BLE latency → Classic up to 6s; BLE under 3ms.
4. Address style permanent and manually configured → Static IP.
5. DHCP dynamic configuration handshake acronym → DORA.
6. DORA handshake steps → Discover, Offer, Request, Acknowledge.
7. TCP full form → Transmission Control Protocol.
8. UDP full form → User Datagram Protocol.
9. Reliable, connection-oriented transport protocol → TCP.
10. Fast, lightweight, connectionless transport protocol → UDP.
11. UDP minimum header size → 8 bytes.
12. TCP minimum header size → 20 bytes.
13. IPv6 address length in bits → 128 bits.
14. IPv4 address length in bits → 32 bits.
15. IPv6 feature for stateless autoconfiguration → SLAAC.
16. MAC address length in bits → 48 bits.
17. MAC address data link layer level → Layer 2 (Physical address).
18. MAC address manufacturer identifier first 24 bits → OUI (Organizationally Unique Identifier).
19. Logical endpoints routing network traffic in OS → Network Ports (16-bit).
20. HTTP message format style → ASCII text headers.
21. CoAP transport protocol and minimum header size → UDP; 4 bytes.
22. MQTT architecture model and minimum header size → Publish-Subscribe (Broker-based); 2 bytes.
23. Weightless protocol radio spectrum utilization → Sub-GHz TV White Space (TVWS).
24. Computing proximity closest to data source → Mist computing.
25. Proximity order of computing layers → Mist → Edge → Fog → Cloud.
26. Computing layer running on regional routers → Fog computing.
27. Layer connecting IoT devices with WAN → Network layer.
28. IoTA full form → Internet of Things Architecture.
29. Protocol linking all devices in the internet → TCP/IP.
30. Computing emphasizing proximity to end user → Fog computing.

# Chapter 4: Thinking About Prototyping

1. Prototyping sketching purpose → Fast, low-cost exploration of concepts.
2. Low fidelity prototype main benefit → High ease of creation and low initial cost.
3. High fidelity prototype main benefit → Evaluates real-time performance and user experience.
4. Sourcing model prioritizing IP protection and restricted designs → Closed Source.
5. Sourcing model bypassing royalty fees and accelerating development → Open Source.
6. MVP full form in startup prototyping → Minimum Viable Product.
7. Scale-up design challenge in prototyping → Transitioning from breadboards to mass-manufactured PCBs.
8. Prototyping board with breadboard friendly pins → Arduino Uno.
9. Community-driven hardware source code repository → GitHub.
10. Value of tapping into the community → Reusable libraries, fast debugging, and hardware templates.

# Chapter 5: Prototyping Physical Design

1. 3D printing technology style → Additive manufacturing.
2. Filament material standard for FDM 3D printing → PLA (Polylactic Acid) or ABS.
3. Laser cutting process style → Subtractive manufacturing.
4. Laser cutter material compatibility constraint → Dangerous fumes from PVC/plastics containing chlorine.
5. CNC milling definition → Computer-controlled rotating tool cutting block material.
6. Subtractive method for high-accuracy metal brackets → CNC milling.
7. Fast method for enclosure mockups → Laser cut cardboard or acrylic.
8. 3D printing technique using UV laser on resin → SLA (Stereolithography).
9. Recycling/repurposing in physical prototyping → Reusing existing enclosures or containers.
10. File format for 3D printing → STL (Stereolithography) or 3MF.

# Chapter 6: Prototyping Embedded Devices

1. Arduino processor architecture style → AVR/ARM 8-bit or 32-bit Microcontroller.
2. Raspberry Pi processor architecture style → ARM 64-bit Microprocessor.
3. Arduino boot speed characteristics → Instant boot.
4. Raspberry Pi boot time → 15 to 30 seconds.
5. Arduino standard RAM capacity → 2 KB SRAM (ATmega328P).
6. Raspberry Pi RAM capacity range → 1 GB to 8 GB LPDDR4.
7. GPIO full form → General Purpose Input Output.
8. I2C serial bus lines → SDA (Data) and SCL (Clock).
9. SPI serial bus lines → MOSI, MISO, SCLK, and CS (Chip Select).
10. UART serial bus lines → TX (Transmit) and RX (Receive).
11. Raspberry Pi GPIO logic voltage limit → 3.3V.
12. BeagleBone Black ADC resolution → 12-bit (7 analog input channels).
13. BeagleBone co-processors for deterministic real-time I/O → PRUs (Programmable Real-Time Units).
14. Electric Imp split coding architecture → Device code and Cloud code.
15. Electric Imp programming language → Squirrel.
16. Electric Imp vendor constraint → Closed vendor lock-in.
17. Smartphone prototyping advantage → Rich built-in sensors and wireless communication.
18. Plug Computer primary advantage → Always-on mains powered 24/7 server design.
19. Arduino programming language wrapper base → C/C++ wrapper.
20. PCI Express role in IoT gateways → Interconnecting high-speed Wi-Fi, Bluetooth, or cellular cards.
21. Ethernet 10/100M support connection target → Local Area Network (LAN).
22. More powerful model between Pi 2 and Pi 3 → Raspberry Pi 3.

# Chapter 7: Prototyping Online Components

1. API full form → Application Programming Interface.
2. REST API resource formats → JSON or XML.
3. API architecture consideration beyond tech → Security, access control, and authentication.
4. Protocol for real-time bidirectional web communications → WebSockets.
5. MQTT broker role in online components → Directs publisher messages to target subscribers.
6. Push notification protocol for mobile alerts → APNs (Apple) or FCM (Firebase).
7. Standard auth method for securing APIs → OAuth 2.0 / API Keys.
8. CORS full form in API development → Cross-Origin Resource Sharing.
9. HTTP code for resource not found → 404.
10. HTTP code for successful request → 200 OK.
11. Scope of API architecture beyond technical elements → Multi homing (mobile networks with dynamic membership).

# Chapter 8: Techniques for Writing Embedded Code

1. Primary risk of dynamic memory allocation in MCU → Heap fragmentation leading to crashes.
2. Dynamic memory allocation alternative → Static allocation of fixed-size buffers.
3. Blocking delay side effect → Halts CPU cycles, blocking event handlers.
4. Non-blocking delay implementation → State machines using `millis()` checks.
5. Battery life optimization technique using low power → CPU deep sleep modes.
6. Action to audit third-party libraries → Checking Flash and RAM consumption reports.
7. Serial print debugging drawback → Alters timing execution and consumes RAM/UART.
8. JTAG/SWD debugging advantage → Non-intrusive breakpoints and real-time register audit.
9. Reliability phase forwarding packets hop-by-hop → Message relaying.
10. Reliability phase tracking sequence counter gaps → Lost message detection.
11. Reliability phase asking for missing packets only → Selective recovery.
12. Reliability first step in WSN reliable transfer → Initialization.
13. CPU clock reduction scaling method → DVFS (Dynamic Voltage and Frequency Scaling).
14. Non-intrusive debugging probe connector → JTAG or SWD.
15. Best storage for persistent configuration settings → EEPROM or Flash.

# Chapter 9: Prototype to Reality (Business Models & Manufacturing)

1. Business Model Canvas creator → Alexander Osterwalder.
2. Number of building blocks in BMC → 9.
3. BMC block defining product value to customers → Value Proposition.
4. Lean Startup build-measure-learn cycle first stage → Build a Minimum Viable Product (MVP).
5. Core decision after build-measure-learn evaluation → Pivot or Persevere.
6. Startup funding using small public contributions → Crowdfunding (Kickstarter).
7. PCB full form → Printed Circuit Board.
8. First step in PCB design workflow → Creating the schematic diagram.
9. Manufacturing technique for high-volume plastic enclosures → Injection molding.
10. Certification required for electronic sales in Europe → CE.
11. Certification required for radio devices in USA → FCC.
12. Startup funding from high-net-worth individuals → Angel Investment.

# Chapter 10: Ethics & Smart Cities

1. Smart City definition → Urban area optimizing utility services using IoT data.
2. Smart Lighting energy savings percentage → Up to 80% using ambient LDR sensors.
3. Smart Waste sensor type → Ultrasonic distance sensor.
4. Smart waste routing optimization → Skips empty bins, planning routes dynamically.
5. V2X full form in Intelligent Transportation Systems → Vehicle-to-Everything.
6. Priority route technique for emergency vehicles → Emergency traffic preemption.
7. Smart City baseline data ingestion layer → Integrated Information Provider.
8. Smart City command and control center → Management Center.
9. Smart City citizen interface touchpoint layer → Mobile Unified Service.
10. Smart City GIS analytics layer → Urban Application Platform.
11. Passive constant monitoring of public without consent → Surveillance Creep.
12. Deducing personal habits from benign appliance logs → Data Profiling.
13. Remote bricking definition → Disabling device functionality remotely by vendor.
14. Botnet created by compromising default password IoT → Mirai botnet.
15. Mitigating vendor lock-in using standardized APIs → Open standards adoption (Matter).
16. Stake level in physical security → High.
17. Reliable bidirectional signaling challenge category → Signaling.
18. Availability of video/data hosting → Security system.
19. IoT service manageability feature → Simple and fast installation.
20. Ethics pillar for modular/recyclable materials → Circular design / environmental impact.
