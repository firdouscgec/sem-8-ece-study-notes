# Flashcards: Unit IV - Advanced Control Techniques

These active recall Question-and-Answer cards are designed to test your memory on the feedforward, cascade, ratio, override, split-range, adaptive, and internal model control schemes of Unit IV.

---

### 🎴 Card 1: Feed-Forward Control Principle
*   **Question:** What is the core operating principle of Feed-Forward control?
*   **Answer:** Feed-forward control is an **anticipatory (proactive)** control strategy. It measures the major process load disturbances ($d(t)$) *before* they enter the process, calculates the exact correction required to offset the disturbance, and adjusts the manipulated variable ($m(t)$) immediately to keep the process variable ($y(t)$) at the setpoint without waiting for an error to develop.

---

### 🎴 Card 2: Feed-Forward vs. Feedback Control
*   **Question:** Compare Feed-Forward and Feedback control regarding speed and stability.
*   **Answer:**
    *   **Feedback Control:** 
        *   *Action:* Reactive (acts only *after* error occurs).
        *   *Speed:* Slower.
        *   *Stability:* Can cause loop instability/oscillations if gain is high.
        *   *Advantage:* Compensates for all disturbances, even unmeasured ones.
    *   **Feed-Forward Control:**
        *   *Action:* Proactive (acts before error occurs).
        *   *Speed:* Faster.
        *   *Stability:* Inherently stable (operates open-loop relative to process output).
        *   *Disadvantage:* Only compensates for measured disturbances; requires an accurate process model.

---

### 🎴 Card 3: Cascade Control Architecture
*   **Question:** Describe the loop structure and controller roles in a Cascade Control system.
*   **Answer:**
    *   **Structure:** Comprises two nested feedback loops: a primary (outer) loop and a secondary (inner) loop.
    *   **Controllers:** 
        *   **Primary (Master) Controller:** Measures the primary output variable (e.g. reactor temperature) and calculates the setpoint for the secondary controller.
        *   **Secondary (Slave) Controller:** Measures a secondary intermediate variable (e.g. jacket coolant flow rate) and directly drives the control valve.

---

### 🎴 Card 4: Cascade Control Advantages
*   **Question:** Why is Cascade control highly effective at rejecting disturbances inside the secondary loop?
*   **Answer:** Disturbances arising inside the inner loop (e.g. coolant pressure fluctuations) are detected and corrected by the fast secondary slave controller *before* they can affect the primary process variable (reactor temperature). This isolates the slow primary outer loop from secondary-path disturbances.

---

### 🎴 Card 5: Ratio Control
*   **Question:** What is Ratio control, and what are "wild flow" and "controlled flow"?
*   **Answer:**
    *   **Ratio Control:** A control scheme designed to maintain the flow rate of one stream in a fixed, constant proportion to the flow rate of another stream (e.g., maintaining a precise air-to-fuel ratio in a combustion furnace).
    *   **Wild Flow ($F_{wild}$):** The uncontrolled stream whose flow rate fluctuates freely.
    *   **Controlled Flow ($F_{controlled}$):** The manipulated stream adjusted by the controller to match the target ratio: $F_{controlled} = R \times F_{wild}$.

---

### 🎴 Card 6: Override (Selective) Control
*   **Question:** Explain the principle of Override control.
*   **Answer:** It is a protective control scheme where a single manipulated variable is shared between a normal process controller and a safety/constraint controller. A **High Selector (HS)** or **Low Selector (LS)** chooses which controller command passes to the valve. During normal operation, the main controller runs the process, but if a safety limit is approached, the safety controller "overrides" control to protect the equipment.

---

### 🎴 Card 7: Split-Range Control
*   **Question:** Define Split-Range control and give a practical example.
*   **Answer:**
    *   **Definition:** A control scheme where a single controller output signal is split to control two or more control valves operating in different ranges.
    *   **Example:** jacked reactor temperature control. A single temperature controller output (0-100%) is split:
        *   0% to 50% output opens the cooling water valve.
        *   50% to 100% output opens the steam heating valve.
        *   At exactly 50%, both valves are closed (dead band).

---

### 🎴 Card 8: Adaptive Control (STR vs. MRAC)
*   **Question:** What is Adaptive control? Compare Self-Tuning Regulators (STR) and Model Reference Adaptive Control (MRAC).
*   **Answer:**
    *   **Adaptive Control:** A control system that automatically adjusts its controller parameters (gain, reset time) in real-time to compensate for changes in process dynamics or parameters.
    *   **STR:** Explicitly estimates the process parameters online using recursive least squares, then recalculates/redesigns the controller parameters.
    *   **MRAC:** Uses a reference model that defines the desired process output response. The adjustment loop directly updates controller gains to minimize the error between the actual process output and the reference model output.

---

### 🎴 Card 9: Internal Model Control (IMC)
*   **Question:** Explain the basic concept and block diagram components of Internal Model Control.
*   **Answer:**
    *   **Concept:** IMC incorporates an explicit mathematical model of the process in parallel with the actual physical process.
    *   **Mechanism:** The controller output goes to both the process and the model. The model output is subtracted from the actual process output to yield a feedback signal representing unmodeled disturbances and model mismatch.
    *   **Design:** If the process model is exact, the feedback path is open, and perfect control is achieved by setting the controller to be the mathematical inverse of the process model.
