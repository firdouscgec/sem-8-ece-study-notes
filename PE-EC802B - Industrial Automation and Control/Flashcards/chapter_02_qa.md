# Flashcards: Unit II - Controller Tuning & PID

These active recall Question-and-Answer cards are designed to test your memory on proportional, integral, and derivative control actions, tuning methods (Ziegler-Nichols, Cohen-Coon), and PID implementation of Unit II.

---

### 🎴 Card 1: Proportional (P) Control Action
*   **Question:** Write the equation for a Proportional (P) controller and state its main disadvantage.
*   **Answer:**
    *   **Equation:** $p(t) = K_c e(t) + p_s$ (where $K_c$ is proportional gain, $e(t)$ is error, and $p_s$ is bias/steady-state output).
    *   **Disadvantage:** It cannot eliminate steady-state error (offset) when load changes occur.

---

### 🎴 Card 2: Integral (I) Control Action (Reset)
*   **Question:** Write the equation for an Integral (I) controller and state its main advantage and disadvantage.
*   **Answer:**
    *   **Equation:** $p(t) = \frac{1}{\tau_I} \int_0^t e(t^*) dt^* + p(0)$ (where $\tau_I$ is integral/reset time).
    *   **Advantage:** Completely eliminates steady-state offset ($e_{ss} = 0$).
    *   **Disadvantage:** Introduces a phase lag of $-90^\circ$, making the system more oscillatory, and is susceptible to **integral windup** during saturation.

---

### 🎴 Card 3: Derivative (D) Control Action (Rate)
*   **Question:** Write the equation for a Derivative (D) controller and state why it cannot be used alone.
*   **Answer:**
    *   **Equation:** $p(t) = \tau_D \frac{de(t)}{dt}$ (where $\tau_D$ is derivative/rate time).
    *   **Why not alone:** It acts only on the rate of change of error. If the error is constant (even if very large), the derivative output is zero. It has no sense of the current error value.

---

### 🎴 Card 4: Proportional Band vs Proportional Gain
*   **Question:** Define Proportional Band (PB) and write its mathematical relationship to Proportional Gain ($K_c$).
*   **Answer:**
    *   **Proportional Band:** The range of error input (expressed as a percentage of full range) required to drive the controller output through its full range (e.g. from 0% to 100%).
    *   **Equation:** $K_c = \frac{100}{PB}$ (Narrow band = High gain, Wide band = Low gain).

---

### 🎴 Card 5: Offset Definition
*   **Question:** What is "offset" in control systems, and why does Proportional-only control cause it?
*   **Answer:**
    *   **Offset:** The steady-state error between the process setpoint and the actual process variable ($e_{ss} = y_{sp} - y_{ss}$).
    *   **Cause in P-control:** To maintain a controller output different from the bias value ($p_s$) to match a new load demand, a non-zero error ($e(t)$) must persist in the equation $p(t) = K_c e(t) + p_s$.

---

### 🎴 Card 6: OP-AMP PI Controller Circuit
*   **Question:** How is an electronic PI controller implemented using an OP-AMP?
*   **Answer:**
    *   **Configuration:** The input path has resistor $R_1$. The feedback path contains a resistor $R_2$ in series with a capacitor $C$.
    *   **Parameters:** 
        *   Proportional Gain: $K_c = \frac{R_2}{R_1}$
        *   Integral Time Constant: $\tau_I = R_2 C$
        *   Transfer Function: $G_c(s) = -\frac{R_2}{R_1} \left(1 + \frac{1}{R_2 C s}\right)$

---

### 🎴 Card 7: OP-AMP PD Controller Circuit
*   **Question:** How is an electronic PD controller implemented using an OP-AMP?
*   **Answer:**
    *   **Configuration:** The input path has a resistor $R_1$ in parallel with a capacitor $C$. The feedback path contains resistor $R_2$.
    *   **Parameters:**
        *   Proportional Gain: $K_c = \frac{R_2}{R_1}$
        *   Derivative Time Constant: $\tau_D = R_1 C$
        *   Transfer Function: $G_c(s) = -\frac{R_2}{R_1} (1 + R_1 C s)$

---

### 🎴 Card 8: Ziegler-Nichols Closed-Loop Tuning
*   **Question:** Describe the steps for Ziegler-Nichols Closed-Loop (Continuous Oscillation) tuning.
*   **Answer:**
    1.  Deactivate Integral and Derivative modes (set $\tau_I = \infty$, $\tau_D = 0$).
    2.  Increase Proportional Gain ($K_c$) slowly while introducing setpoint changes until the process variable reaches sustained, constant-amplitude oscillations.
    3.  Record this gain as the **Ultimate Gain ($K_u$)** and the period of oscillation as the **Ultimate Period ($P_u$)**.
    4.  Calculate PID parameters using ZN formulas: $K_c = 0.6 K_u$, $\tau_I = 0.5 P_u$, $\tau_D = 0.125 P_u$.

---

### 🎴 Card 9: Ziegler-Nichols Open-Loop Tuning
*   **Question:** Explain the Ziegler-Nichols Open-Loop (Process Reaction Curve) method.
*   **Answer:**
    1.  Place the controller in manual mode and apply a step change of magnitude $\Delta M$ to the control valve.
    2.  Plot the process response. Identify the inflection point to draw a tangent line.
    3.  Extract the **Process Reaction Rate ($R$)** (slope of tangent) and the **Transport Lag ($L$)** (time delay from step start to tangent line intersection with time axis).
    4.  Calculate parameters: e.g. for P-control, $K_c = \frac{\Delta M}{R L}$.

---

### 🎴 Card 10: Cohen-Coon Tuning Rules
*   **Question:** When is the Cohen-Coon tuning method preferred over Ziegler-Nichols?
*   **Answer:** It is preferred for processes with **large dead-time-to-time-constant ratios** ($\frac{\theta}{\tau} > 0.5$), where Ziegler-Nichols rules tend to over-tune and cause unstable oscillations. Cohen-Coon takes self-regulation and time constant into account to achieve a $1/4$ decay ratio.

---

### 🎴 Card 11: Quarter-Amplitude Decay Ratio
*   **Question:** What does the "Quarter-Amplitude Decay Ratio" criterion specify?
*   **Answer:** A design target for controller tuning where the amplitude of each successive peak in a transient disturbance response is exactly one-quarter ($1/4$ or 25%) of the amplitude of the preceding peak. It represents a good trade-off between speed of response and stability.

---

### 🎴 Card 12: Servo vs. Regulatory Control
*   **Question:** Define Servo and Regulatory control objectives.
*   **Answer:**
    *   **Servo Control:** The objective is to force the process variable to track a dynamically changing setpoint ($y_{sp}(t)$) as closely and rapidly as possible ($y(t) \rightarrow y_{sp}(t)$).
    *   **Regulatory Control:** The setpoint is constant. The objective is to reject the effect of external load disturbances ($d(t)$) and maintain the process variable at the setpoint.

---

### 🎴 Card 13: Digital PID Algorithms
*   **Question:** Differentiate between Positional and Velocity algorithms in digital PID controllers.
*   **Answer:**
    *   **Positional Algorithm:** Computes the actual physical position of the control valve at each sampling step: $u(n) = K_c \left[ e(n) + \frac{\Delta t}{\tau_I} \sum e(i) + \frac{\tau_D}{\Delta t} (e(n) - e(n-1)) \right]$. Requires initialization to prevent bumps.
    *   **Velocity Algorithm:** Computes only the change in valve position at each step: $\Delta u(n) = u(n) - u(n-1)$. It is naturally immune to integral windup and easier to handle in manual-to-auto transfers.
