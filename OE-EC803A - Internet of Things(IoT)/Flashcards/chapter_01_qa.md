# Flashcards: Unit I: Introduction to IoT

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit I.

---

### 🎴 Card 1:
Q1. What is the Internet of Things (IoT)?  
**Ans.** A dynamic global network infrastructure with self-configuring capabilities based on standard and interoperable communication protocols, connecting physical and virtual "things" embedded with sensors, actuators, and connectivity.

---

### 🎴 Card 2:
Q2. What is the fundamental difference between the World Wide Web (WWW) and the Internet of Things (IoT)?  
**Ans.** The WWW connects **humans to information** (browser-based client-server requests), while the IoT connects **devices/things to other devices/things** (machine-to-machine data exchanges and actions).

---

### 🎴 Card 3:
Q3. Explain the concept of an "Enchanted Object" and give an example.  
**Ans.** A physical, everyday object enhanced with digital intelligence, sensors, and internet connectivity, providing information via subtle, ambient cues without changing its native physical form. **Example:** An umbrella handle that glows blue when rain is forecast.

---

### 🎴 Card 4:
Q4. Differentiate between a Wireless Sensor Network (WSN) and an IoT network.  
**Ans.** A WSN is a localized network of sensor nodes focused purely on data collection (sensing). An IoT network is a global network that integrates sensors, internet gateways, cloud analytics, and **actuators** to both sense and dynamically control/affect the physical world.

---

### 🎴 Card 5:
Q5. Compare Machine-to-Machine (M2M) communication and the Internet of Things (IoT) across scope and protocols.  
**Ans.** M2M is typically point-to-point, closed, isolated, and hardware-centric using legacy/cellular links. IoT is a global, open-standard, cloud-centric network using standard internet protocols (IP, TCP/IP, MQTT, CoAP) and web APIs.

---

### 🎴 Card 6:
Q6. Explain the four "flavors" (communication models) of IoT.  
**Ans.** 
1. **Device-to-Device (D2D):** Direct local link between devices (e.g. Bluetooth).
2. **Device-to-Cloud (D2C):** Direct IP connection to a cloud platform.
3. **Device-to-Gateway (D2G):** Local link to a gateway, which forwards data to the cloud.
4. **Back-End Data Sharing (C2C):** Cloud-to-cloud API connections for data sharing.

---

### 🎴 Card 7:
Q7. What are the key differences between traditional IoT and Industrial IoT (IIoT)?  
**Ans.** Traditional IoT is consumer-focused (convenience, moderate reliability, low safety risk). IIoT is industrial-focused (mission-critical operations, zero-downtime tolerance, extreme safety/security standards, high financial impact of failure).

---

### 🎴 Card 8:
Q8. Describe the role of a "Gateway" in an IoT network.  
**Ans.** An IoT Gateway acts as a bridge between local constrained devices and the wider internet. It performs protocol translation (e.g., Zigbee to IP), data aggregation, and local preprocessing (edge computing).

---

### 🎴 Card 9:
Q9. List the three interfaces defined in the ETSI M2M Functional Architecture.  
**Ans.** 
1. **dIa (Device-to-Application):** Connects device apps to local service capabilities.
2. **mIa (M2M-to-Application):** Connects network apps to network service capabilities.
3. **mId (M2M-to-Device):** Connects the device/gateway layer to the network service capability layer.

---

### 🎴 Card 10:
Q10. What are the three core functional layers of a Generic M2M System Solution?  
**Ans.** 
1. **M2M Area Network (Device Domain):** Local sensors, actuators, and local links.
2. **Communication Network (Network Domain):** Long-distance links (Cellular, WAN, satellite).
3. **M2M Applications (Application Domain):** Cloud backend and user applications.

---

### 🎴 Card 11:
Q11. List the four main stages of the Information-Driven Value Chain for IoT.  
**Ans.** **Sense** (sensors capture states) $\rightarrow$ **Transmit** (send data over IP) $\rightarrow$ **Store/Analyze** (databases and data processing) $\rightarrow$ **Decide/Act** (actuators perform control actions).

---

### 🎴 Card 12:
Q12. What are the SOS and SensorML standards in the OGC framework?  
**Ans.** **SOS (Sensor Observation Service)** is an API standard for querying real-time sensor observations. **SensorML (Sensor Model Language)** is an XML schema describing sensor system parameters and metadata.

---

### 🎴 Card 13:
Q13. Name four major challenges faced when implementing an IoT system.  
**Ans.** 
1. **Security & Privacy** (vulnerability of resource-constrained nodes).
2. **Interoperability** (communication barriers between vendors).
3. **Data Volume Management** (processing massive unstructured streams).
4. **Power constraints** (achieving long battery lives for remote nodes).

---

### 🎴 Card 14:
Q14. How does an IoT-oriented approach provide more value than M2M in a Health Band system?  
**Ans.** M2M only sends heart rate to a single monitor. IoT integrates the data with EMR databases, third-party fitness apps, local pharmacies, and runs predictive cloud algorithms to alert the user of anomalies via their phone.

---

### 🎴 Card 15:
Q15. Define and compare the four categories of IoT by scope: Personal, Group, Community, and Industrial IoT.  
**Ans.** 
1. **Personal IoT:** Consumer-focused B2C processes (e.g., smartwatches, home voice assistants).
2. **Group IoT:** Localized shared environments (e.g., connected office lights, smart classroom boards).
3. **Community IoT:** Municipal scale benefiting citizens (e.g., smart city air monitoring, bicycle sharing).
4. **Industrial IoT (IIoT):** Mission-critical business/factory systems with zero-downtime tolerance (e.g., turbine vibration monitors, smart grid stations).