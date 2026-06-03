# Chapter-wise Sequenced Questions & Repeated Trends

This document organizes the Previous Year Questions (PYQs) from 2022–2025 by syllabus unit and introduces high-probability practice questions to ensure 100% syllabus coverage.

---

## 📂 Chapter 1: Unit I - Sensors, Actuators & Signal Conditioning

### 1. Very Short Answer Questions (1 Mark)
* **Q1.** What is the operating frequency of an ultrasonic sensor? `[1M]` `[2024-25]`
  * *Answer:* **10–65 kHz**
* **Q2.** The primary sensing element of the pressure thermometer is _______. `[1M]` `[2024-25]`
  * *Answer:* **Pressure bulb filled with a liquid**
* **Q3.** Thermocouples generate output voltage according to the _______. `[1M]` `[2024-25]`
  * *Answer:* **Seebeck effect**
* **Q4.** Touch screen devices use which sensor? `[1M]` `[2024-25]`
  * *Answer:* **Capacitive sensors**
* **Q5.** What is the purpose of a pressure gauge in a boiler plant? `[1M]` `[2023-24]`
  * *Answer:* **To measure pressure and display it**
* **Q6.** State the cause for using starters with D.C. motors. `[1M]` `[2023-24]`
  * *Answer:* **To limit the high starting current**
* **Q7.** The span of the pneumatic signal used in industry is _______. `[1M]` `[2022-23]`
  * *Answer:* **3-15 psi**
* **Q8.** The gauge factor of a strain gauge indicates its _______. `[1M]` `[2022-23]`
  * *Answer:* **Sensitivity**

### 2. Short Answer Questions (5 Marks)
* **Q1.** Explain the operation of a piezoelectric actuator. `[5M]` `[★★★★]` `[2024-25]`
* **Q2.** Describe the operation of a sensor protection circuit. `[5M]` `[★★★]` `[2024-25]`
* **Q3.** What are the different pressure sensors? Explain the application of force sensors. `[5M]` `[★★★★]` `[2023-24]`
* **Q4.** What are the different types of piezoelectric actuators? `[5M]` `[★★★]` `[2023-24]`
* **Q5.** Briefly explain the sensor protection circuit. `[5M]` `[★★★]` `[2023-24]`
* **Q6.** What is an ADC in digital signal processing? `[5M]` `[★★]` `[2023-24]`
* **Q7.** What do you mean by active and passive transducers? Give suitable examples. `[5M]` `[★★★★★]` `[2022-23]`
* **Q8.** What is the application of actuators? `[5M]` `[★★]` `[2022-23]`
* **Q9.** Explain the operation of a servomotor. `[5M]` `[★★★★]` `[2022-23]`
* **Q10.** Explain the operating principle of LVDT with a neat diagram. `[5M]` `[★★★★★]` `[2022-23]`
* **Q11. [Syllabus Gap - Practice]** Define Calibration. Explain the difference between Systematic (determinate) and Random (indeterminate) errors in measurement. `[5M]` `[★★★★]`
* **Q12. [Syllabus Gap - Practice]** How do we estimate the limiting error (or uncertainty) when multiple independent variables are combined in a system calculation? Write the formula. `[5M]` `[★★★]`

### 3. Long Answer Questions (15 Marks)
* **Q1. Stepper Motor, Noise, & Protection** `[15M]` `[★★★★]` `[2023-24]`
  * (a) Explain the construction and principle of action of a stepper motor. `[3M]`
  * (b) What is half-stepping and micro-stepping in connection with the running of a stepper motor? Explain with suitable diagrams. `[4M]`
  * (c) How do you suppress signal noise in practice? `[4M]`
  * (d) Explain various techniques to protect a sensor using a sensor protection circuit. `[4M]`
* **Q2. Signal Conditioning Design** `[15M]` `[★★★★★]` `[2024-25]`
  * (a) Define signal conditioning. Draw the block diagram of a signal conditioning circuit with all its functions. `[10M]`
  * (b) What is the importance of a signal conditioning circuit? `[5M]`
* **Q3. Filter Circuits** `[15M]` `[★★★★]` `[2023-24]`
  * (a) What is filtering in signal processing? What are the applications of a filtering circuit? `[5M]`
  * (b) Design the following filters using OP-AMPs and explain their working principles: High-pass, Low-pass, Band-pass, Band-reject. `[10M]`
* **Q4. LVDT Transfer Characteristics** `[15M]` `[★★★★★]` `[2022-23]`
  * (a) Draw a schematic diagram of an LVDT. `[5M]`
  * (b) Explain its electro-mechanical transfer characteristics with a suitable block diagram. `[10M]`
* **Q5. Thermocouple & Compensation** `[15M]` `[★★★★★]` `[2022-23]`
  * (a) State the principle on which the thermocouple works. Mention the name along with its temperature range and composition of two commonly used thermocouples. `[10M]`
  * (b) What is the technique of cold junction compensation? `[5M]`
* **Q6. Pneumatic Actuators & Motors** `[15M]` `[★★★★]` `[2022-23]`
  * (a) Draw the diagram of a pneumatic actuator and explain its operation in detail. `[10M]`
  * (b) Write the difference between a servomotor and a stepper motor. `[5M]`
* **Q7. Ultrasonic Sensors** `[15M]` `[★★]` `[2022-23]`
  * (a) Explain the principle of operation of an ultrasonic sensor with a neat sketch. `[10M]`
  * (b) Write the application areas of an ultrasonic sensor. `[5M]`

---

## 📂 Chapter 2: Unit II - Controller Tuning & Implementation

### 1. Very Short Answer Questions (1 Mark)
* **Q1.** Cohen-Coon tuning rules are used for _______ systems. `[1M]` `[2024-25]`
  * *Answer:* **Processes with time-lag and self-regulation**
* **Q2.** What type of controller is used for the elimination of offset? `[1M]` `[2024-25]`
  * *Answer:* **Integral controller (I-controller)**
* **Q3.** The Ziegler-Nichols tuning method is used for _______. `[1M]` `[2024-25]`
  * *Answer:* **Processes with time-lag and self-regulation**
* **Q4.** The derivative mode (D controller) is also known as _______. `[1M]` `[2024-25]`
  * *Answer:* **Rate controller**
* **Q5.** If the proportional band of an electronic PID controller is set at 10, then what is the proportional gain ($K_c$)? `[1M]` `[2024-25]`
  * *Answer:* **Proportional gain $K_c = 100 / PB = 100/10 = 10$**
* **Q6.** The quarter-amplitude decay ratio is basically a design criterion specified by the Ziegler-Nichols method which implies that the amplitude of an oscillation must be reduced by a factor of _______. `[1M]` `[2023-24]`
  * *Answer:* **1/4**
* **Q7.** A summing amplifier block followed by an inverter block represents a _______ controller. `[1M]` `[2023-24]`
  * *Answer:* **PI controller** (when integrating and proportional resistors are configured)
* **Q8.** What are the advantages of a pneumatic controller? `[1M]` `[2023-24]`
  * *Answer:* **Simple in construction, explosion-proof/safe in hazardous areas, high power output**
* **Q9.** Which of the following controllers has the maximum offset? `[1M]` `[2023-24]`
  * (a) P-controller (b) P-I controller (c) P-I-D controller (d) P-D controller
  * *Answer:* **(a) P-controller**
* **Q10.** In an electronic Integral controller, if the resistance and capacitance values are both doubled, then the controller response time will be _______ and the controller gain will be _______. `[1M]` `[2023-24]`
  * *Answer:* **Doubled, halved** (since integration time constant $\tau_I = RC$ is quadrupled)
* **Q11.** If the Proportional Band (PB) of a P-controller is very wide, then the system response is _______. `[1M]` `[2022-23]`
  * *Answer:* **Slow (and has high offset)**
* **Q12.** The function of reset action in a process controller is to _______. `[1M]` `[2022-23]`
  * *Answer:* **Eliminate offset (steady-state error)**
* **Q13.** Which controllers do not show a continuous action? `[1M]` `[2022-23]`
  * *Answer:* **Digital controllers** (discrete-time action)
* **Q14.** What is the transfer function of a dead-time element? `[1M]` `[2022-23]`
  * *Answer:* **$G(s) = e^{-s T_d}$**
* **Q15.** Provide an example of a self-regulating system. `[1M]` `[2022-23]`
  * *Answer:* **Liquid level in a tank with constant gravity outflow**

### 2. Short Answer Questions (5 Marks)
* **Q1.** Compare servo and regulatory operations in process control. `[5M]` `[★★★★★]` `[2024-25]`
* **Q2.** Write down the PID controller tuning criteria. `[5M]` `[★★★★]` `[2024-25]`

### 3. Long Answer Questions (15 Marks)
* **Q1. OP-AMP PID Controller Design** `[15M]` `[★★★★★]` `[2024-25]`
  * (a) Design electronic P, PI, and PD controllers using OP-AMP circuits, drawing their schematics and writing their transfer functions. `[10M]`
  * (b) What is the necessity of controller tuning? `[5M]`
* **Q2. Tuning Rules & Implementation** `[15M]` `[★★★★★]` `[2023-24]`
  * (a) Discuss the Ziegler-Nichols tuning method and Cohen-Coon tuning method. Explain the difference between their process reaction curves. `[5M]`
  * (b) Discuss the implementation of PID controllers in both digital (microcontroller/computer) and analog (electronic/pneumatic) domains. `[10M]`

---

## 📂 Chapter 3: Unit III - Automation Systems (PLC, DCS, SCADA)

### 1. Very Short Answer Questions (1 Mark)
* **Q1.** Which control valve is used for pressure control? `[1M]` `[2024-25]`
  * *Answer:* **Globe valve** (often used for throttling control)
* **Q2.** Database management and decisions regarding production are handled in which level of the DCS structure? `[1M]` `[2023-24]`
  * *Answer:* **Level 3 (Production control/Management level)**
* **Q3.** What are the components of a SCADA system? `[1M]` `[2023-24]`
  * *Answer:* **MTU (Master Terminal Unit), RTU (Remote Terminal Unit) or PLCs, Communication Network, HMI (Human Machine Interface)**
* **Q4.** When a control valve plug is fully connected to the _______, then it is fully closed. `[1M]` `[2023-24]`
  * *Answer:* **Valve seat**

### 2. Short Answer Questions (5 Marks)
* **Q1.** Explain the importance of DCS in process control. `[5M]` `[★★★★]` `[2024-25]`
* **Q2.** Discuss the advantages and disadvantages of PLCs over conventional electromagnetic relay-based controllers. `[5M]` `[★★★★★]` `[2023-24]`
* **Q3.** Define PLC. Explain the architecture of a PLC with a simplified block diagram. `[5M]` `[★★★★★]` `[2022-23]`
* **Q4. [Syllabus Gap - Practice]** List the five PLC programming languages as per the IEC 61131-3 standard. Briefly explain any two. `[5M]` `[★★★★]`

### 3. Long Answer Questions (15 Marks)
* **Q1. SCADA Architecture & Significance** `[15M]` `[★★★★★]` `[2024-25]`
  * (a) Write the full form of SCADA. What is the significance of SCADA in process control and automation? `[5M]`
  * (b) Describe the architecture of SCADA with a suitable block diagram, explaining the functions of its components. `[10M]`
* **Q2. PLC Design & Ladder Logic** `[15M]` `[★★★★★]` `[2023-24 Reconstructed]`
  * (a) Define PLC. State two advantages of PLC over traditional electromagnetic relay control panels. `[3M]`
  * (b) Develop PLC ladder logic diagrams for the following process automation applications:
    * (i) A standard Start/Stop latching control circuit for an industrial motor with an Emergency Stop button and overload input. `[3M]`
    * (ii) Realization of an EX-OR logic gate using basic contacts (NO/NC). `[3M]`
    * (iii) A liquid tank level control system: turn ON the filling pump when the low-level sensor (L) activates, and turn it OFF when the high-level sensor (H) activates. `[3M]`
    * (iv) Realization of standard logic gates: NAND and NOR operations. `[3M]`
* **Q3. DCS Block Diagram & Types** `[15M]` `[★★★★]` `[2023-24]`
  * (a) Draw the general block diagram of a Distributed Control System (DCS) and explain the function of the different blocks. `[6M]`
  * (b) What are the different types of DCS? `[4M]`
  * (c) Explain with a diagram the operation of any one of them in process control. `[5M]`

---

## 📂 Chapter 4: Unit IV - Advanced Control Techniques

### 1. Very Short Answer Questions (1 Mark)
* **Q1.** A cascade controller is used when the process shows _______. `[1M]` `[2024-25]`
  * *Answer:* **Slow response and large time lag (multiple capacities)**
* **Q2.** State the load disturbances in the feed-forward control strategy of a simple heat exchanger. `[1M]` `[2023-24]`
  * *Answer:* **Inlet flow rate, inlet temperature, and fluid composition**
* **Q3.** Which control scheme is known as anticipatory control? `[1M]` `[2022-23]`
  * *Answer:* **Feed-forward control**
* **Q4.** When should Cascade Control be used? `[1M]` `[2022-23]`
  * *Answer:* **When there are significant secondary disturbances that affect the primary loop**
* **Q5.** The response of Feed-forward control is _______ than Feedback control. `[1M]` `[2022-23]`
  * *Answer:* **Faster (proactive/anticipatory)**
* **Q6.** A ratio control system is a special type of _______ control system. `[1M]` `[2022-23]`
  * *Answer:* **Feed-forward control system**
* **Q7.** The purpose of ratio control is to _______. `[1M]` `[2022-23]`
  * *Answer:* **Maintain a constant ratio between two process variables (e.g., fuel and air ratio)**

### 2. Short Answer Questions (5 Marks)
* **Q1. [Syllabus Gap - Practice]** Explain the concept of Split-Range (Duplex) control. Give a practical industrial example where Split-Range control is applied. `[5M]` `[★★★★]`
* **Q2. [Syllabus Gap - Practice]** Explain the concept of Adaptive Control. State the difference between Self-Tuning Regulators (STR) and Model Reference Adaptive Control (MRAC). `[5M]` `[★★★]`
* **Q3. [Syllabus Gap - Practice]** What is Internal Model Control (IMC)? Draw its basic block diagram. `[5M]` `[★★★★]`

### 3. Long Answer Questions (15 Marks)
* **Q1. Feed-Forward Control System** `[15M]` `[★★★★★]` `[2024-25]`
  * (a) Draw the block diagram of a feed-forward control system and explain its operation. `[10M]`
  * (b) Compare feedback and feed-forward control systems. `[5M]`
* **Q2. Override Control** `[15M]` `[★★★★]` `[2024-25]`
  * (a) Explain the operation of override control with a neat sketch and a practical application example. `[10M]`
  * (b) What is the necessity of override control? `[5M]`
* **Q3. Cascade Control System** `[15M]` `[★★★★★]` `[2022-23]`
  * (a) State the advantages of a cascade controller. `[5M]`
  * (b) Draw the block diagram of a cascade control scheme and explain its operation, defining primary and secondary loops. `[10M]`
