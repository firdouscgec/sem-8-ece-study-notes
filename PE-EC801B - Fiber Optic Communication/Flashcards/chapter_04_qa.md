# Flashcards: Unit IV - Optical Sources & Detectors

These active recall Question-and-Answer cards cover the comparison of LEDs and Laser Diodes, lasing threshold conditions, PIN and APD photodiodes, responsivity derivations, receiver noise mechanisms, link power budget design, rise-time budget analysis, and the quantum limit of detection.

---

### 🎴 Card 1: LED vs. Laser Diode
*   **Question:** Compare Light Emitting Diodes (LEDs) and Laser Diodes (LDs) in terms of emission process, spectral width, coupling efficiency, and coherence.
*   **Answer:**
    *   **LED:**
        *   *Emission:* Spontaneous emission (recombination of electron-hole pairs without external photon trigger).
        *   *Spectral Width:* Broad ($\Delta\lambda \approx 30 \text{ to } 50\ \text{nm}$), causing high material dispersion.
        *   *Coupling Efficiency:* Low (isotropic Lambertian output beam).
        *   *Coherence:* Incoherent.
    *   **Laser Diode:**
        *   *Emission:* Stimulated emission (excited carriers triggered by incident photons; requires population inversion and optical feedback).
        *   *Spectral Width:* Narrow ($\Delta\lambda < 1 \text{ to } 3\ \text{nm}$), enabling high-speed transmission.
        *   *Coupling Efficiency:* High (highly directional, narrow output beam).
        *   *Coherence:* Coherent.

---

### 🎴 Card 2: Population Inversion & Lasing Threshold
*   **Question:** Define population inversion, and write the mathematical condition for the threshold gain ($g_{th}$) in a Fabry-Perot cavity laser.
*   **Answer:**
    *   **Population Inversion:** A non-equilibrium state where the number of electrons in the higher energy level (conduction band) exceeds the number in the lower energy level (valence band), causing stimulated emission to dominate over absorption.
    *   **Threshold Gain Formula:**
        $$g_{th} = \alpha_t + \frac{1}{2L} \ln\left(\frac{1}{R_1 R_2}\right)$$
    *   *Parameters:* $\alpha_t$ is the medium absorption and scattering loss coefficient, $L$ is the cavity length, and $R_1, R_2$ are the reflectivities of the cavity facets.

---

### 🎴 Card 3: PIN vs. APD Photodetector
*   **Question:** Compare PIN photodiodes and Avalanche Photodiodes (APDs) in terms of structures, gain, and operating voltages.
*   **Answer:**
    *   **PIN Photodiode:**
        *   *Structure:* P-type and N-type semiconductor layers separated by a lightly-doped intrinsic (I) region.
        *   *Gain:* No internal gain ($M = 1$).
        *   *Operating Voltage:* Low reverse bias ($\approx 5 \text{ to } 15\ \text{V}$).
        *   *Noise:* Low noise, stable over temperature.
    *   **Avalanche Photodiode (APD):**
        *   *Structure:* P-I-N structure with an additional high-field multiplication region.
        *   *Gain:* High internal gain ($M \approx 50 \text{ to } 100$) via carrier multiplication by *impact ionization*.
        *   *Operating Voltage:* High reverse bias ($\approx 100 \text{ to } 300\ \text{V}$).
        *   *Noise:* Higher noise due to random carrier multiplication (multiplication noise).

---

### 🎴 Card 4: Quantum Efficiency & Responsivity
*   **Question:** Define Quantum Efficiency ($\eta$) and Responsivity ($R$), and write the formula relating them.
*   **Answer:**
    *   **Quantum Efficiency ($\eta$):** The fraction of incident photons that generate electron-hole pairs collected at the device terminals:
        $$\eta = \frac{\text{Number of electron-hole pairs collected}}{\text{Number of incident photons}} = \frac{I_p / e}{P_{in} / h\nu}$$
    *   **Responsivity ($R$):** The ratio of output photocurrent ($I_p$) to the incident optical power ($P_{in}$):
        $$R = \frac{I_p}{P_{in}} = \frac{\eta e}{h\nu} = \frac{\eta e \lambda}{hc} \approx \frac{\eta \lambda(\mu\text{m})}{1.24}\ \text{A/W}$$
    *   *Parameters:* $e$ is electron charge, $h$ is Planck's constant, $\nu$ is optical frequency, $\lambda$ is wavelength, and $c$ is speed of light.

---

### 🎴 Card 5: Detector Materials & the $1550\text{ nm}$ Window
*   **Question:** Why is Silicon (Si) unsuitable for the $1550\text{ nm}$ window, and what materials are preferred?
*   **Answer:**
    *   **Silicon Unsuitability:** Silicon has a bandgap of $E_g \approx 1.1\ \text{eV}$, which corresponds to a cutoff wavelength of $\lambda_c = hc/E_g \approx 1.1\ \mu\text{m}$. Light at $1550\text{ nm}$ ($E \approx 0.8\ \text{eV}$) has insufficient photon energy to excite electrons across Silicon's bandgap, making Si transparent at this wavelength.
    *   **Preferred Materials:** **Indium Gallium Arsenide (InGaAs)** or **Germanium (Ge)**. InGaAs has a narrower bandgap ($E_g \approx 0.73\ \text{eV}$), corresponding to $\lambda_c \approx 1.7\ \mu\text{m}$, allowing it to achieve high absorption and responsivity in both the $1310\text{ nm}$ and $1550\text{ nm}$ windows.

---

### 🎴 Card 6: Noise in Optical Receivers
*   **Question:** What are the three primary sources of noise in a digital optical receiver?
*   **Answer:**
    1.  **Shot Noise:** Caused by the random, quantum arrival of photons and thermal generation of dark current. It is signal-dependent and amplified by the photodetector gain ($M$):
        $$\langle i_{shot}^2 \rangle = 2e(I_p + I_d)M^{2+x}B$$ (where $I_d$ is dark current, and $x$ is the APD excess noise factor).
    2.  **Thermal Noise (Johnson Noise):** Caused by the random thermal motion of electrons within the load resistor $R_L$ of the receiver:
        $$\langle i_{thermal}^2 \rangle = \frac{4 k_B T B}{R_L}$$
    3.  **Amplifier Noise:** Noise added by the active transistors in the receiver preamplifier stage, represented by the preamplifier noise figure.

---

### 🎴 Card 7: Link Power Budget
*   **Question:** Explain the purpose and state the mathematical equation of the Link Power Budget.
*   **Answer:**
    *   **Purpose:** To ensure that the transmitter launched optical power is sufficient to overcome all attenuation and connector/splice losses along the fiber path, delivering power to the receiver that exceeds its sensitivity limit with a safe safety margin.
    *   **Equation:**
        $$P_T - P_R = \alpha L + \alpha_{sp} N_{sp} + \alpha_c N_c + M_s$$
    *   *Parameters:* $P_T$ is source power ($\text{dBm}$), $P_R$ is receiver sensitivity ($\text{dBm}$), $\alpha$ is fiber attenuation ($\text{dB/km}$), $L$ is fiber length ($\text{km}$), $\alpha_{sp}$ is splice loss, $N_{sp}$ is number of splices, $\alpha_c$ is connector loss, $N_c$ is number of connectors, and $M_s$ is the system safety margin (typically $3 \text{ to } 6\ \text{dB}$).

---

### 🎴 Card 8: Rise-Time Budget
*   **Question:** Write the system rise-time ($t_{sys}$) formula and state the limit for a Non-Return-to-Zero (NRZ) digital system.
*   **Answer:**
    *   **System Rise-Time Formula:**
        $$t_{sys} = \left( t_{tx}^2 + t_{mat}^2 + t_{mod}^2 + t_{rx}^2 \right)^{1/2}$$
        where $t_{tx}$ is transmitter rise time, $t_{rx}$ is receiver rise time, $t_{mat}$ is material dispersion rise time, and $t_{mod}$ is modal dispersion rise time.
    *   **NRZ Limit:** To prevent inter-symbol interference and ensure the channel has sufficient bandwidth, the system rise-time must not exceed $70\%$ of the bit period $T$:
        $$t_{sys} \le 0.7 T = \frac{0.7}{B_T}$$ (where $B_T$ is the transmission bit rate).

---

### 🎴 Card 9: Quantum Limit of Detection
*   **Question:** What is the Quantum Limit of Detection, and how many photons are required for a BER of $10^{-9}$ in an ideal receiver?
*   **Answer:**
    *   **Definition:** The fundamental physical limit of receiver sensitivity assuming an ideal photodetector (quantum efficiency $\eta = 1$, zero dark current, and zero thermal noise), where errors occur solely due to the Poisson statistical fluctuations in photon arrival.
    *   **Derivation:** The probability of registering $0$ electrons when a pulse containing $N_p$ photons is sent is given by the Poisson distribution: $P(0) = e^{-N_p}$.
    *   To achieve a Bit Error Rate (BER) of $10^{-9}$, we set $P(0) \le 10^{-9}$:
        $$e^{-N_p} = 10^{-9} \implies N_p = \ln(10^9) \approx 20.7 \approx 21\text{ photons}$$
    *   *Result:* An average of **21 photons** per pulse is the absolute minimum required to achieve a $10^{-9}$ error rate.
