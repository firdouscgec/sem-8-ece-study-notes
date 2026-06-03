# Flashcards: Unit X: Ethics & Smart Cities

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and ethical principles of Unit X.

---

### 🎴 Card 1:
Q1. Define a Smart City and explain the role IoT plays in its implementation.  
**Ans.** A Smart City is an urban area that uses ICT and IoT sensors to gather data, manage resources, and run municipal utilities efficiently. IoT nodes act as the sensory network (detecting traffic, light, and trash fill-levels) to optimize power, logistics, and service delivery.

---

### 🎴 Card 2:
Q2. What is the working principle and benefits of Smart Lighting in a Smart City?  
**Ans.**  
* **Working Principle:** Streetlights use Light Dependent Resistors (LDRs) and motion sensors (PIR) to adjust light intensity based on time, ambient light, and activity.  
* **Benefits:** Saves up to 80% energy during low-traffic periods, and automatically reports bulb failures to a central maintenance panel.

---

### 🎴 Card 3:
Q3. Explain how dynamic signal control and emergency preemption function in smart traffic management.  
**Ans.**  
* **Dynamic Signal Control:** Cameras/sensors monitor traffic volume at intersections and adjust signal phases in real-time to clear actual queues rather than using rigid timers.  
* **Emergency Preemption:** Traffic signals track approaching emergency vehicles (ambulances/fire engines) via GPS and automatically switch to green to provide priority routing.

---

### 🎴 Card 4:
Q4. Describe the working principle of ultrasonic waste tracking in smart cities.  
**Ans.** Bins are fitted with ultrasonic sensors on their inner lids. The sensor measures the distance to the trash surface to track the fill level and sends this data via cellular modules (NB-IoT) to central routing software. This allows municipal trucks to skip empty bins and optimize collection routes.

---

### 🎴 Card 5:
Q5. What is Vehicle-to-Everything (V2X) communication in Intelligent Transportation Systems (ITS)?  
**Ans.** V2X communication is the transfer of information between a vehicle and any entity that may affect the vehicle (including other vehicles V2V, and roadside infrastructure V2I). It enables real-time public transit tracking, smart parking spot reservation, and vehicle collision warnings.

---

### 🎴 Card 6:
Q6. List the four main pillars of ethical challenges in IoT.  
**Ans.**  
1. **Privacy** (surveillance creep, data profiling, consent ambiguity).  
2. **Control & Ownership** (vendor lock-in, remote bricking, data custody).  
3. **Security Vulnerabilities** (botnets, physical safety risk, unpatched firmware).  
4. **Environmental Impact** (e-waste, planned obsolescence, high scale energy use).

---

### 🎴 Card 7:
Q7. Differentiate between "surveillance creep" and "data profiling" in the context of IoT privacy.  
**Ans.**  
* **Surveillance Creep:** The passive, constant monitoring of individuals in private/public spaces by ambient sensors without active consent.  
* **Data Profiling:** Aggregating and analyzing multiple benign sensor data points (like appliance usage and TV logs) using machine learning to deduce highly personal schedules, habits, and details.

---

### 🎴 Card 8:
Q8. What is remote bricking and how does it relate to vendor lock-in?  
**Ans.** Remote bricking occurs when a vendor disables a device remotely or shuts down the cloud servers required for its operation, rendering functional hardware useless. This is a severe risk of vendor lock-in, where proprietary walled gardens prevent users from running their devices on open or alternative local platforms.

---

### 🎴 Card 9:
Q9. How do insecure consumer IoT devices lead to Mirai-class botnets?  
**Ans.** Millions of cheap IoT devices (IP cameras, baby monitors) are shipped with hardcoded default passwords and lack secure boot. Attackers scan the internet, compromise these devices using automated scripts, and recruit them into massive botnets to run Distributed Denial of Service (DDoS) attacks.

---

### 🎴 Card 10:
Q10. Name four mitigation strategies that address the ethical challenges of IoT.  
**Ans.**  
1. **Privacy by Design:** Local edge processing and data minimization.  
2. **Open Standards:** Matter/Zigbee open APIs to prevent vendor lock-in.  
3. **Security Lifecycle:** Unique default passwords and mandatory security updates.  
4. **Circular Design:** Modular builds with replaceable batteries and recycling programs.
