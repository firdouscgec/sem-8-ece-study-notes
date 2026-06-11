# Flashcards: Unit VIII: Embedded Code Development & Prototype to Reality

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit VIII.

---

### 🎴 Card 1:
Q1. Why should dynamic memory allocation be avoided on microcontrollers?  
**Ans.** Calling `malloc()`/`free()` at runtime causes **heap fragmentation** — free memory splits into non-contiguous blocks too small for new allocations. Microcontrollers lack virtual memory, so fragmentation leads to crashes. Use fixed-size, statically allocated buffers instead.

---

### 🎴 Card 2:
Q2. What is the difference between blocking delays and non-blocking timer-based state machines?  
**Ans.** `delay()` halts the entire CPU, wasting cycles and blocking other tasks. Non-blocking approaches use `millis()` or hardware timer interrupts to schedule work, allowing the CPU to handle other events while waiting.

---

### 🎴 Card 3:
Q3. Name three techniques for optimizing battery life in embedded IoT firmware.  
**Ans.**  
1. Leverage deep sleep modes (power down CPU/radio, wake on timer/GPIO).  
2. Reduce radio duty cycle (short, infrequent burst transmissions).  
3. Lower clock speed when idle via Dynamic Voltage and Frequency Scaling (DVFS).

---

### 🎴 Card 4:
Q4. What should you audit before adopting a third-party library for an embedded project?  
**Ans.** Compile the library and check its **Flash and RAM consumption** using the compiler's memory usage report. Avoid bloated frameworks designed for desktops; prefer lightweight, single-purpose embedded libraries.

---

### 🎴 Card 5:
Q5. Compare Serial Print debugging and JTAG/SWD hardware debugging.  
**Ans.**  
* **Serial Print:** Simple, no special hardware. But it modifies code timing (masks race conditions) and consumes UART and RAM.  
* **JTAG/SWD:** Non-intrusive, allows breakpoints and real-time register inspection. But requires a physical debug probe and complex setup.

---

### 🎴 Card 6:
Q6. Name five common funding channels for IoT startups.  
**Ans.**  
1. Bootstrapping (self-funding).  
2. Crowdfunding (Kickstarter/Indiegogo).  
3. Angel investors (seed equity).  
4. Venture capital (Series A/B/C).  
5. Government grants and hardware accelerators (SBIR, HAX, Techstars).

---

### 🎴 Card 7:
Q7. What is the Business Model Canvas and how many building blocks does it contain?  
**Ans.** The BMC (Alexander Osterwalder) is a single-page strategic tool mapping **9 building blocks**: Customer Segments, Value Proposition, Channels, Customer Relationships, Revenue Streams, Key Resources, Key Activities, Key Partnerships, and Cost Structure.

---

### 🎴 Card 8:
Q8. Describe the Build-Measure-Learn loop in Lean Startup methodology applied to IoT.  
**Ans.**  
1. **Build:** Create a Minimum Viable Product (MVP) — simplest functional prototype.  
2. **Measure:** Deploy to early adopters; collect usage data and error rates.  
3. **Learn:** Analyze data to validate or invalidate the core hypothesis. Then **Persevere** or **Pivot**.

---

### 🎴 Card 9:
Q9. What does "Pivot or Persevere" mean in the context of an IoT startup?  
**Ans.** After each Build-Measure-Learn cycle, the startup decides: **Persevere** (data validates the hypothesis, continue the current direction) or **Pivot** (data invalidates the hypothesis, change the customer segment, value proposition, or technology platform).

---

### 🎴 Card 10:
Q10. State two advantages and two disadvantages of applying Lean Startup to IoT hardware ventures.  
**Ans.**  
* *Advantages:* Reduces financial risk before expensive mass production; accelerates time-to-market by focusing on validated features.  
* *Disadvantages:* Hardware MVPs are slower and costlier to iterate than software MVPs; early adopters may not represent the broader market.

---

### 🎴 Card 11:
Q11. List the four phases of the Reliable Data Transfer Algorithm in IoT/WSN networks.  
**Ans.** 
1. **Initialization:** Prepares routing tables, synchronizes nodes, and resets sequence counters.
2. **Message Relaying:** Sensors forward packets **hop-by-hop** through router nodes toward the sink.
3. **Lost Message Detection:** The receiver (sink) monitors sequence gaps (e.g. 1, 2, 4) to identify missing packets.
4. **Selective Recovery:** The sink requests retransmission of **only the specific missing packets** (e.g. packet 3), minimizing channel congestion and node power consumption.

