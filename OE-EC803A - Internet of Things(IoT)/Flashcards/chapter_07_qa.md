# Flashcards: Unit VII: Prototyping Online Components

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit VII.

---

### 🎴 Card 1:
Q1. What is an API in the context of IoT?  
**Ans.** An **API (Application Programming Interface)** is a set of defined rules and protocols allowing different software applications to communicate. In IoT, APIs bridge physical devices (sensors/actuators) and online services (cloud platforms, databases, third-party apps).

---

### 🎴 Card 2:
Q2. Distinguish between consuming an existing API and writing a new API for IoT.  
**Ans.**  
* **Consuming:** The device acts as a client, sending HTTP requests to a third-party cloud API to fetch/push data (e.g., querying OpenWeatherMap).  
* **Writing:** The device acts as a server, exposing its own RESTful endpoints so external apps can read sensors or control actuators (e.g., `GET /api/sensors/soil-moisture`).

---

### 🎴 Card 3:
Q3. Define the role of Cloud Computing in IoT and list its four primary functions.  
**Ans.** Cloud computing provides remote, scalable infrastructure for IoT. Four functions:  
1. **Data Storage** (unlimited scalable archives).  
2. **Data Processing & Analytics** (ML training, stream processing).  
3. **Device Management** (registration, OTA updates, device twins).  
4. **Application Hosting** (dashboards, mobile backends, notification services).

---

### 🎴 Card 4:
Q4. Explain the role of Cloud Computing in a Smart Grid architecture.  
**Ans.** Smart Meters transmit real-time consumption data to the cloud. The cloud performs demand forecasting, load balancing, and peak shaving. It sends control commands to grid substations and provides consumer-facing apps for real-time billing and usage alerts.

---

### 🎴 Card 5:
Q5. Name three advantages and three disadvantages of cloud computing in Smart Grids.  
**Ans.**  
* *Advantages:* Centralized processing of millions of meters, elastic scaling during peak demand, and long-term historical trend analysis.  
* *Disadvantages:* Latency too slow for protection relay decisions, granular data reveals private household behaviors, and WAN outages disconnect all meters.

---

### 🎴 Card 6:
Q6. Describe the four levels of Big Data Analytics in IoT.  
**Ans.**  
1. **Descriptive** ("What happened?") — Dashboards and summaries.  
2. **Diagnostic** ("Why did it happen?") — Root cause analysis.  
3. **Predictive** ("What will happen?") — ML forecasting.  
4. **Prescriptive** ("What should we do?") — Automated optimal actions.

---

### 🎴 Card 7:
Q7. Give a concrete IoT example for Predictive and Prescriptive analytics.  
**Ans.**  
* **Predictive:** A motor vibration model forecasts ball bearing failure in 14 days based on 6-month frequency patterns.  
* **Prescriptive:** The system auto-schedules a maintenance work order, reserves spare parts, and assigns a technician without human intervention.

---

### 🎴 Card 8:
Q8. What are Real-Time Reactions in IoT? Give an example.  
**Ans.** The ability of an IoT system to process an incoming event and trigger an immediate, automated response. **Example:** A motion sensor detects an intruder; within 200 ms the system triggers a siren, locks smart doors, turns on floodlights, and pushes a phone notification.

---

### 🎴 Card 9:
Q9. How do WebSockets differ from standard HTTP for IoT communication?  
**Ans.** HTTP is request-response only (client must poll). WebSockets upgrade a single TCP connection into a **persistent, full-duplex, bidirectional** channel where both client and server can push messages at any time without re-establishing a connection.

---

### 🎴 Card 10:
Q10. Compare HTTP Polling, WebSockets, and MQTT for real-time IoT.  
**Ans.**  
* **HTTP Polling:** High latency, client-initiated only, high overhead per request.  
* **WebSockets:** Very low latency, full-duplex bidirectional, ideal for browser dashboards.  
* **MQTT:** Low latency, broker-mediated pub/sub push, minimal 2-byte header, ideal for massive device networks.
