# Flashcards: Unit I - Introduction to Optical Fiber Communication

These active recall Question-and-Answer cards are designed to test your memory on the system block diagrams, refraction principles, Numerical Aperture derivations, meridional vs. skew rays, and waveguide propagation of Unit I.

---

### 🎴 Card 1: Fiber Optic Communication System Blocks
*   **Question:** What are the seven key components of a fiber optic communication link in sequential order?
*   **Answer:**
    1.  **Information Source & Electrical Transmitter:** Source message generated and coded/multiplexed.
    2.  **Drive Circuit:** Modulates the input electrical signal into drive current.
    3.  **Optical Source:** Converts electrical signals to light waves (LED or Laser).
    4.  **Optical Fiber Cable (Channel):** Waveguide that guides light pulses via Total Internal Reflection.
    5.  **Optical Detector (Photodetector):** Converts light back to current (PIN or APD).
    6.  **Electrical Receiver:** Amplifies, filters, and demodulates the signal.
    7.  **Destination:** Recipient device.

---

### 🎴 Card 2: Advantages of Optical Fibers
*   **Question:** State four major advantages of using optical fibers over copper cables.
*   **Answer:**
    1.  **Enormous Bandwidth:** Terahertz carrier frequencies provide huge data capacity.
    2.  **Low Attenuation:** Losses as low as $0.2\ \text{dB/km}$ allow long spans without repeaters.
    3.  **EMI Immunity:** Dielectric (glass/plastic) cables are immune to electrical noise and lightning.
    4.  **High Security & No Crosstalk:** Confines light, making physical tapping difficult and removing crosstalk.

---

### 🎴 Card 3: Critical Angle and TIR
*   **Question:** Write the equation for the Critical Angle ($\theta_c$) and list the two conditions required for Total Internal Reflection (TIR) to occur.
*   **Answer:**
    *   **Equation:** $\theta_c = \sin^{-1}\left(\frac{n_2}{n_1}\right)$
    *   **TIR Conditions:**
        1.  Light must travel from a denser medium ($n_1$) to a rarer medium ($n_2$) ($n_1 > n_2$).
        2.  The angle of incidence at the interface must exceed the critical angle ($\theta_i > \theta_c$).

---

### 🎴 Card 4: Numerical Aperture (NA) Definition & Formula
*   **Question:** Define Numerical Aperture (NA) and state its formula in terms of (a) core/cladding indices ($n_1, n_2$), and (b) relative refractive index difference ($\Delta$).
*   **Answer:**
    *   **Definition:** The sine of the acceptance angle in air ($\text{NA} = \sin(\theta_a)$), representing the light-gathering capacity of the fiber.
    *   **Formulas:**
        *   **(a)** $\text{NA} = \sqrt{n_1^2 - n_2^2}$
        *   **(b)** $\text{NA} = n_1 \sqrt{2 \Delta}$ (where $\Delta \approx \frac{n_1 - n_2}{n_1}$)

---

### 🎴 Card 5: Relative Refractive Index Difference ($\Delta$)
*   **Question:** Write the exact and approximate expressions for the relative refractive index difference ($\Delta$).
*   **Answer:**
    *   **Exact:** $\Delta = \frac{n_1^2 - n_2^2}{2 n_1^2}$
    *   **Approximation:** $\Delta \approx \frac{n_1 - n_2}{n_1}$

---

### 🎴 Card 6: Meridional vs. Skew Rays
*   **Question:** What is the fundamental difference in the propagation path between Meridional and Skew rays?
*   **Answer:**
    *   **Meridional Rays:** Pass through the fiber's longitudinal central axis during every reflection, propagating in a single plane.
    *   **Skew Rays:** Do not pass through the central axis; instead, they follow a helical or spiral trajectory along the boundaries of the core.

---

### 🎴 Card 7: Ray Model vs. Wave Model
*   **Question:** Under what conditions do we use the Ray Model, and when is the Wave Model required?
*   **Answer:**
    *   **Ray Model (Geometric Optics):** Valid when the core diameter ($d$) is much larger than the optical wavelength ($\lambda$) ($d \gg \lambda$). Typically used for Multimode Fibers.
    *   **Wave Model (Waveguide Theory):** Required when the core diameter ($d$) is comparable to the wavelength ($\lambda$) ($d \approx \lambda$). Mandatory for Single-Mode Fibers to describe wave interference and modal cutoff.

---

### 🎴 Card 8: Propagation Modes in Cylindrical Dielectric Rods
*   **Question:** Why do hybrid modes (HE/EH) propagate in optical fibers, and how do they differ from TE and TM modes?
*   **Answer:**
    *   Because of the vector boundary conditions at the curved core-cladding interface.
    *   **TE Modes:** Transverse Electric ($E_z = 0$, $H_z \neq 0$).
    *   **TM Modes:** Transverse Magnetic ($H_z = 0$, $E_z \neq 0$).
    *   **Hybrid (HE/EH) Modes:** Both $E_z \neq 0$ and $H_z \neq 0$. They represent waves propagating along helical skew ray paths.
