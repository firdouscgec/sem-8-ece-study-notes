# Flashcards: Unit III - Automation Systems (PLC, DCS, SCADA)

These active recall Question-and-Answer cards are designed to test your memory on the PLC programming, architecture, DCS hierarchy, and SCADA systems of Unit III.

---

### 🎴 Card 1: PLC vs. Relay Control Panels
*   **Question:** State 3 advantages of Programmable Logic Controllers (PLCs) over conventional electromagnetic relay control systems.
*   **Answer:**
    1.  **Flexibility:** Logic modifications are done through software programming without re-wiring.
    2.  **Reliability & Maintenance:** Solid-state components eliminate mechanical wear and contact failure. Diagnostics display fault locations.
    3.  **Space and Cost:** A single compact PLC replaces hundreds of relays, decreasing panel footprint and wiring cost.

---

### 🎴 Card 2: PLC Hardware Architecture
*   **Question:** What are the four major hardware components of a industrial PLC?
*   **Answer:**
    1.  **Central Processing Unit (CPU):** Executes the program logic and controls memory.
    2.  **Memory Unit:** Stores operating system, user program code, and I/O status tables.
    3.  **Power Supply:** Converts industrial AC voltage to stable low-voltage DC (5V/24V) for internal circuits.
    4.  **I/O Modules:** Interfaces the CPU to field devices (inputs: switches, sensors; outputs: solenoids, contactors).

---

### 🎴 Card 3: PLC Scan Cycle
*   **Question:** Explain the steps executed during a single PLC Scan Cycle.
*   **Answer:**
    1.  **Read Inputs:** Reads the status of all input modules and copies their states into the Input Image Table memory.
    2.  **Program Execution:** Solves the ladder logic code rung-by-rung using the image tables.
    3.  **Diagnostics & Communication:** Performs internal self-tests and processes communications (e.g. SCADA requests).
    4.  **Write Outputs:** Copies the solved states from the Output Image Table to the physical output terminals to drive actuators.

---

### 🎴 Card 4: IEC 61131-3 PLC Languages
*   **Question:** What are the 5 standard PLC programming languages defined by IEC 61131-3?
*   **Answer:**
    1.  **Ladder Diagram (LD):** Graphical language resembling relay schematics (most common).
    2.  **Function Block Diagram (FBD):** Graphical language representing signals flowing through logical functional blocks.
    3.  **Structured Text (ST):** High-level, text-based programming (similar to C/Pascal).
    4.  **Instruction List (IL):** Low-level, text-based assembly-like language.
    5.  **Sequential Function Chart (SFC):** Structured flowchart language used to coordinate sequential steps and transitions.

---

### 🎴 Card 5: SCADA Definition & Functions
*   **Question:** Define SCADA and state its 4 primary functions.
*   **Answer:**
    *   **SCADA:** Supervisory Control and Data Acquisition. A software-based system used to monitor and control large-scale distributed processes.
    *   **Functions:**
        1.  **Data Acquisition:** Gathering analog/digital readings from RTUs and PLCs.
        2.  **Supervisory Control:** Sending setpoints or control commands to field controllers.
        3.  **Data Presentation (HMI):** Displaying live process values and graphics to operators.
        4.  **Alarming and Archiving:** Recording historical data trends and logging warning states.

---

### 🎴 Card 6: SCADA System Components
*   **Question:** What is the role of MTU, RTU, and HMI in a SCADA architecture?
*   **Answer:**
    *   **Master Terminal Unit (MTU):** The central server/computer that runs the SCADA software, initiates communications, processes data, and sends control commands.
    *   **Remote Terminal Unit (RTU):** Field microprocessors that read sensor inputs, execute basic control, transmit data to the MTU, and receive MTU commands.
    *   **Human-Machine Interface (HMI):** Graphic terminals/displays showing real-time trends, animations, and alarms to operators.

---

### 🎴 Card 7: DCS Definition & DCS vs. SCADA
*   **Question:** What is a Distributed Control System (DCS), and how does it differ from SCADA?
*   **Answer:**
    *   **DCS:** A control system where controllers are distributed throughout different geographic/process zones, connected via a high-speed control network.
    *   **Difference:** DCS is **process-centric** (optimized for continuous analog PID loops, high speed, and tightly integrated database), whereas SCADA is **data-centric** (optimized for geographically wide areas with slower telemetry, dial-up/wireless links, and supervisory control).

---

### 🎴 Card 8: DCS Hierarchical Levels
*   **Question:** Detail the 5 levels of a standard Distributed Control System (DCS) hierarchy.
*   **Answer:**
    *   **Level 0 (Field Level):** Physical sensors, transmitter elements, and control valve actuators.
    *   **Level 1 (Direct Control):** Dedicated process controllers (I/O cards, controllers executing PID algorithms).
    *   **Level 2 (Supervisory Level):** Operator workstations (HMIs, console computers).
    *   **Level 3 (Production Control):** Production scheduling, quality control, database management.
    *   **Level 4 (Enterprise Level):** Corporate ERP systems for business logistics and planning.

---

### 🎴 Card 9: PLC Ladder Logic - Motor Start/Stop
*   **Question:** Describe how a Start/Stop motor control with a seal-in contact is programmed in a Ladder Diagram.
*   **Answer:**
    *   **Rung configuration:** A single rung connects the left rail (Power) to the motor coil output `[M]` on the right rail.
    *   **Logic path:** 
        *   An `NO` Start button contact is placed in parallel with an `NO` auxiliary contact of the motor coil output `[M]` (acting as the latch/seal-in).
        *   This parallel combination is placed in series with an `NC` Stop button contact and an `NC` overload contact.
        *   Pressing Start completes the path to `[M]`, which immediately closes its own parallel auxiliary contact, maintaining current flow even after Start is released.

---

### 🎴 Card 10: PLC Ladder Logic - EX-OR Gate
*   **Question:** How do you realize an EX-OR logic operation ($Y = A \bar{B} + \bar{A} B$) in a PLC ladder diagram?
*   **Answer:**
    *   **Rung configuration:** Consists of two parallel branches feeding into a single output coil `[Y]`.
    *   **Branch 1:** Contains an `NO` contact of input `A` in series with an `NC` contact of input `B`.
    *   **Branch 2:** Contains an `NC` contact of input `A` in series with an `NO` contact of input `B`.

---

### 🎴 Card 11: PLC Ladder Logic - Level Control
*   **Question:** Describe the ladder logic required to control a tank pump: turn ON when low sensor (L) triggers, and turn OFF when high sensor (H) triggers.
*   **Answer:**
    *   **Rung configuration:** A single rung controls the pump coil output `[P]`.
    *   **Logic path:** 
        *   An `NO` contact of low sensor `L` is placed in parallel with an `NO` latch contact of the pump `P`.
        *   This parallel block is placed in series with an `NC` contact of high sensor `H`.
        *   When `L` is activated, the rung completes and turns on `P`, which seals in. The pump runs until `H` activates, opening the `NC` contact and breaking the seal-in.
