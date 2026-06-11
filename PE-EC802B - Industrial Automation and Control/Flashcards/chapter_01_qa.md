# Flashcards: Unit I - Sensors, Actuators & Signal Conditioning

These active recall Question-and-Answer cards are designed to test your memory on the displacement, force, ultrasonic, temperature, and pressure sensors, actuators, and signal conditioning circuits of Unit I.

---

### 🎴 Card 1: Active vs. Passive Transducers
*   **Question:** What is the primary difference between Active and Passive transducers? Give examples of each.
*   **Answer:** 
    *   **Active Transducer (Self-generating):** Generates its own electrical output (voltage/current) without requiring an external power source. Examples: Thermocouple, Piezoelectric crystal, Solar cell.
    *   **Passive Transducer (Externally powered):** Requires an external electrical source to operate, as it produces a change in electrical parameters (resistance, capacitance, inductance). Examples: RTD, Thermistor, LVDT, Strain gauge.

---

### 🎴 Card 2: LVDT Operating Principle
*   **Question:** How does a Linear Variable Differential Transformer (LVDT) measure displacement?
*   **Answer:** It uses electromagnetic induction. It consists of one primary coil (excited by AC), two secondary coils connected in series-opposition, and a movable ferromagnetic core. As the core moves due to external displacement, the magnetic coupling between the primary and secondaries changes, creating a differential AC output voltage ($E_{out} = E_{s1} - E_{s2}$) proportional to the core's displacement.

---

### 🎴 Card 3: LVDT Null Voltage & Phase Shift
*   **Question:** What is "null voltage" in an LVDT, and how does the phase change across the null position?
*   **Answer:**
    *   **Null Voltage:** The small residual AC output voltage present when the core is exactly in the center (null position), caused by stray capacitances, harmonics, and magnetic leakage.
    *   **Phase Shift:** When the core passes the null position, the phase of the differential output voltage shifts by $180^\circ$, indicating the direction of movement.

---

### 🎴 Card 4: Thermocouple & Seebeck Effect
*   **Question:** State the physical principle on which the Thermocouple works.
*   **Answer:** The **Seebeck Effect**: When two dissimilar metals are joined to form two junctions kept at different temperatures, an electromotive force (EMF) or thermoelectric voltage is generated in the circuit, which is directly proportional to the temperature difference between the junctions ($V \propto T_{hot} - T_{cold}$).

---

### 🎴 Card 5: Thermocouple Types and Composition
*   **Question:** Name two commonly used industrial thermocouples along with their temperature ranges and material compositions.
*   **Answer:**
    1.  **Type K:**
        *   *Composition:* Chromel (Nickel-Chromium) (+) / Alumel (Nickel-Aluminum) (-)
        *   *Temperature Range:* $-200^\circ\text{C}$ to $+1250^\circ\text{C}$
    2.  **Type J:**
        *   *Composition:* Iron (+) / Constantan (Copper-Nickel) (-)
        *   *Temperature Range:* $0^\circ\text{C}$ to $+750^\circ\text{C}$

---

### 🎴 Card 6: Cold Junction Compensation (CJC)
*   **Question:** What is the necessity of Cold Junction Compensation in thermocouple measurements, and how is it done?
*   **Answer:**
    *   **Necessity:** Thermocouple EMF depends on the temperature difference between the hot (measuring) and cold (reference) junctions. If the cold junction temperature fluctuates with the ambient environment, measurement errors occur.
    *   **Implementation:** The reference junction temperature is measured using a stable solid-state sensor (like an RTD or thermistor), and a compensating voltage corresponding to this reference temperature is mathematically added to the thermocouple reading.

---

### 🎴 Card 7: Ultrasonic Sensor Principle
*   **Question:** Explain the operation of an ultrasonic sensor and write its distance calculation equation.
*   **Answer:**
    *   **Operation:** An ultrasonic transmitter emits a high-frequency sound wave (above 20 kHz). The wave travels through the air, hits an object, and reflects back. An ultrasonic receiver detects the returning echo.
    *   **Equation:** Distance $d = \frac{v \times t}{2}$ (where $v$ is the speed of sound in air, and $t$ is the round-trip time-of-flight).

---

### 🎴 Card 8: Motors Comparison
*   **Question:** Compare DC, Stepper, and Servo motors based on feedback and rotation control.
*   **Answer:**
    *   **DC Motor:** Open-loop, continuous high-speed rotation, requires feedback (tachometer) for speed control.
    *   **Stepper Motor:** Open-loop (typically), rotates in discrete angular steps (incrementally), high holding torque at standstill, prone to step loss.
    *   **Servo Motor:** Closed-loop (uses encoder feedback), precise control of angular position, speed, and acceleration, does not lose steps.

---

### 🎴 Card 9: Stepper Motor Stepping Modes
*   **Question:** Define Full-Stepping, Half-Stepping, and Micro-Stepping in stepper motors.
*   **Answer:**
    *   **Full-Stepping:** The motor rotates by its basic step angle (e.g. $1.8^\circ$) by exciting phases sequentially.
    *   **Half-Stepping:** Alternates between exciting one phase and two phases, doubling the resolution (e.g. $0.9^\circ$ steps) and smoothing movement.
    *   **Micro-Stepping:** Divides the step angle further by controlling winding currents continuously as sine/cosine waves, reducing vibration and noise.

---

### 🎴 Card 10: Piezoelectric Actuator
*   **Question:** Explain the principle of a Piezoelectric actuator.
*   **Answer:** It works on the **Inverse Piezoelectric Effect**: when an external electric field/voltage is applied across a piezoelectric crystal (such as quartz or PZT), the crystal experiences mechanical strain, resulting in microscopic physical deformation. Stacked layers are used in industry to generate high forces with sub-nanometer displacement resolution.

---

### 🎴 Card 11: Pneumatic Actuator
*   **Question:** Explain the operating mechanism of a diaphragm-type pneumatic actuator.
*   **Answer:** Compressed air (typically 3-15 psi) is introduced into a chamber separated by a flexible diaphragm. The air pressure pushes the diaphragm against a restoring spring, moving a stem connected to a control valve plug. When air pressure decreases, the spring pushes the diaphragm back to its default position.

---

### 🎴 Card 12: Signal Conditioning Blocks
*   **Question:** What are the five major operations in a standard analog sensor signal conditioning circuit?
*   **Answer:**
    1.  **Amplification:** Boosts weak sensor signals (millivolts) to standard levels (0-5V or 4-20mA).
    2.  **Filtering:** Suppresses high-frequency noise and interference.
    3.  **Isolation:** Protects controller circuits from high-voltage surges using optocouplers.
    4.  **Analog-to-Digital Conversion (ADC):** Converts analog voltage to binary numbers.
    5.  **Linearization/Compensation:** Corrects sensor non-linearities and temperature drift.

---

### 🎴 Card 13: Active Filters
*   **Question:** Draw the basic schematics of active Low-Pass and High-Pass filters using OP-AMPs and write their cutoff frequency equation.
*   **Answer:**
    *   **Low-Pass Filter:** Winding resistor $R$ on the non-inverting input path, with capacitor $C$ connected to ground. Passes DC and low frequencies.
    *   **High-Pass Filter:** Capacitor $C$ on the non-inverting input path, with resistor $R$ connected to ground. Passes high frequencies, blocks DC.
    *   **Cutoff Frequency:** $f_c = \frac{1}{2\pi R C}$

---

### 🎴 Card 14: Noise Suppression Techniques
*   **Question:** List 3 common methods used to suppress electrostatic and electromagnetic noise in industrial signal lines.
*   **Answer:**
    1.  **Shielding:** Encasing signal wires in a conductive braided copper shield connected to ground.
    2.  **Twisted-Pair Cabling:** Twisting signal wires together to cancel out differential-mode electromagnetic noise.
    3.  **Physical Separation:** Running low-voltage instrument signals in separate conduits away from high-power AC motor cables.

---

### 🎴 Card 15: Sensor Protection Circuits
*   **Question:** What components are used in sensor protection circuits to prevent damage from overvoltages?
*   **Answer:**
    *   **Zener Diodes:** Shunt voltage to ground if it exceeds the Zener breakdown threshold.
    *   **TVS (Transient Voltage Suppressors):** Clamp fast, high-voltage spikes (lightning/switching surges).
    *   **Current Limiting Resistors / Fuses:** Limit fault current entering the sensing pin.

---

### 🎴 Card 16: Calibration and Limiting Errors
*   **Question:** Define Calibration and Limiting Error.
*   **Answer:**
    *   **Calibration:** The process of comparing a sensor's measurement readings against a known, certified reference standard to determine accuracy and adjust deviation.
    *   **Limiting Error (Guarantee Error):** The maximum deviation or tolerance limit specified by the manufacturer within which the sensor error is guaranteed to lie (e.g. $\pm 1\%$ of full scale).

---

### 🎴 Card 17: Process Loop Standards & Converters (Q1.9)
*   **Question:** List the components of a standard 4–20 mA current loop, explain the benefits of a 4 mA active zero, and define the functions of I/P and P/I converters.
*   **Answer:**
    *   **Current Loop Components:**
        1.  **DC Power Supply:** Provides driving voltage (e.g., $24\ \text{V DC}$).
        2.  **Two-Wire Path:** Copper wires carrying the loop current.
        3.  **Transmitter:** Regulates current proportional to the sensor reading.
        4.  **Receiver / Load Resistor:** Converts loop current to voltage (e.g., $250\ \Omega$ converting $4\text{--}20\ \text{mA}$ to $1\text{--}5\ \text{V}$ for the ADC).
    *   **Benefits of 4 mA Active Zero:**
        1.  *Fault Detection:* Wire breakage drops current to $0\ \text{mA}$, triggering an alarm (unlike a $0\text{--}20\ \text{mA}$ loop where $0$ could represent a minimum process value).
        2.  *Self-Powering:* The $4\ \text{mA}$ standby current powers transmitter internal circuitry, eliminating the need for separate local power cables.
    *   **Converters:**
        *   **I/P Converter:** Converts electrical control current ($4\text{--}20\ \text{mA}$) into standard pneumatic pressure ($3\text{--}15\ \text{psi}$) to drive pneumatic actuators.
        *   **P/I Converter:** Converts pneumatic signal pressure ($3\text{--}15\ \text{psi}$) into an electrical current loop signal ($4\text{--}20\ \text{mA}$) for transmission.

---

### 🎴 Card 18: Capacitive & Potentiometric Displacement Sensors (Q1.10)
*   **Question:** Describe the parameters varied in capacitive displacement sensors and compare them with potentiometric sensors.
*   **Answer:**
    *   **Capacitive Sensors:** Measure position using the parallel-plate formula $C = \frac{\epsilon_0 \epsilon_r A}{d}$ by varying:
        1.  *Separation ($d$):* Axial displacement of one plate. Extremely sensitive, used for sub-micron movements.
        2.  *Overlapping Area ($A$):* Lateral sliding displacement. Highly linear, used for larger strokes.
        3.  *Permittivity ($\epsilon_r$):* Moving a dielectric slab between plates (common for liquid level sensing).
    *   **Potentiometric Sensors:** A mechanical wiper slides along a resistive track, acting as a voltage divider:
        $$V_{out} = V_{ref} \left( \frac{x}{L} \right)$$
    *   **Comparison:**
        *   *Capacitive:* Non-contact (no mechanical wear), infinite resolution, high sensitivity, but vulnerable to stray capacitances and noise.
        *   *Potentiometric:* Contact-based (prone to mechanical friction/wear), simple circuit design, high voltage output, low cost, but susceptible to dust/vibration.

