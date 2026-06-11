# Flashcards: Unit VI: Prototyping Embedded Devices

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit VI.

---

### 🎴 Card 1:
Q1. What is the fundamental architectural difference between Arduino and Raspberry Pi?  
**Ans.** Arduino is a **microcontroller** platform (8-bit ATmega, bare-metal firmware, no OS, instant boot). Raspberry Pi is a **microprocessor** platform (64-bit ARM Cortex-A72 SoC, runs a full Linux OS, 15–30 second boot).

---

### 🎴 Card 2:
Q2. Compare Arduino and Raspberry Pi across RAM, connectivity, and power consumption.  
**Ans.**  
* **Arduino:** 2 KB SRAM, no built-in Wi-Fi/BLE (needs shields), ultra-low power (~50 mA).  
* **Raspberry Pi:** 1–8 GB LPDDR4, built-in Wi-Fi/BLE/Ethernet, higher power (~600 mA–1.2 A).

---

### 🎴 Card 3:
Q3. When should you use Arduino over Raspberry Pi for an IoT project?  
**Ans.** Use Arduino for single-task, deterministic, real-time control loops requiring microsecond-level timing (e.g., reading a sensor every 100 ms and toggling a relay), where low power consumption and instant boot are critical.

---

### 🎴 Card 4:
Q4. List five strengths of the Raspberry Pi for IoT prototyping.  
**Ans.**  
1. Full Linux OS support (thousands of packages).  
2. High processing power (quad-core ARM, 1.5 GHz).  
3. Built-in Wi-Fi, BLE, and Gigabit Ethernet.  
4. Massive community and documentation.  
5. Versatile 40-pin GPIO header (I2C, SPI, UART).

---

### 🎴 Card 5:
Q5. List five limitations of the Raspberry Pi for IoT.  
**Ans.**  
1. No built-in ADC (needs external MCP3008).  
2. High power consumption (~1.2 A under load).  
3. Non-real-time OS (cannot guarantee microsecond timing).  
4. SD card filesystem corruption risk on power loss.  
5. Thermal throttling under sustained CPU load.

---

### 🎴 Card 6:
Q6. Name four operating systems supported by the Raspberry Pi.  
**Ans.** Raspberry Pi OS (Debian-based, official), Ubuntu Server/Desktop (ARM64), Windows 10 IoT Core (headless UWP apps), and RISC OS (lightweight, fast-boot niche OS).

---

### 🎴 Card 7:
Q7. Define GPIO pins and name the three communication buses available on the Raspberry Pi GPIO header.  
**Ans.** **GPIO** pins are programmable digital pins configurable as Input or Output. The three communication buses are:  
1. **I2C** (SDA + SCL, shared multi-device bus).  
2. **SPI** (MOSI, MISO, SCLK, CS, high-speed full-duplex).  
3. **UART** (TX + RX, point-to-point serial).

---

### 🎴 Card 8:
Q8. State five critical safety guidelines for Raspberry Pi GPIO pins.  
**Ans.**  
1. Never exceed 3.3V on any GPIO pin.  
2. Never draw more than 16 mA per pin.  
3. Never short 5V to 3.3V or GND.  
4. Always use current-limiting resistors for LEDs.  
5. Never hot-plug wires while the Pi is powered on.

---

### 🎴 Card 9:
Q9. What are the two unique hardware advantages of the BeagleBone Black over the Raspberry Pi?  
**Ans.**  
1. **Built-in 12-bit ADC** (7 analog input channels at 1.8V max), unlike the Pi which has no native ADC.  
2. **PRU (Programmable Real-Time Units):** Two independent 200 MHz co-processors for deterministic, microsecond-level I/O alongside Linux.

---

### 🎴 Card 10:
Q10. Explain the architecture and primary limitation of the Electric Imp platform.  
**Ans.** Electric Imp splits device logic into Device Code (runs on the physical module) and Cloud Code (runs on Electric Imp's managed servers), using the proprietary Squirrel language. **Primary limitation:** Complete vendor lock-in — if the vendor shuts down its cloud, all devices become non-functional.

---

### 🎴 Card 11:
Q11. Why are smartphones and tablets useful as IoT prototyping platforms, and what is their biggest limitation?  
**Ans.** They have rich built-in sensor arrays (accelerometer, GPS, camera, microphone) and connectivity (Wi-Fi, BLE, NFC, Cellular), eliminating the need for separate breakout boards. **Biggest limitation:** Not designed for always-on, unattended operation (battery drain, OS updates, thermal shutdowns).

---

### 🎴 Card 12:
Q12. What is a Plug Computer and what is its primary IoT advantage?  
**Ans.** A Plug Computer is a small, wall-socket-mounted computing device (e.g., SheevaPlug) that runs Linux and draws power directly from mains electricity. **Primary advantage:** Always-on by design, making it ideal for 24/7 home automation hubs or local MQTT brokers without battery concerns.

---

### 🎴 Card 13:
Q13. Compare ARM vs. x86 ISAs, and state the roles of PCIe and Ethernet in IoT hardware.  
**Ans.** 
* **ARM vs. x86:** ARM is RISC-based, emphasizing energy efficiency for battery-powered edge nodes (e.g. Raspberry Pi). x86 is CISC-based, emphasizing processing throughput at the cost of high power and cooling (e.g. Galileo).
* **PCIe (Peripheral Component Interconnect Express):** A high-speed serial bus used to plug modular wireless cards (Wi-Fi, Bluetooth, 4G/5G, LoRaWAN) into gateways.
* **Ethernet (10/100Mbit):** Provides a physical wired LAN connection that is immune to RF interference, offering highly reliable and low-latency data transmission.

