# Quick Revision: PE-EC801B - Fiber Optic Communication

This high-density revision sheet compiles core definitions, mathematical formulas, essential diagrams to practice drawing, frequently asked exam questions, and fast-recall points across all 6 units of the syllabus.

---

## 📋 Important Definitions

### Unit I: Introduction
*   **Snell's Law:** A law stating that the ratio of the sines of the angles of incidence and refraction is equal to the ratio of velocities in the two media, or equivalently, the product of the refractive index and the sine of the angle is constant: $n_1 \sin \theta_1 = n_2 \sin \theta_2$.
*   **Critical Angle ($\theta_c$):** The minimum angle of incidence at the core-cladding boundary above which total internal reflection (TIR) occurs, defined as $\theta_c = \sin^{-1}(n_2/n_1)$.
*   **Acceptance Angle ($\theta_a$):** The maximum angle at which a ray of light entering the fiber core from air will be guided by total internal reflection along the fiber.
*   **Numerical Aperture (NA):** A dimensionless parameter measuring the light-gathering ability of the fiber, defined as the sine of the acceptance angle: $\text{NA} = \sin \theta_a = \sqrt{n_1^2 - n_2^2}$.
*   **Meridional Rays:** Rays of light that pass through the longitudinal axis of the fiber core, remaining within a single plane.
*   **Skew Rays:** Rays that propagate through the fiber core without crossing the fiber's central longitudinal axis, following a helical path.

### Unit II: Optical Fibers
*   **Normalized Frequency ($V$-number):** A dimensionless parameter that determines the number of guided modes a fiber can support: $V = \frac{2\pi a}{\lambda} \text{NA}$.
*   **Cutoff Wavelength ($\lambda_c$):** The minimum wavelength at which a single-mode fiber supports only the fundamental mode ($\text{LP}_{01}$), defined under the condition $V = 2.405$.
*   **Mode-Field Diameter (MFD):** A measure of the radial distribution of optical power in the fundamental mode of a single-mode fiber, representing the width where the intensity drops to $1/e^2$ of its peak.
*   **Step-Index Fiber:** A fiber with a constant refractive index in the core and a sudden decrease (step) at the core-cladding boundary.
*   **Graded-Index Fiber:** A fiber with a core refractive index that decreases continuously and parabolically from the center axis out to the cladding boundary.

### Unit III: Signal Degradation
*   **Attenuation:** The reduction in optical power of a signal as it propagates through a fiber, measured in $\text{dB/km}$.
*   **Dispersion:** The temporal broadening of an optical pulse as it travels along a fiber, limiting the transmission bandwidth.
*   **Intermodal Dispersion:** Pulse broadening in multimode fibers caused by different modes traveling at different group velocities, arriving at different times.
*   **Intramodal (Chromatic) Dispersion:** Pulse broadening within a single mode caused by different wavelength components traveling at different speeds, consisting of material and waveguide dispersion.
*   **Optical Time Domain Reflectometer (OTDR):** An instrument that injects high-power optical pulses into a fiber and measures the backscattered and reflected light (Rayleigh scattering and Fresnel reflection) to locate faults and measure attenuation.
*   **GRIN-rod Lens:** A compact graded-index glass cylinder where the refractive index decreases parabolically from the central axis, used for collimating or focusing light.
*   **Expanded-Beam Connector:** A fiber connector that uses lenses to expand and collimate the exiting beam across an air gap, reducing lateral alignment sensitivity.


### Unit IV: Optical Sources & Detectors
*   **Population Inversion:** A state in a laser medium where more electrons reside in a higher, excited energy state than in a lower, ground state, enabling net optical amplification.
*   **Threshold Gain ($g_{th}$):** The minimum gain required in a laser cavity to balance the internal and mirror reflection losses, allowing laser oscillation to begin.
*   **Responsivity ($R$):** The ratio of generated photocurrent to the incident optical power in a photodetector, measured in $\text{A/W}$.
*   **Quantum Efficiency ($\eta$):** The ratio of the number of electron-hole pairs collected at the terminals of a photodetector to the number of incident photons.
*   **Avalanche Photodiode (APD):** A highly sensitive photodetector that uses impact ionization under high reverse bias to provide internal current gain through avalanche multiplication.
*   **Isotype & Anisotype Heterojunctions:** Isotype is a junction between two different materials of the same conductivity type (e.g. n-N). Anisotype is between different conductivity types (e.g. p-N).
*   **Radiative Minority Carrier Lifetime ($\tau_r$):** The average time an injected minority carrier survives in a band before undergoing radiative recombination.


### Unit V: Optical Switches & Amplifiers
*   **Erbium-Doped Fiber Amplifier (EDFA):** A lumped optical amplifier that uses Erbium ions embedded in a silica core, pumped at $980\text{ nm}$ or $1480\text{ nm}$, to amplify signals directly in the $1550\text{ nm}$ window.
*   **Raman Amplifier:** An amplifier that exploits Stimulated Raman Scattering (SRS) in the transmission fiber to transfer energy from high-power pump lasers to signal wavelengths distributed along the link.
*   **Coupling Length ($L_c$):** The physical length of a directional coupler required for $100\%$ of the optical power to transfer from the launch waveguide to the parallel waveguide.
*   **Wavelength Division Multiplexing (WDM):** The technique of combining multiple optical carrier signals of different wavelengths onto a single optical fiber to increase data capacity.

### Unit VI: Nonlinear Effects
*   **Kerr Effect:** The phenomenon where the refractive index of a medium changes in proportion to the local optical intensity of the propagating light: $n(I) = n_0 + n_2 I$.
*   **Self-Phase Modulation (SPM):** A nonlinear phase shift induced on an optical pulse by its own intensity envelope, leading to spectral broadening.
*   **Four-Wave Mixing (FWM):** A parametric nonlinear process where three waves of different frequencies beat together to generate new intermodulation sidebands.
*   **Optical Soliton:** A stable optical pulse that propagates over long distances without changing its shape, achieved by balancing anomalous Group Velocity Dispersion (GVD) and Self-Phase Modulation (SPM).

---

## 🧮 Key Formulas

### 1. Numerical Aperture (NA) & Acceptance Angle
$$\text{NA} = \sin \theta_a = \sqrt{n_1^2 - n_2^2} \approx n_1 \sqrt{2\Delta}$$
$$\Delta = \frac{n_1 - n_2}{n_1}$$
*   Where:
    *   $\theta_a$ = Acceptance angle in air
    *   $n_1$ = Core refractive index
    *   $n_2$ = Cladding refractive index
    *   $\Delta$ = Relative refractive index difference
*   *Numerical Example:* Given $n_1 = 1.48$ and $n_2 = 1.46$:
    $$\Delta = \frac{1.48 - 1.46}{1.48} \approx 0.0135$$
    $$\text{NA} = \sqrt{1.48^2 - 1.46^2} = \sqrt{2.1904 - 2.1316} \approx \mathbf{0.242}$$
    $$\theta_a = \sin^{-1}(0.242) \approx \mathbf{14.0^\circ}$$

### 2. Normalized Frequency ($V$-number) & Mode Count ($N$)
$$V = \frac{2\pi a}{\lambda} \text{NA}$$
$$N_{\text{step}} \approx \frac{V^2}{2} \quad \text{and} \quad N_{\text{graded}} \approx \frac{V^2}{4}$$
*   Where:
    *   $a$ = Core radius
    *   $\lambda$ = Operating wavelength
    *   $N_{\text{step}}, N_{\text{graded}}$ = Total number of guided modes
*   *Numerical Example:* A step-index fiber with core diameter $80\ \mu\text{m}$ ($a = 40\ \mu\text{m}$), $\text{NA} = 0.2$, operating at $\lambda = 0.85\ \mu\text{m}$:
    $$V = \frac{2\pi \times 40}{0.85} \times 0.2 \approx \mathbf{59.14}$$
    $$N_{\text{step}} \approx \frac{59.14^2}{2} \approx \mathbf{1749 \text{ modes}}$$

### 3. Cutoff Wavelength ($\lambda_c$) for Single-Mode Fiber
$$\lambda_c = \frac{2\pi a \text{NA}}{V_c} = \frac{2\pi a \text{NA}}{2.405}$$
*   Where:
    *   $V_c = 2.405$ is the single-mode cutoff limit.
*   *Numerical Example:* For core radius $a = 4.5\ \mu\text{m}$ and $\text{NA} = 0.12$:
    $$\lambda_c = \frac{2\pi \times 4.5 \times 0.12}{2.405} \approx \mathbf{1.409\ \mu\text{m}} = \mathbf{1409\text{ nm}}$$

### 4. Attenuation Coefficient ($\alpha$)
$$\alpha_{\text{dB/km}} = \frac{10}{L} \log_{10}\left(\frac{P_{\text{in}}}{P_{\text{out}}}\right)$$
*   Where:
    *   $L$ = Fiber link length in $\text{km}$
    *   $P_{\text{in}}$ = Optical power launched at input
    *   $P_{\text{out}}$ = Optical power measured at output

### 5. Multimode Intermodal Delay ($\Delta\tau$) & RMS Broadening ($\sigma_{\text{inter}}$)
$$\Delta\tau = \frac{L n_1 \Delta}{c} \quad \text{and} \quad \sigma_{\text{inter}} \approx \frac{L n_1 \Delta}{2\sqrt{3}c}$$
*   Where:
    *   $c$ = Speed of light in vacuum ($\approx 3 \times 10^5\text{ km/s}$)
    *   $\Delta\tau$ = Total delay difference between fastest and slowest modes.

### 6. Photodetector Responsivity ($R$) & Quantum Efficiency ($\eta$)
$$R = \frac{\eta q}{h \nu} = \frac{\eta q \lambda}{h c} \approx \frac{\eta \lambda}{1.24}$$
*   Where:
    *   $q$ = Electron charge ($1.6 \times 10^{-19}\ \text{C}$)
    *   $h$ = Planck's constant ($6.626 \times 10^{-34}\ \text{J}\cdot\text{s}$)
    *   $\lambda$ = Wavelength in $\mu\text{m}$
*   *Numerical Example:* A photodiode operating at $\lambda = 1.3\ \mu\text{m}$ with quantum efficiency $\eta = 70\%$ ($0.7$):
    $$R \approx \frac{0.7 \times 1.3}{1.24} \approx \mathbf{0.734\ \text{A/W}}$$

### 7. Laser Cavity Dynamics and Physics Equations
*   **Facet Reflectivity ($R$):**
    $$R = \left( \frac{n - 1}{n + 1} \right)^2$$
    *(where $n$ is refractive index of active semiconductor).*
*   **Longitudinal Mode Count ($m$):**
    $$m = \frac{2nL}{\lambda}$$
    *(where $L$ is cavity length and $\lambda$ is free-space wavelength).*
*   **Mode Frequency Separation ($\Delta f$):**
    $$\Delta f = \frac{c}{2nL}$$
*   **Mode Wavelength Separation ($\Delta \lambda$):**
    $$\Delta \lambda = \frac{\lambda^2 \Delta f}{c} = \frac{\lambda^2}{2nL}$$
*   **Radiative Minority Carrier Lifetime ($\tau_r$):**
    $$\tau_r = \frac{1}{B \cdot p_0}$$
    *(where $B$ is recombination coefficient and $p_0$ is majority carrier hole concentration).*


### 7. Rise-Time Budget for Digital Links
$$t_{\text{sys}} = \sqrt{t_{\text{tx}}^2 + t_{\text{disp}}^2 + t_{\text{rx}}^2} \le 0.7 T \quad (\text{for NRZ coding})$$
*   Where:
    *   $t_{\text{sys}}$ = Total system rise-time.
    *   $t_{\text{tx}}, t_{\text{rx}}$ = Transmitter and receiver electrical rise-times.
    *   $t_{\text{disp}}$ = Fiber dispersion rise-time (chromatic + modal).
    *   $T$ = Bit period ($1/\text{BitRate}$).

### 8. Directional Coupler Power Equations
$$P_1(z) = P_0 \cos^2(\kappa z) \quad \text{and} \quad P_2(z) = P_0 \sin^2(\kappa z)$$
$$L_c = \frac{\pi}{2\kappa}$$
*   Where:
    *   $\kappa$ = Evanescent coupling coefficient
    *   $L_c$ = Coupling length

### 9. Soliton Peak Power ($P_0$)
$$P_0 = \frac{|\beta_2|}{\gamma T_0^2}$$
*   Where:
    *   $\beta_2$ = Group Velocity Dispersion (GVD) parameter ($\text{s}^2/\text{m}$)
    *   $\gamma$ = Fiber nonlinearity coefficient ($\text{W}^{-1}\text{km}^{-1}$)
    *   $T_0$ = Half-width (pulse duration parameter) of the soliton

---

## 🎨 Diagrams to Practice Drawing

Prepare to sketch these block architectures, ray paths, and schematic layouts by hand for long-form answers:

### 1. General & Fiber-Optic Communication Systems (Unit I)
Detailed comparison of general electronic vs. photonic transmission pipelines.  
![General & Fiber-Optic Communication System](../Images/chapter_01/fiber_comm_block.png)

### 2. Ray Propagation & Numerical Aperture (Unit I)
Ray paths at the core-cladding boundary showing refraction, critical angle, and acceptance cone.  
![Ray Propagation & Angles](../Images/chapter_01/ray_propagation.png)

### 3. Attenuation Curve & Transmission Windows (Unit III)
Wavelength dependent attenuation showing Rayleigh scattering, infrared absorption, and the $1310/1550\text{ nm}$ windows.  
![Attenuation Curve & Transmission Windows](../Images/chapter_03/attenuation_curve.png)

### 4. Multimode vs. Single-Mode Pulse Broadening (Unit III)
Illustration of how multiple paths lead to dispersion and overlapping output pulses.  
![Pulse Broadening](../Images/chapter_03/pulse_broadening.png)

### 5. OTDR Configuration & Trace (Unit III)
OTDR optical splitter block diagram and the corresponding backscatter log trace identifying splices, faults, and reflection peaks.  
![OTDR block diagram](../Images/chapter_03/otdr_block.png)
![OTDR trace](../Images/chapter_03/otdr_trace.png)

### 6. Laser Resonator Cavity (Unit IV)
Double-heterostructure gain medium with cleaved mirror end-facets highlighting optical feedback.  
![Laser Cavity structure](../Images/chapter_04/laser_cavity.png)

### 7. Digital Optical Receiver Pipeline (Unit IV)
Block diagram tracking signal from photodiode through pre-amplifier, filter, and decision circuit.  
![Optical Receiver structure](../Images/chapter_04/optical_receiver.png)

### 8. EDFA Physical Layout (Unit V)
Optical configuration detailing Erbium spool, pump laser, WDM coupler, and input/output isolators.  
![EDFA Block diagram](../Images/chapter_05/edfa_block.png)

### 9. Directional Coupler States (Unit V)
Layout showing coupling paths for Cross State (zero volts) and Bar State (voltage applied).  
![Directional Coupler Switch States](../Images/chapter_05/directional_coupler.png)

### 10. MZI Optical Switch Layout (Unit V)
Y-splitter arms with deposited metal electrodes creating phase difference via electro-optic index shift.  
![MZI Switch Layout](../Images/chapter_05/mzi_switch.png)

### 11. OADM and OXC Routing Architectures (Unit V)
Wavelength drop/add filters and cross-connect fiber routing tables.  
![OADM Architecture](../Images/chapter_05/oadm_block.png)
![OXC Wavelength Routing](../Images/chapter_05/oxc_routing.png)

### 12. SRS vs. SBS Scattering Processes (Unit VI)
Energy transition flowcharts comparing optical molecular phonons (SRS) vs. acoustic density wave phonons (SBS).  
![SRS vs. SBS scattering](../Images/chapter_06/srs_vs_sbs.png)

### 13. SPM Pulse Chirping (Unit VI)
Envelope index changes mapping leading edge red shifts and trailing edge blue shifts.  
![SPM frequency chirping](../Images/chapter_06/spm_chirp.png)

### 14. Soliton Envelope Balance (Unit VI)
Interaction curve showing anomalous GVD compression exactly counteracting SPM broadening.  
![Soliton propagation balance](../Images/chapter_06/soliton_balance.png)

---

## ❓ Frequently Asked Questions

### Q1. Derive the expression for Acceptance Angle and Numerical Aperture (NA) of a multimode step-index fiber. [10M]
*   **Step 1:** Consider a ray of light entering the fiber core from a medium of refractive index $n_0$ (air, $n_0 = 1$) at an angle $\theta_0$ to the fiber axis.
*   **Step 2:** Apply Snell's Law at the air-core interface:
    $$n_0 \sin \theta_0 = n_1 \sin \theta_1$$
*   **Step 3:** The refracted ray strikes the core-cladding boundary at an angle of incidence $\phi$. For total internal reflection to occur, $\phi \ge \theta_c$. From geometry:
    $$\theta_1 = 90^\circ - \phi \implies \sin \theta_1 = \cos \phi$$
*   **Step 4:** Substitute this into Snell's Law:
    $$n_0 \sin \theta_0 = n_1 \cos \phi = n_1 \sqrt{1 - \sin^2 \phi}$$
*   **Step 5:** Under critical conditions, $\sin \phi = \sin \theta_c = n_2/n_1$. Substituting this yields:
    $$n_0 \sin \theta_a = n_1 \sqrt{1 - \left(\frac{n_2}{n_1}\right)^2} = \sqrt{n_1^2 - n_2^2}$$
*   **Step 6:** Setting $n_0 = 1$ for air, we get the final expression for NA:
    $$\text{NA} = \sin \theta_a = \sqrt{n_1^2 - n_2^2}$$

### Q2. Compare step-index and graded-index fibers in terms of profiles, ray paths, and intermodal dispersion. [5M]
*   **Refractive Index Profile:** Step-index has a constant index $n_1$ in the core with a step decrease at the cladding. Graded-index has a parabolic index profile decreasing from the core axis outward.
*   **Ray Propagation Path:** Light travels in zig-zag straight lines in step-index cores. In graded-index cores, rays bend continuously in sinusoidal, helical paths.
*   **Intermodal Dispersion:** High in step-index fibers because rays traveling at larger angles take longer paths. Low in graded-index fibers because rays traveling on longer outer paths travel faster (where refractive index is lower), keeping arrival times synchronized.

### Q3. Derive the intermodal delay difference ($\Delta\tau$) in a step-index fiber. [10M]
*   **Fastest Ray:** Propagates along the central longitudinal axis of length $L$. Travel time is:
    $$t_{\text{min}} = \frac{L}{v} = \frac{L n_1}{c}$$
*   **Slowest Ray:** Travels at the critical angle $\theta_c$, reflecting repeatedly. Path length is $L/\sin \theta_c = L(n_1/n_2)$. Travel time is:
    $$t_{\text{max}} = \frac{L (n_1/n_2)}{v} = \frac{L n_1^2}{c n_2}$$
*   **Delay Difference ($\Delta\tau$):**
    $$\Delta\tau = t_{\text{max}} - t_{\text{min}} = \frac{L n_1}{c} \left(\frac{n_1}{n_2} - 1\right) = \frac{L n_1}{c} \left(\frac{n_1 - n_2}{n_2}\right)$$
*   Since $n_2 \approx n_1$ for weakly guiding fibers:
    $$\Delta\tau \approx \frac{L n_1 \Delta}{c}$$

### Q4. Detail the differences between PIN photodiodes and Avalanche Photodiodes (APDs). [5M]
*   **Structure:** PIN photodiode has a standard Intrinsic semiconductor layer between P and N regions. APD has an additional high-field multiplication region.
*   **Gain Mechanism:** PIN photodiodes have no internal gain (one electron per photon, $M=1$). APDs provide internal gain ($M = 10 \text{ to } 100$) through avalanche multiplication.
*   **Responsivity:** PIN responsibility is lower ($\approx 0.6 \text{ to } 0.8\ \text{A/W}$). APD responsivity is much higher due to multiplication factor $M$.
*   **Noise & Bias:** PIN photodiodes require low reverse bias voltage ($5 \text{ to } 15\ \text{V}$) and generate low noise. APDs require very high reverse bias voltage ($100 \text{ to } 300\ \text{V}$) and introduce excess avalanche noise.

### Q5. Differentiate between Erbium-Doped Fiber Amplifiers (EDFA) and Raman Amplifiers. [5M]
*   **Gain Medium:** EDFA uses a short, lumped section of silica fiber heavily doped with Erbium ions. Raman amplification uses the standard long transmission fiber itself (distributed gain).
*   **Amplification Principle:** EDFA uses stimulated emission from excited Erbium ions. Raman uses Stimulated Raman Scattering (SRS) where high-power pump photons transfer energy to signal photons.
*   **Operating Band:** EDFA is restricted to the fixed C-band ($1530 \text{ to } 1565\text{ nm}$) and L-band ($1565 \text{ to } 1625\text{ nm}$). Raman amplifiers can operate at any wavelength by tuning the pump laser frequency.
*   **Pump Power:** EDFAs require moderate pump powers ($10 \text{ to } 100\ \text{mW}$). Raman amplifiers require very high pump powers ($> 500\ \text{mW}$).

### Q6. Explain how optical solitons propagate without broadening in a fiber. [10M]
*   **The Problem:** Normal pulse propagation suffers from Group Velocity Dispersion (GVD), which spreads different frequency components temporally, causing pulse broadening.
*   **Anomalous GVD:** At wavelengths $>1310\text{ nm}$ in standard fiber, GVD is anomalous ($D > 0$), meaning higher-frequency (blue) components travel faster than lower-frequency (red) components, creating a GVD chirp (blue leading, red trailing).
*   **SPM Effect:** Due to the intensity-dependent Kerr effect, Self-Phase Modulation (SPM) creates a nonlinear phase shift that shifts the leading edge to lower frequencies (red shift) and the trailing edge to higher frequencies (blue shift).
*   **The Balance:** Because the chirps introduced by anomalous GVD and SPM are equal and opposite, they cancel each other out. The optical pulse propagates as a fundamental soliton ($N=1$), preserving its shape indefinitely.

---

## ⚡ One-Line Revision Bullets

*   **Unit I:** Total internal reflection requires light to travel from a denser core ($n_1$) to a rarer cladding ($n_2$) at an angle greater than the critical angle $\theta_c$.
*   **Unit II:** Single-mode propagation in a step-index fiber is achieved only when the normalized frequency $V < 2.405$.
*   **Unit III:** Intramodal dispersion consists of material dispersion (wavelength-dependent index) and waveguide dispersion (wavelength-dependent boundary guidance), and it dominates in single-mode links.
*   **Unit IV:** Laser diodes rely on optical feedback in a resonator cavity to achieve stimulated emission, whereas LEDs rely on spontaneous emission.
*   **Unit V:** Mach-Zehnder Interferometers act as high-speed optical switches by applying voltage across electrodes to induce a $\pi$ phase difference between interferometer arms.
*   **Unit VI:** Four-Wave Mixing generates severe crosstalk in WDM systems, which is mitigated by introducing local chromatic dispersion (NZ-DSF) to break phase-matching.
