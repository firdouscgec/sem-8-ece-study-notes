# Flashcards: Unit III - Signal Degradation in Optical Fibers

These active recall Question-and-Answer cards cover the mechanisms of attenuation, macro/microbending losses, optical transmission windows, intermodal and intramodal dispersion, preform fabrication methods, and measurement techniques (OTDR, cut-back method, far-field NA measurement).

---

### 🎴 Card 1: Attenuation vs. Dispersion
*   **Question:** Compare the physical causes, system consequences, and standard measurement units for attenuation and dispersion in optical fibers.
*   **Answer:**
    *   **Attenuation:**
        *   *Cause:* Light energy loss due to absorption, Rayleigh scattering, and radiative bending.
        *   *Consequence:* Reduces the optical signal power at the receiver, limiting the maximum transmission distance (link reach).
        *   *Unit:* Decibels per kilometer ($\text{dB/km}$).
    *   **Dispersion:**
        *   *Cause:* Temporal spreading of light pulses as they propagate, due to velocity differences of different modes (intermodal) or wavelengths (intramodal).
        *   *Consequence:* Causes overlapping of adjacent pulses (Inter-Symbol Interference, ISI), which limits the bandwidth and the maximum data rate (bit rate).
        *   *Unit:* Picoseconds per nanometer-kilometer ($\text{ps/(nm}\cdot\text{km)}$) for chromatic dispersion; picoseconds or nanoseconds per kilometer ($\text{ps/km}$ or $\text{ns/km}$) for modal dispersion.

---

### 🎴 Card 2: Attenuation Mechanisms
*   **Question:** What are the three main physical mechanisms of attenuation in silica optical fibers?
*   **Answer:**
    1.  **Absorption:**
        *   *Intrinsic:* Material electronic transitions in the UV band and atomic/molecular vibrations in the infrared band.
        *   *Extrinsic:* Presence of impurities, specifically transition metal ions ($\text{Fe}^{2+}, \text{Cu}^{2+}$) and hydroxyl ($\text{OH}^-$) ions from water vapor.
    2.  **Scattering:** Mainly *Rayleigh scattering*, caused by microscopic localized density and composition fluctuations frozen into the glass during cooling. It is inversely proportional to the fourth power of wavelength ($\alpha_{sc} \propto 1/\lambda^4$).
    3.  **Bending Losses:**
        *   *Macrobending:* Light escapes when the fiber is bent with a visible curvature radius, making the angle of incidence at the interface smaller than the critical angle.
        *   *Microbending:* Microscopic axial deviations caused by localized mechanical stresses/uneven pressures during cabling.

---

### 🎴 Card 3: Optical Transmission Windows
*   **Question:** Detail the three standard transmission windows used in optical fiber communication in terms of typical wavelength and attenuation.
*   **Answer:**
    *   **First Window ($850\text{ nm}$ band):** Attenuation is relatively high ($\approx 2.0 \text{ to } 3.0\ \text{dB/km}$) due to Rayleigh scattering. Used primarily for short-distance, low-cost local links using GaAs LEDs or VCSELs.
    *   **Second Window ($1310\text{ nm}$ band / O-band):** Attenuation drops to $\approx 0.4\ \text{dB/km}$. Crucial because standard silica single-mode fibers exhibit *zero chromatic dispersion* at this wavelength.
    *   **Third Window ($1550\text{ nm}$ band / C-band):** Attenuation reaches its absolute physical minimum of $\approx 0.2\ \text{dB/km}$. This window is widely used for long-haul transmission and matches the gain spectrum of Erbium-Doped Fiber Amplifiers (EDFAs).

---

### 🎴 Card 4: Intermodal Dispersion and RMS Broadening
*   **Question:** State the formulas for (a) the intermodal delay difference ($\Delta t_{modal}$) and (b) the RMS pulse broadening ($\sigma_{modal}$) for a multimode step-index fiber.
*   **Answer:**
    *   **(a) Intermodal Delay Difference:** The time difference between the slowest mode (propagating at the critical angle) and the fastest mode (axial ray):
        $$\Delta t_{modal} = t_{slowest} - t_{fastest} = \frac{n_1 L}{c} \Delta \approx \frac{L (\text{NA})^2}{2 n_1 c}$$
    *   **(b) RMS Pulse Broadening ($\sigma_{modal}$):** Assuming a uniform distribution of power among all modes:
        $$\sigma_{modal} = \frac{\Delta t_{modal}}{2\sqrt{3}} = \frac{n_1 L \Delta}{2\sqrt{3} c}$$
    *   *Parameters:* $L$ is fiber length, $n_1$ is core index, $\Delta$ is relative index difference, and $c$ is the speed of light in vacuum.

---

### 🎴 Card 5: Intramodal (Chromatic) Dispersion
*   **Question:** Define Intramodal (Chromatic) Dispersion and distinguish between its two primary components: Material Dispersion and Waveguide Dispersion.
*   **Answer:**
    *   **Definition:** Pulse broadening within a single propagating mode because the source has a finite spectral width $\sigma_\lambda$, and different wavelengths travel at different velocities.
    *   **Material Dispersion ($D_M$):** Arises from the wavelength-dependence of the refractive index of the glass material ($n_1(\lambda)$):
        $$D_M = -\frac{\lambda}{c} \frac{d^2 n_1}{d\lambda^2}$$
    *   **Waveguide Dispersion ($D_W$):** Arises from fiber geometry, as the fraction of optical power residing in the core and cladding changes with wavelength (dependent on $V$-number):
        $$D_W = -\frac{n_2 \Delta}{c \lambda} V \frac{d^2(Vb)}{dV^2}$$

---

### 🎴 Card 6: Dispersion-Shifted vs. Dispersion-Flattened Fibers
*   **Question:** Explain the difference between Dispersion-Shifted Fibers (DSF) and Dispersion-Flattened Fibers (DFF).
*   **Answer:**
    *   **Dispersion-Shifted Fiber (DSF):** In standard single-mode fibers, zero dispersion occurs at $1310\text{ nm}$ while minimum loss is at $1550\text{ nm}$. DSF modifies the fiber's refractive index profile (e.g., using a triangular core) to increase waveguide dispersion, shifting the zero-dispersion wavelength to $1550\text{ nm}$ to combine zero dispersion and minimum attenuation.
    *   **Dispersion-Flattened Fiber (DFF):** Uses multiple cladding layers (e.g., quadruple-clad profile) to tailor waveguide dispersion such that it cancels material dispersion over a wide spectral range, keeping chromatic dispersion very low ($< 2\ \text{ps/(nm}\cdot\text{km)}$) across the $1300\text{ nm}$ to $1600\text{ nm}$ range.

---

### 🎴 Card 7: Fiber Fabrication Methods
*   **Question:** Briefly describe the four primary fabrication methods used to manufacture optical fibers.
*   **Answer:**
    1.  **Modified Chemical Vapor Deposition (MCVD):** A dry mixture of reactant gases ($\text{SiCl}_4, \text{GeCl}_4, \text{O}_2$) is passed inside a rotating silica tube heated externally by a traversing burner. Oxide soot deposits on the inner wall, is sintered, and the tube is collapsed into a solid preform.
    2.  **Outside Vapor Deposition (OVD):** Glass soot is deposited layer-by-layer onto a rotating mandrel via flame hydrolysis of chemical vapors. The mandrel is removed, and the porous preform is consolidated in a furnace.
    3.  **Vapor Axial Deposition (VAD):** Core and cladding soot particles are deposited axially on the end of a seed rod. It is a continuous process where soot deposition and sintering occur sequentially.
    4.  **Double-Crucible Method:** Direct melt technique where core glass is placed in an inner crucible and cladding glass in an outer crucible. The glasses melt and flow out coaxially, drawing the fiber directly.

---

### 🎴 Card 8: Optical Time Domain Reflectometer (OTDR)
*   **Question:** What is the working principle of an OTDR, and what features are observed on a typical OTDR trace?
*   **Answer:**
    *   **Working Principle:** Injects high-intensity optical pulses into the fiber and detects the backscattered light (Rayleigh scattering) and reflected light (Fresnel reflections) as a function of time.
    *   **OTDR Trace Features:**
        *   *Continuous downward slope:* Measures Rayleigh backscattering, representing the fiber's attenuation coefficient ($\text{dB/km}$).
        *   *Sharp upward peaks:* Represent Fresnel reflections from connectors, mechanical splices, or cleaved ends.
        *   *Non-reflective downward steps:* Represent localized loss without reflection, indicating fusion splices or macrobends.

---

### 🎴 Card 9: Fiber Measurement Techniques
*   **Question:** Explain how (a) fiber attenuation is measured using the Cut-Back Method, and (b) how the Numerical Aperture (NA) is measured.
*   **Answer:**
    *   **(a) Cut-Back Method:**
        1.  Measure the output optical power $P_2(L)$ at the far end of the long test fiber of length $L$.
        2.  Without disturbing the input launch conditions, cut the fiber a few meters from the launch end and measure the output power $P_1(z)$ at this short distance $z$.
        3.  The fiber attenuation is: $\alpha = \frac{10}{L-z} \log_{10}\left(\frac{P_1(z)}{P_2(L)}\right)\ \text{dB/km}$.
    *   **(b) NA Measurement:** Light exiting the fiber end is projected into the far field. The angular distribution of intensity is measured. The NA is calculated from the half-angle ($\theta_{5\%}$) where the intensity drops to $5\%$ of its peak value: $\text{NA} = \sin(\theta_{5\%})$.
