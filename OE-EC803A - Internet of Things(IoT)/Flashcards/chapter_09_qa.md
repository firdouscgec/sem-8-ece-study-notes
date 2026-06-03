# Flashcards: Unit IX: Moving to Manufacture

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit IX.

---

### 🎴 Card 1:
Q1. List the seven steps in the PCB design-to-manufacturing pipeline in order.  
**Ans.**  
1. Schematic Capture.  
2. PCB Layout (Board Design).  
3. Design Rule Check (DRC).  
4. Gerber File Generation.  
5. PCB Fabrication.  
6. Component Assembly (SMT/THT).  
7. Testing and Quality Assurance.

---

### 🎴 Card 2:
Q2. What is a Gerber file and why is it important?  
**Ans.** A Gerber file is the universal, industry-standard format for PCB manufacturing. A complete set includes a separate file for each copper layer, solder mask layer, silkscreen layer, and drill file. It is the deliverable sent to the fabrication house.

---

### 🎴 Card 3:
Q3. Differentiate between SMT and Through-Hole assembly techniques.  
**Ans.**  
* **SMT (Surface Mount):** Pick-and-place machine positions tiny components on solder paste pads; reflow oven melts and bonds them. Fast and automated.  
* **Through-Hole (THT):** Larger components are inserted through drilled holes and soldered via wave soldering or manual soldering. Stronger mechanical bonds.

---

### 🎴 Card 4:
Q4. Name the four testing methods used after PCB assembly.  
**Ans.**  
1. **AOI** (Automated Optical Inspection) — camera scan for defects.  
2. **ICT** (In-Circuit Testing) — electrical probe for continuity.  
3. **Functional Test** — power on, flash firmware, verify all systems.  
4. **Burn-In Test** — sustained stress operation for 24–72 hours.

---

### 🎴 Card 5:
Q5. What are the five categories of testing an IoT system must undergo before mass manufacture?  
**Ans.**  
1. Hardware Testing (ESD, thermal, drop/vibration, EMI).  
2. Software/Firmware Testing (unit, integration, regression, OTA).  
3. Connectivity Testing (Wi-Fi range, BLE pairing, MQTT QoS).  
4. Security Testing (pen testing, firmware analysis, TLS validation).  
5. User Acceptance Testing (onboarding, mobile app UX, field trials).

---

### 🎴 Card 6:
Q6. Explain ESD testing and thermal cycling in the context of IoT hardware validation.  
**Ans.**  
* **ESD Testing:** Subjects the device to high-voltage static discharge pulses (IEC 61000-4-2) to ensure survival during real-world handling.  
* **Thermal Cycling:** Repeatedly cycles between extreme temperatures (e.g., -20°C to +70°C) to test solder joint reliability and component tolerance.

---

### 🎴 Card 7:
Q7. What is the purpose of firmware binary analysis in IoT security testing?  
**Ans.** The firmware binary is extracted and decompiled to check for hardcoded credentials, API keys, unencrypted sensitive data, and insecure coding patterns that an attacker could exploit.

---

### 🎴 Card 8:
Q8. What is injection molding and what are its key advantages and disadvantages for IoT enclosures?  
**Ans.** Molten plastic is injected into a precision steel mold at high pressure; after cooling, the part is ejected.  
* *Advantage:* Produces thousands of identical, smooth parts per day at very low per-unit cost.  
* *Disadvantage:* Extremely high upfront mold tooling cost ($10K–$100K+); any design change requires a new mold.

---

### 🎴 Card 9:
Q9. Name four regulatory certifications required before selling an IoT product commercially.  
**Ans.**  
1. **FCC Part 15** (US — RF emissions limits).  
2. **CE Marking** (EU — health, safety, environment conformity).  
3. **RoHS** (EU/Global — restriction of hazardous substances).  
4. **UL / IEC 62368-1** (Global — electrical safety).

---

### 🎴 Card 10:
Q10. What are the four key aspects of scaling up software when moving from prototype to mass production?  
**Ans.**  
1. Auto-scaling cloud infrastructure (AWS ECS, Kubernetes).  
2. Centralized device fleet management and bulk OTA updates.  
3. Distributed NoSQL/time-series databases for high-velocity data.  
4. CI/CD pipelines for automated firmware and cloud releases.
