# Flashcards: Unit II - Optical Fibers & Waveguide Theory

These active recall Question-and-Answer cards are designed to test your memory on the classification of optical fibers, core-cladding boundary conditions, wave propagation parameters, and Bessel equations of Unit II.

---

### 🎴 Card 1: Step-Index vs. Graded-Index Refractive Index Profiles
*   **Question:** What are the mathematical refractive index profiles for Step-Index (SI) and Graded-Index (GI) fibers?
*   **Answer:**
    *   **Step-Index (SI):** Refractive index is constant in the core ($n_1$) and drops abruptly to cladding ($n_2$) at $r = a$:
        $$n(r) = \begin{cases} n_1 & \text{for } r < a \\ n_2 & \text{for } r \ge a \end{cases}$$
    *   **Graded-Index (GI):** Parabolic continuous index drop across the core:
        $$n(r) = n_1 \sqrt{1 - 2\Delta\left(\frac{r}{a}\right)^2} \quad \text{for } r < a$$

---

### 🎴 Card 2: Single-Mode vs. Multimode Core Sizes & Dispersion
*   **Question:** Compare Single-Mode Fiber (SMF) and Multimode Fiber (MMF) on core diameter and intermodal dispersion.
*   **Answer:**
    *   **SMF:** Core diameter is small ($8\text{--}10\ \mu\text{m}$); intermodal dispersion is zero since only one mode exists.
    *   **MMF:** Core diameter is large ($50\text{--}100\ \mu\text{m}$); intermodal dispersion is high because many modes propagate with different delay times.

---

### 🎴 Card 3: V-number Formula
*   **Question:** Write the equation for the Normalized Frequency (V-number) of a step-index fiber.
*   **Answer:**
    $$V = \frac{2\pi a}{\lambda}\text{NA} = \frac{2\pi a}{\lambda}\sqrt{n_1^2 - n_2^2}$$
    where $a$ is the core radius and $\lambda$ is the operating wavelength in free space.

---

### 🎴 Card 4: Single-Mode Cutoff Condition
*   **Question:** What is the maximum V-number threshold ($V_c$) for single-mode propagation in a step-index fiber?
*   **Answer:**
    $$V < 2.405$$
    Below $V = 2.405$, only the fundamental mode ($\text{HE}_{11}$) propagates.

---

### 🎴 Card 5: Number of Guided Modes ($N$)
*   **Question:** State the formulas for the total number of guided modes ($N$) in (a) Step-Index (SI), and (b) Graded-Index (GI) parabolic fibers.
*   **Answer:**
    *   **(a)** $N_{SI} \approx \frac{V^2}{2}$
    *   **(b)** $N_{GI} \approx \frac{V^2}{4}$

---

### 🎴 Card 6: Cutoff Wavelength ($\lambda_c$)
*   **Question:** Write the formula for the Cutoff Wavelength ($\lambda_c$) of a single-mode step-index fiber.
*   **Answer:**
    $$\lambda_c = \frac{2\pi a \text{NA}}{2.405} = \frac{2\pi a \sqrt{n_1^2 - n_2^2}}{2.405}$$
    Above $\lambda_c$, the fiber operates in single-mode; below it, higher-order modes propagate.

---

### 🎴 Card 7: Mode-Field Diameter (MFD)
*   **Question:** Define Mode-Field Diameter (MFD) and state its significance.
*   **Answer:**
    *   **Definition:** The radial distance across the fiber center where the optical power density drops to $1/e^2$ of its peak value (representing the spatial width of the fundamental mode, which extends slightly into the cladding).
    *   **Significance:** Determines coupling efficiency, splice sensitivity, and susceptibility to microbending loss.

---

### 🎴 Card 8: Field Distribution Functions (Core vs. Cladding)
*   **Question:** What mathematical functions represent the electromagnetic fields ($E_z, H_z$) in the core ($r < a$) and cladding ($r > a$) regions of a step-index fiber?
*   **Answer:**
    *   **Core Region ($r < a$):** Bessel functions of the first kind ($J_\nu(u r / a)$), representing oscillatory behavior inside the core.
    *   **Cladding Region ($r > a$):** Modified Bessel functions of the second kind ($K_\nu(w r / a)$), representing evanescent decay of fields into the cladding.

---

### 🎴 Card 9: Waveguide Boundary Continuity
*   **Question:** Which field components must be continuous at the core-cladding boundary ($r = a$)?
*   **Answer:**
    The tangential components of the electric and magnetic fields:
    $$E_z, \quad H_z, \quad E_\phi, \quad H_\phi$$

---

### 🎴 Card 10: Propagation Mode Classes
*   **Question:** Name the four types of propagation modes found in circular dielectric waveguides.
*   **Answer:**
    1.  **TE Modes:** Transverse Electric ($E_z = 0, H_z \neq 0$).
    2.  **TM Modes:** Transverse Magnetic ($H_z = 0, E_z \neq 0$).
    3.  **HE Modes:** Hybrid modes ($E_z \neq 0, H_z \neq 0$) dominated by the electric field.
    4.  **EH Modes:** Hybrid modes ($E_z \neq 0, H_z \neq 0$) dominated by the magnetic field.
