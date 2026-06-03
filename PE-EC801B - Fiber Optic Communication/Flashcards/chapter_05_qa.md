# Flashcards: Unit V - Optical Switches & Amplifiers

These active recall Question-and-Answer cards cover Erbium-Doped Fiber Amplifiers (EDFA), Raman Amplifiers, DWDM systems, Fused Biconical Taper (FBT) couplers, coupled mode analysis of directional couplers, Lithium Niobate ($\text{LiNbO}_3$) electro-optic switches, SONET layers, and WDM network elements (OADMs, OXCs, RWA problem, wavelength conversion).

---

### 🎴 Card 1: EDFA vs. Raman Amplifiers
*   **Question:** Compare EDFA and Raman Amplifiers in terms of gain medium, gain mechanism, pumping wavelength, and gain flexibility.
*   **Answer:**
    *   **EDFA (Erbium-Doped Fiber Amplifier):**
        *   *Gain Medium:* Erbium-ion ($\text{Er}^{3+}$) doped silica fiber.
        *   *Gain Mechanism:* Population inversion and stimulated emission of Erbium ions.
        *   *Pumping Wavelengths:* $980\text{ nm}$ (higher efficiency) or $1480\text{ nm}$ (higher output power).
        *   *Gain Flexibility:* Fixed gain band, operating in C-band ($1530 \text{ to } 1565\ \text{nm}$) and L-band ($1565 \text{ to } 1625\ \text{nm}$).
    *   **Raman Amplifier:**
        *   *Gain Medium:* The intrinsic silica glass core of standard transmission fiber (distributed amplification).
        *   *Gain Mechanism:* Stimulated Raman Scattering (SRS), where pump photons transfer energy to signal photons via optical phonons.
        *   *Pumping Wavelengths:* Must be $\approx 100\text{ nm}$ shorter than the signal wavelength (Stokes shift of $\approx 13.2\ \text{THz}$).
        *   *Gain Flexibility:* Highly flexible; the gain band can be placed anywhere in the fiber window by selecting the pump wavelength.

---

### 🎴 Card 2: Coarse WDM vs. Dense WDM
*   **Question:** Compare Coarse WDM (CWDM) and Dense WDM (DWDM) systems in terms of channel spacing, channel capacity, and cost/laser stability.
*   **Answer:**
    *   **CWDM (Coarse WDM):**
        *   *Channel Spacing:* Large spacing, typically $20\text{ nm}$.
        *   *Capacity:* Low (typically 8 to 16 channels).
        *   *Lasers/Filters:* Wide optical filters and uncooled, low-precision, inexpensive lasers.
        *   *Application:* Low-cost metro/access networks.
    *   **DWDM (Dense WDM):**
        *   *Channel Spacing:* Narrow spacing, $\le 1.6\text{ nm}$ (typically $0.8\text{ nm}$ corresponding to $100\text{ GHz}$ or $0.4\text{ nm}$ for $50\text{ GHz}$ ITU grids).
        *   *Capacity:* Very high (80 to $160+$ channels over a single fiber).
        *   *Lasers/Filters:* Narrow, temperature-stabilized Distributed Feedback (DFB) lasers and high-precision optical filters.
        *   *Application:* Long-haul, high-capacity core networks.

---

### 🎴 Card 3: Fused Biconical Taper (FBT) Coupler
*   **Question:** Explain the construction and power-coupling mechanism of a Fused Biconical Taper (FBT) coupler.
*   **Answer:**
    *   **Construction:** Two bare optical fibers are aligned parallel and in contact, heated to melting temperature, and slowly stretched under tension. This creates a unified coupling region with a tapered, reduced core diameter.
    *   **Coupling Mechanism:** In the tapered region, the fiber cores shrink, making the optical fields weakly guided. The fundamental mode fields expand into the cladding and overlap. Power transfers between the fibers through *evanescent wave coupling*. The splitting ratio ($3\ \text{dB}$, $90/10$, etc.) is determined by the length of the tapered coupling region.

---

### 🎴 Card 4: Directional Couplers as Switches
*   **Question:** How does a symmetric directional coupler act as a $2 \times 2$ optical switch? Explain the cross state and the bar state.
*   **Answer:**
    *   **Cross State (Default):** When no voltage is applied ($\Delta\beta = 0$), the two waveguides are phase-matched. Light entering Port 1 transfers completely to Port 2 after propagating a distance equal to the coupling length $L = L_c = \frac{\pi}{2\kappa}$.
    *   **Bar State (Switched):** An external voltage is applied across electrodes. Due to the electro-optic effect, this changes the refractive indices of the guides, creating a phase mismatch ($\Delta\beta = \beta_1 - \beta_2 \neq 0$). This phase mismatch prevents complete coupling, forcing the light to remain in the input waveguide and exit at Port 1.

---

### 🎴 Card 5: Coupled Mode Analysis Formula
*   **Question:** Write the formula for the output power in the second waveguide ($P_2(z)$) of a directional coupler and define its coupling length ($L_c$).
*   **Answer:**
    *   **Power Transfer Equation:** If power $P(0) = P_0$ is launched into Guide 1 at $z=0$, the power coupled into Guide 2 at distance $z$ is:
        $$P_2(z) = P_0 \frac{\kappa^2}{\kappa^2 + (\Delta\beta/2)^2} \sin^2\left(\sqrt{\kappa^2 + (\Delta\beta/2)^2} z\right)$$
        where $\kappa$ is the coupling coefficient and $\Delta\beta$ is the phase mismatch.
    *   **Coupling Length ($L_c$):** The length required for $100\%$ power transfer when the guides are identical ($\Delta\beta = 0$):
        $$L_c = \frac{\pi}{2\kappa}$$

---

### 🎴 Card 6: Lithium Niobate ($\text{LiNbO}_3$) electro-optic switches
*   **Question:** Describe the structure and working mechanism of a Mach-Zehnder Interferometer (MZI) switch on Lithium Niobate.
*   **Answer:**
    *   **Structure:** An optical waveguide is diffused on a Lithium Niobate ($\text{LiNbO}_3$) substrate. It splits into two symmetric parallel arms at an input Y-junction, and recombines at an output Y-junction. Electrodes are placed along one or both arms.
    *   **Working Mechanism:**
        *   When no voltage is applied, light in both arms travels at the same speed, arriving in phase at the output junction. They interfere constructively, exiting the device (ON state).
        *   Applying a voltage shifts the refractive index of the arm waveguide via the electro-optic effect. This creates a phase difference $\Delta\phi = \pi$ between the arms. At the output, the fields interfere destructively, radiating the optical power into the substrate (OFF state).

---

### 🎴 Card 7: SONET Layers
*   **Question:** What are the four protocol layers of SONET, and what are their functions?
*   **Answer:**
    1.  **Photonic (Physical) Layer:** Manages physical transmission parameters, converting electrical signals into optical pulses and vice versa.
    2.  **Section Layer:** Manages transmission over a single physical fiber link, handling framing, scrambling, and basic link error monitoring.
    3.  **Line Layer:** Manages transport between multiplexers, handling synchronization, protection switching, and payload multiplexing.
    4.  **Path Layer:** Manages end-to-end transport between path terminating equipment (PTE), handling packet assembly, payload mapping, and end-to-end error checking.

---

### 🎴 Card 8: OADM vs. OXC
*   **Question:** Compare the functions of an Optical Add-Drop Multiplexer (OADM) and an Optical Cross-Connect (OXC) in WDM networks.
*   **Answer:**
    *   **OADM (Optical Add-Drop Multiplexer):** Used at network nodes to selectively *drop* (extract) specific wavelength channels from a multiplexed fiber, and *add* new signals on those same wavelengths, while allowing all other wavelength channels to pass through transparently.
    *   **OXC (Optical Cross-Connect):** Operates at the junction of multiple fiber routes. It dynamically routes channels from any input fiber to any output fiber on a wavelength-by-wavelength basis, performing space-division and wavelength routing without converting the optical signal to the electrical domain.

---

### 🎴 Card 9: RWA Problem & Wavelength Conversion
*   **Question:** What is the Routing and Wavelength Assignment (RWA) problem, and how does wavelength conversion help?
*   **Answer:**
    *   **RWA Problem:** The challenge of establishing lightpaths in a wavelength-routed network by finding an optimal path and assigning a specific wavelength. Under the *wavelength continuity constraint*, the same wavelength must be used on every fiber link along the entire path.
    *   **Wavelength Conversion:** A process that translates the optical wavelength of a signal (e.g., from $\lambda_1$ to $\lambda_2$) at an intermediate node entirely in the optical domain.
    *   **Impact:** It removes the wavelength continuity constraint. By allowing a lightpath to change wavelengths at intermediate nodes, wavelength conversion reduces blocking probability and increases network capacity.
