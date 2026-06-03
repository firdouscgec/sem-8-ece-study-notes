# Flashcards: Unit III: Internet Principles for Connected Devices

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit III.

---

### 🎴 Card 1:
Q1. Define Bluetooth Low Energy (BLE) and name its four core features.  
**Ans.** **BLE** is a wireless personal area network technology designed for low-power, short-range IoT communication.  
*Features:* Ultra-low power consumption (runs on coin cells), fast connection setup (<3 ms), Advertising Mode (beacon broadcasting), and GATT data hierarchy (Profiles/Services/Characteristics).

---

### 🎴 Card 2:
Q2. What are the key differences between Classic Bluetooth and Bluetooth Low Energy (BLE)?  
**Ans.**  
* **Classic Bluetooth:** High-throughput continuous data stream, high power consumption (~1W), latency up to 6s, max 7 slaves.  
* **BLE:** Low duty cycle, ultra-low power consumption (~0.01W), latency <3ms, unlimited mesh topology nodes.

---

### 🎴 Card 3:
Q3. Differentiate between Static and Dynamic IP addressing in IoT.  
**Ans.** **Static IP** is manually configured and permanent; ideal for central network gateways or brokers. **Dynamic IP** is automatically assigned for a temporary lease duration by a DHCP server; ideal for edge sensor nodes.

---

### 🎴 Card 4:
Q4. Explain the DORA handshake process in DHCP.  
**Ans.** **DORA** stands for:
1. **D**iscover: Client broadcasts to find a DHCP server.
2. **O**ffer: Server proposes an IP address and network config.
3. **R**equest: Client requests to lease the proposed IP.
4. **A**cknowledge (ACK): Server commits the lease to the client.

---

### 🎴 Card 5:
Q5. Provide a brief example of DHCP dynamically configuring an IoT node on boot.  
**Ans.** A smart thermostat boots up, broadcasts a `DHCPDISCOVER` packet over Wi-Fi. The home router replies with a `DHCPOFFER` proposing `192.168.1.15`. The thermostat accepts via `DHCPREQUEST`, and the router registers the thermostat's MAC address and confirms with a `DHCPACK`.

---

### 🎴 Card 6:
Q6. Differentiate between TCP and UDP in terms of connection style, reliability, header overhead, and speed.  
**Ans.**  
* **TCP:** Connection-oriented (3-way handshake), reliable (ACKs/retransmissions), 20-byte min header, slower speed.  
* **UDP:** Connectionless, best-effort (no delivery guarantee), 8-byte header, faster speed (low latency).

---

### 🎴 Card 7:
Q7. Why is UDP preferred over TCP in resource-constrained IoT settings?  
**Ans.**  
1. **Power Conservation:** No connection handshakes/teardowns, saving radio uptime battery.  
2. **Low Overhead:** 8-byte header (vs TCP's 20-byte) saves precious network bandwidth.  
3. **Real-time Performance:** Dropped packets are ignored instead of causing lag via retransmission queues.

---

### 🎴 Card 8:
Q8. List five primary benefits of using IPv6 instead of IPv4 in IoT networks.  
**Ans.**  
1. Massive address space ($3.4 \times 10^{38}$ IPs).  
2. SLAAC (Stateless Address Autoconfiguration).  
3. Simplified, fixed-length 40-byte headers.  
4. Native IPsec security.  
5. Optimized multicasting (replaces wasteful broadcasts).

---

### 🎴 Card 9:
Q9. What is the length and structure of an IPv6 address?  
**Ans.**  
* **Length:** 128 bits (16 bytes).  
* **Structure:** Written as 8 groups of 4 hexadecimal digits separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`). It contains a 64-bit Network Prefix and a 64-bit Interface Identifier.

---

### 🎴 Card 10:
Q10. What is a MAC address, its standard length, and its role in a network?  
**Ans.** A **MAC address** is a unique physical hardware identifier assigned to a network interface controller (NIC) by the manufacturer. It is **48 bits** (6 bytes) long, operates at the Data Link Layer (Layer 2), and uniquely identifies a physical node on a local network segment.

---

### 🎴 Card 11:
Q11. Describe the internal bit structure of a 48-bit MAC address.  
**Ans.** It is split into two halves:
1. **OUI (Organizationally Unique Identifier):** First 24 bits, identifying the manufacturer (assigned by IEEE). Contains U/L (Universal/Local) and I/G (Individual/Group) bits.  
2. **NIC Specific ID:** Last 24 bits, uniquely assigned to the individual chip by the manufacturer.

---

### 🎴 Card 12:
Q12. What are network ports, and what are their standard classifications?  
**Ans.** Ports are **16-bit logical endpoints** (values 0–65535) in the OS that route incoming network traffic to specific software processes.  
*Classifications:* Well-Known Ports (0–1023), Registered Ports (1024–49151), and Dynamic/Private Ports (49152–65535).

---

### 🎴 Card 13:
Q13. Explain the working principle, strengths, and limitations of HTTP in IoT.  
**Ans.**  
* **Principle:** Synchronous Request-Response protocol over TCP.  
* **Strengths:** Ubiquitous, easy integration with web databases, secure (HTTPS/TLS).  
* **Limitations:** High text-header overhead (>100s of bytes), synchronous pull-only model (forces wasteful client polling), heavy memory footprint.

---

### 🎴 Card 14:
Q14. Explain the working principle, strengths, and limitations of CoAP in IoT.  
**Ans.**  
* **Principle:** RESTful Client-Server protocol running over UDP, using compact binary headers (4 bytes min) and supporting Observation mode.  
* **Strengths:** Tiny packet overhead, asynchronous pushes, optimized for resource-constrained microcontrollers.  
* **Limitations:** Transport-layer unreliability (requires custom application-layer error handling), NAT traversal issues with UDP.

---

### 🎴 Card 15:
Q15. Explain the working principle, strengths, and limitations of MQTT in IoT.  
**Ans.**  
* **Principle:** Broker-based, event-driven Publish/Subscribe messaging protocol over TCP.  
* **Strengths:** Tiny binary headers (2 bytes min), decoupled one-to-many communication, three QoS levels, Last Will and Testament (LWT) support.  
* **Limitations:** Centralized broker acts as a single point of failure, TCP connection keep-alives drain battery, no native security (needs TLS).

---

### 🎴 Card 16:
Q16. Summarize the transport protocol, architecture model, and minimum header size of HTTP, CoAP, and MQTT.  
**Ans.**  
* **HTTP:** TCP | Client-Server (Req-Resp) | 100+ bytes (ASCII text headers).  
* **CoAP:** UDP | Client-Server (RESTful + Observe) | 4 bytes (Binary header).  
* **MQTT:** TCP | Broker-based (Publish-Subscribe) | 2 bytes (Binary header).