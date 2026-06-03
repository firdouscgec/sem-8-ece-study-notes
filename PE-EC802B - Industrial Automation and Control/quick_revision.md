# Quick Revision: PE-EC802B - Industrial Automation and Control

This document compiles high-density definitions, essential formulas, tuning tables, practicing diagrams, and a comprehensive database of solved exam one-liners across all 4 units for active recall.

---

## Section 1: Core Definitions to Memorize

### Unit I: Sensors & Actuators
- **Active Transducers:** Self-generating sensors that convert physical energy directly into electrical energy without requiring an external power source (e.g., Thermocouples, Piezoelectric crystals).
- **Passive Transducers:** Sensors that cause a change in electrical parameters ($R, L, C$) and require an auxiliary external electrical source to operate (e.g., RTDs, LVDTs, Strain Gauges).
- **LVDT (Linear Variable Differential Transformer):** A passive inductive transducer consisting of a primary coil and two series-opposing secondary coils. It measures linear displacement with infinite resolution by tracking the position of a moving ferromagnetic core.
- **Seebeck Effect:** The generation of an electromotive force (EMF) when two dissimilar metal junctions are held at different temperatures.
- **Gauge Factor (G):** A measure of the sensitivity of a strain gauge, representing the ratio of fractional change in resistance to longitudinal strain.
- **Back EMF ($E_b$):** The internal voltage induced in a DC motor's rotating armature that opposes the applied terminal voltage.
- **Motor Starters:** Devices that limit the high starting current of a motor (which occurs because Back EMF is zero at standstill) by inserting a variable series resistance.
- **Pneumatic Actuator:** An actuator that converts compressed air signals (standard $3\text{--}15\ \text{psi}$) into linear or rotary displacement.
- **Optoisolation:** The use of an optocoupler (LED + phototransistor) to transmit signals across an optical path, preventing high voltage transients on the field side from damaging the controller.
- **Calibration:** The process of comparing an instrument's output against a traceable reference standard of higher accuracy to detect deviations and establish correction bounds.
- **Systematic Errors:** Predictable, unidirectional measurement offsets caused by calibration errors, environmental changes, or parallax. They can be eliminated by calibration.
- **Random Errors:** Unpredictable variations caused by electrical noise or environmental fluctuations. They cannot be eliminated but are reduced statistically using the mean of multiple readings.

### Unit II: Controller Tuning
- **Servo Operation:** A control loop operating condition where the primary goal is to track a dynamically changing setpoint ($R(s)$).
- **Regulatory Operation:** A control loop operating condition where the primary goal is to keep the process variable constant by rejecting load disturbances ($D(s)$).
- **Self-Regulating System:** A process that naturally finds a new stable equilibrium following a step change in input without any controller intervention (e.g., gravity-drained liquid tank).
- **Non-Self-Regulating (Integrating) System:** A process that continuously drifts or ramps following a step input change until a physical limit is hit (e.g., pump-drained tank).
- **Dead-Time (Transport Lag):** The time delay between the application of an input signal and the first observable process response, modeled as $e^{-s T_d}$.
- **Proportional Band (PB):** The percentage of error required to drive the controller output from $0\%$ to $100\%$. Formulated as $PB = 100/K_c$.
- **Reset Windup:** The saturation of an Integral controller's output due to a persistent error, leading to large overshoot as the controller takes time to decrease its integrated value.
- **Noise Amplification:** A major limitation of Derivative controllers where high-frequency measurement noise is amplified by the derivative term ($\tau_D \frac{de}{dt}$), causing control valve wear.

### Unit III: Automation Systems
- **PLC (Programmable Logic Controller):** A rugged, solid-state industrial computer designed to monitor inputs, execute sequential program logic, and control field actuators.
- **PLC Scan Cycle:** The continuous execution cycle consisting of: (1) Read inputs to image table, (2) Solve ladder program sequentially, (3) Perform diagnostics/comm, and (4) Update output terminals.
- **DCS (Distributed Control System):** A control architecture where autonomous controllers (LCUs) are distributed throughout a plant, coordinated via a high-speed system bus, eliminating a single point of failure.
- **SCADA (Supervisory Control and Data Acquisition):** A software-hardware system designed for supervisory control and real-time telemetry data collection from geographically dispersed remote assets.
- **Master Terminal Unit (MTU):** The central host server in a SCADA system that queries remote field stations, stores databases, and drives operator HMIs.
- **Remote Terminal Unit (RTU):** A rugged remote microcontroller deployed at SCADA field sites to collect sensor data, format telemetry, and execute supervisory commands.
- **Globe Valve:** A linear control valve with a spherical body and baffle plate, widely used for throttling fluid pressure and flow rate control.
- **Valve Seat Ring:** The stationary seat ring fixed inside a control valve. When the plug is fully connected to the seat, the valve is fully closed.

### Unit IV: Advanced Control Techniques
- **Feedforward Control:** A proactive control strategy where load disturbances are measured and corrected for before they affect the process variable.
- **Ratio Control:** A control system designed to maintain a constant ratio between two flow streams ($R = F_C / F_W$).
- **Cascade Control:** A nested loop configuration containing a primary (outer) Master loop and a fast-acting secondary (inner) Slave loop.
- **Split-Range Control:** A loop configuration where a single controller output is split to drive two or more control valves sequentially (e.g. heating and cooling).
- **Override (Selective) Control:** A safety loop where multiple controllers share a single control valve through High/Low Selectors to protect equipment during limit crossings.
- **Adaptive Control:** A control system that adjusts its gains dynamically in real-time to compensate for process gain drift.
- **Internal Model Control (IMC):** A control structure running a process model in parallel with the actual plant to isolate disturbances ($d = Y - \tilde{Y}$) and feed them back to the controller.

---

## Section 2: Key Formulas & Parameter Tables

### 1. Transducer & Actuator Physics
- **Thermocouple EMF:**
  $$E = a(T_{hot} - T_{cold}) + b(T_{hot} - T_{cold})^2$$
- **Cold Junction Compensation:**
  $$V_{net} = V_{raw} + V_{comp}$$
- **RTD Resistance:**
  $$R_T = R_0 [1 + \alpha(T - T_0)]$$
- **Strain Gauge Gauge Factor (G):**
  $$G = \frac{\Delta R/R}{\Delta L/L} = 1 + 2\nu + \frac{\Delta\rho/\rho}{\Delta L/L}$$
  where $\nu$ is Poisson's ratio, and $\frac{\Delta\rho}{\rho}$ is the piezoresistive effect.
- **Ultrasonic Distance (ToF):**
  $$D = \frac{v \times t}{2}$$
  where $v$ is the speed of sound ($343\ \text{m/s}$ at $20^\circ\text{C}$), and $t$ is the time-of-flight.
- **DC Motor Armature Current & Back EMF:**
  $$E_b = V - I_a R_a \implies I_{start} = \frac{V}{R_a} \quad (\text{since } E_b = 0 \text{ at } N=0)$$

### 2. Controller Equations
- **Active Low-Pass Filter (LPF) Transfer Function & Cut-off:**
  $$H(s) = \frac{A_v}{1 + sRC}, \quad f_c = \frac{1}{2\pi RC}$$
- **Active High-Pass Filter (HPF) Transfer Function & Cut-off:**
  $$H(s) = \frac{A_v sRC}{1 + sRC}, \quad f_c = \frac{1}{2\pi RC}$$
- **Parallel PID Controller Transfer Function:**
  $$G_c(s) = K_c \left[ 1 + \frac{1}{\tau_I s} + \tau_D s \right]$$
- **Ideal Feedforward Controller:**
  $$G_{ff}(s) = -\frac{G_d(s)}{G_v(s) G_p(s)}$$
- **First-Order Padé Approximation of Dead Time:**
  $$e^{-s T_d} \approx \frac{1 - \frac{T_d}{2} s}{1 + \frac{T_d}{2} s}$$

---

### 3. Controller Tuning Tables

**ZN Open-Loop (Process Reaction Curve) Tuning Table:**
- Parameters: Dead time ($L$), Time constant ($T$).
| Controller Type | Proportional Gain ($K_c$) | Integral Time ($\tau_I$) | Derivative Time ($\tau_D$) |
| :--- | :--- | :--- | :--- |
| **P** | $\frac{T}{L}$ | $-$ | $-$ |
| **PI** | $0.9 \frac{T}{L}$ | $3.3 L$ | $-$ |
| **PID** | $1.2 \frac{T}{L}$ | $2.0 L$ | $0.5 L$ |

**ZN Closed-Loop (Ultimate Gain) Tuning Table:**
- Parameters: Ultimate Gain ($K_u$), Ultimate Period ($P_u$).
| Controller Type | Proportional Gain ($K_c$) | Integral Time ($\tau_I$) | Derivative Time ($\tau_D$) |
| :--- | :--- | :--- | :--- |
| **P** | $0.5 K_u$ | $-$ | $-$ |
| **PI** | $0.45 K_u$ | $\frac{P_u}{1.2}$ | $-$ |
| **PID** | $0.6 K_u$ | $0.5 P_u$ | $\frac{P_u}{8}$ |

**Cohen-Coon PID Formulas (Quarter-Amplitude Decay):**
- Parameters: Process Gain ($K_p$), Dead time ($L$), Time constant ($T$).
$$K_c = \frac{1}{K_p} \frac{T}{L} \left[ \frac{4}{3} + \frac{L}{4T} \right], \quad \tau_I = L \left[ \frac{32 + 6(L/T)}{13 + 8(L/T)} \right], \quad \tau_D = L \left[ \frac{4}{11 + 2(L/T)} \right]$$

### 4. Error Propagation
- **Addition or Subtraction ($X = x_1 \pm x_2$):**
  $$\Delta X = \Delta x_1 + \Delta x_2 \quad (\text{absolute errors sum})$$
- **Multiplication or Division ($X = x_1 \cdot x_2$ or $X = x_1 / x_2$):**
  $$\frac{\Delta X}{X} = \frac{\Delta x_1}{x_1} + \frac{\Delta x_2}{x_2} \quad (\text{relative errors sum})$$

---

## Section 3: Diagrams to Practice Sketching

Prepare to sketch these block architectures, response curves, and circuit schematics by hand:

### 1. LVDT Electro-Mechanical Schematic (Unit I)
Detailed diagram showing the primary and secondary series-opposing windings with a movable magnetic core.
![LVDT Electro-Mechanical Schematic](../Images/chapter_01/lvdt_schematic.png)

### 2. LVDT Transfer Characteristics (Unit I)
Output voltage magnitude showing a linear response with a null residual voltage, and the $180^\circ$ phase shift through null.
![LVDT Transfer Characteristics](../Images/chapter_01/lvdt_transfer_char.png)

### 3. Thermocouple & Cold Junction Compensation (Unit I)
Circuit setup showing measuring and reference junctions with an active compensation bridge circuit.
![Thermocouple & Cold Junction Compensation](../Images/chapter_01/thermocouple_compensation.png)

### 4. Pneumatic Spring-Diaphragm Actuator (Unit I)
Mechanical assembly converting control air pressure ($3\text{--}15\ \text{psi}$) to linear stem displacement.
![Pneumatic Spring-Diaphragm Actuator](../Images/chapter_01/pneumatic_actuator.png)

### 5. Signal Conditioning Flow (Unit I)
The sequence of hardware stages processing a physical sensor variable into a digital signal.
![Signal Conditioning Functional Architecture](../Images/chapter_01/signal_conditioning_block.png)

### 6. Active Filters (Unit I)
Operational amplifier circuits for low-pass and high-pass filtering.
![Active Filter Circuit Topologies](../Images/chapter_01/opamp_filters.png)

### 7. OP-AMP Parallel PID (Unit II)
The physical summing op-amp schematic combining proportional, integral, and derivative paths.
![Parallel OP-AMP PID Controller](../Images/chapter_02/opamp_pid_parallel.png)

### 8. PLC Architecture (Unit III)
Internal modules showing CPU, memory, power supply, system bus, and input/output interface cards.
![PLC Hardware Architecture Block Diagram](../Images/chapter_03/plc_architecture.png)

### 9. PLC Ladder Logic (Unit III)
Start/Stop latch logic and Auto-Filling tank logic.
![Motor Start/Stop Latching Control](../Images/chapter_03/motor_latch.png)
![PLC Tank Level Control System](../Images/chapter_03/tank_level_ladder.png)

### 10. DCS Levels (Unit III)
The five levels of hierarchical control: Level 0 (Field), Level 1 (Direct Control), Level 2 (Supervisory), Level 3 (Production), and Level 4 (Enterprise).
![DCS Hierarchical Levels](../Images/chapter_03/dcs_hierarchy.png)

### 11. SCADA Structure (Unit III)
Geographically distributed control architecture showing the Master Terminal Unit (MTU), Remote Terminal Units (RTUs), PLCs, and WAN link.
![SCADA System Topology Block Diagram](../Images/chapter_03/scada_architecture.png)

### 12. Cascade Control Loop (Unit IV)
Nested block diagram featuring a primary (outer) loop controller and a fast secondary (inner) loop controller.
![Cascade Control Loop Block Diagram](../Images/chapter_04/cascade_block.png)

### 13. Override Control (Unit IV)
Selective control block diagram implementing high/low limit selection to protect hardware.
![Override (Selective) Control Loop](../Images/chapter_04/override_control.png)

### 14. Split-Range Control (Unit IV)
Response curves demonstrating a single controller command split to drive multiple actuators sequentially.
![Split-Range (Duplex) Control Loop Graph](../Images/chapter_04/split_range.png)

### 15. Adaptive Controllers (Unit IV)
Block diagrams for both Model Reference Adaptive Control (MRAC) and Self-Tuning Regulators (STR).
![Model Reference Adaptive Control (MRAC)](../Images/chapter_04/mrac_block.png)
![Self-Tuning Regulator (STR)](../Images/chapter_04/str_block.png)

### 16. IMC Block Diagram (Unit IV)
Internal Model Control block structure feeding back isolated disturbances to the controller.
![Internal Model Control (IMC) Block Diagram](../Images/chapter_04/imc_block.png)

---

## Section 4: Solved Exam One-Liners (Active Recall Database)

- **Q1. What is the operating frequency of an ultrasonic sensor?**
  - *Answer:* **10–65 kHz**
- **Q2. The primary sensing element of the pressure thermometer is _______.**
  - *Answer:* **Pressure bulb filled with a liquid**
- **Q3. Thermocouples generate output voltage according to the _______.**
  - *Answer:* **Seebeck effect**
- **Q4. Touch screen devices use which sensor?**
  - *Answer:* **Capacitive sensors**
- **Q5. What is the purpose of a pressure gauge in a boiler plant?**
  - *Answer:* **To measure pressure and display it**
- **Q6. State the cause for using starters with D.C. motors.**
  - *Answer:* **To limit the high starting current**
- **Q7. The span of the pneumatic signal used in industry is _______.**
  - *Answer:* **3-15 psi**
- **Q8. The gauge factor of a strain gauge indicates its _______.**
  - *Answer:* **Sensitivity**
- **Q9. Cohen-Coon tuning rules are used for _______ systems.**
  - *Answer:* **Processes with time-lag and self-regulation**
- **Q10. What type of controller is used for the elimination of offset?**
  - *Answer:* **Integral controller (I-controller)**
- **Q11. The Ziegler-Nichols tuning method is used for _______.**
  - *Answer:* **Processes with time-lag and self-regulation**
- **Q12. The derivative mode (D controller) is also known as _______.**
  - *Answer:* **Rate controller**
- **Q13. If the proportional band of an electronic PID controller is set at 10, then what is the proportional gain ($K_c$)?**
  - *Answer:* **Proportional gain $K_c = 100 / PB = 100/10 = 10$**
- **Q14. The quarter-amplitude decay ratio is basically a design criterion specified by the Ziegler-Nichols method which implies that the amplitude of an oscillation must be reduced by a factor of _______.**
  - *Answer:* **1/4**
- **Q15. A summing amplifier block followed by an inverter block represents a _______ controller.**
  - *Answer:* **PI/PID controller** (when integrating and proportional resistors are configured)
- **Q16. What are the advantages of a pneumatic controller?**
  - *Answer:* **Simple construction, explosion-proof/safe in hazardous areas, high power output**
- **Q17. Which of the following controllers has the maximum offset? (a) P-controller (b) P-I controller (c) P-I-D controller (d) P-D controller**
  - *Answer:* **(a) P-controller**
- **Q18. In an electronic Integral controller, if the resistance and capacitance values are both doubled, then the controller response time will be _______ and the controller gain will be _______.**
  - *Answer:* **Doubled, quartered** (since integration time constant $\tau_I = RC$ is quadrupled)
- **Q19. If the Proportional Band (PB) of a P-controller is very wide, then the system response is _______.**
  - *Answer:* **Slow (and has high offset)**
- **Q20. The function of reset action in a process controller is to _______.**
  - *Answer:* **Eliminate offset (steady-state error)**
- **Q21. Which controllers do not show a continuous action?**
  - *Answer:* **Digital controllers** (discrete-time action)
- **Q22. What is the transfer function of a dead-time element?**
  - *Answer:* **$G(s) = e^{-s T_d}$**
- **Q23. Provide an example of a self-regulating system.**
  - *Answer:* **Liquid level in a tank with constant gravity outflow**
- **Q24. Which control valve is used for pressure control?**
  - *Answer:* **Globe valve** (often used for throttling control)
- **Q25. Database management and decisions regarding production are handled in which level of the DCS structure?**
  - *Answer:* **Level 3 (Production control/Management level)**
- **Q26. What are the components of a SCADA system?**
  - *Answer:* **MTU (Master Terminal Unit), RTU (Remote Terminal Unit) or PLCs, Communication Network, HMI (Human Machine Interface)**
- **Q27. When a control valve plug is fully connected to the _______, then it is fully closed.**
  - *Answer:* **Valve seat**
- **Q28. A cascade controller is used when the process shows _______.**
  - *Answer:* **Slow response and large time lag (multiple capacities)**
- **Q29. State the load disturbances in the feed-forward control strategy of a simple heat exchanger.**
  - *Answer:* **Inlet flow rate, inlet temperature, and fluid composition**
- **Q30. Which control scheme is known as anticipatory control?**
  - *Answer:* **Feed-forward control**
- **Q31. When should Cascade Control be used?**
  - *Answer:* **When there are significant secondary disturbances that affect the primary loop**
- **Q32. The response of Feed-forward control is _______ than Feedback control.**
  - *Answer:* **Faster (proactive/anticipatory)**
- **Q33. A ratio control system is a special type of _______ control system.**
  - *Answer:* **Feed-forward control system**
- **Q34. The purpose of ratio control is to _______.**
  - *Answer:* **Maintain a constant ratio between two process variables (e.g., fuel and air ratio)**
