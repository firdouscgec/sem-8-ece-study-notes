# PE-EC801B: Fiber Optic Communication - One-Liners

---

# Chapter 1: Introduction

1. Light carrier frequency range → Terahertz range ($10^{14}\ \text{Hz}$).
2. Physical principle of light confinement in fiber core → Total Internal Reflection (TIR).
3. Snell's Law equation → $n_1 \sin \theta_1 = n_2 \sin \theta_2$.
4. Critical angle formula at core-clad interface → $\theta_c = \sin^{-1}(n_2 / n_1)$.
5. Two necessary conditions for TIR → Denser to rarer medium propagation; incidence angle exceeding critical angle.
6. Acceptance angle definition → Maximum incident angle at air-core interface for guided propagation.
7. Numerical Aperture (NA) definition → Sine of acceptance angle in air, representing light-gathering capacity.
8. NA formula in terms of refractive indices → $\text{NA} = \sqrt{n_1^2 - n_2^2}$.
9. Approximate NA formula in terms of index difference ($\Delta$) → $\text{NA} \approx n_1 \sqrt{2 \Delta}$.
10. Relative refractive index difference ($\Delta$) formula → $\Delta = \frac{n_1 - n_2}{n_1}$.
11. Rays passing through fiber's longitudinal central axis → Meridional rays.
12. Rays following helical paths without crossing central axis → Skew rays.
13. Acceptance angle formula for air launch ($n_0=1$) → $\theta_a = \sin^{-1}(\sqrt{n_1^2 - n_2^2})$.
14. Geometric (Ray) model validity condition → Core diameter much larger than wavelength ($d \gg \lambda$).
15. Wave model mandatory condition → Core diameter comparable to wavelength ($d \approx \lambda$).
16. Non-propagating mode in cylindrical dielectric rods → Transverse Electromagnetic (TEM) mode.
17. Mode class where $E_z = 0$ and $H_z \neq 0$ → Transverse Electric (TE) mode.
18. Mode class where $H_z = 0$ and $E_z \neq 0$ → Transverse Magnetic (TM) mode.
19. Mode class where both $E_z \neq 0$ and $H_z \neq 0$ → Hybrid mode (HE or EH).
20. Cause of hybrid modes in fibers → Vector boundary conditions at curved core-cladding interface.
21. Main advantages of fiber over copper → Enormous bandwidth, complete immunity to EMI, and low attenuation.
22. Key drawbacks of optical fiber cabling → Fragility, high initial installation cost, and splicing difficulty.
23. Typical cladding diameter size in standard fibers → $125\ \mu\text{m}$.
24. Launching medium refractive index (air) → $n_0 = 1.0$.
25. Critical angle for $n_1 = 1.82$ and $n_2 = 1.73$ → $71.91^\circ$.

# Chapter 2: Optical Fibers

1. Step-index refractive index profile definition → Constant core index dropping abruptly at boundary.
2. Graded-index refractive index profile formula → $n(r) = n_1 \sqrt{1 - 2\Delta(r/a)^\alpha}$ for $r < a$.
3. Profile parameter value ($\alpha$) for parabolic graded-index → $\alpha = 2$.
4. Light path trajectory in step-index fiber → Zig-zag paths via discrete reflections (TIR).
5. Light path trajectory in graded-index fiber → Continuous sinusoidal curving refraction paths.
6. Core diameter of standard single-mode fiber (SMF) → $8 \text{ to } 10\ \mu\text{m}$.
7. Core diameter of standard multimode fiber (MMF) → $50 \text{ to } 100\ \mu\text{m}$.
8. Intermodal dispersion in single-mode fiber → Zero.
9. Normalized frequency ($V$-number) formula → $V = \frac{2\pi a}{\lambda}\text{NA}$.
10. Single-mode propagation condition for step-index fiber → $V < 2.405$.
11. First guided mode to propagate in optical fiber → Fundamental $\text{HE}_{11}$ mode.
12. Number of guided modes ($N$) in step-index multimode fiber → $N \approx \frac{V^2}{2}$.
13. Number of guided modes ($N$) in graded-index parabolic fiber → $N \approx \frac{V^2}{4}$.
14. Cutoff wavelength ($\lambda_c$) formula for single-mode fiber → $\lambda_c = \frac{2\pi a \text{NA}}{2.405}$.
15. Mode-Field Diameter (MFD) definition → Radial width where optical power density falls to $1/e^2$.
16. MARCUSE formula purpose → Estimating mode-field diameter in step-index fibers.
17. Field distribution function in the core ($r < a$) → Bessel function of the first kind ($J_\nu$).
18. Field distribution function in the cladding ($r > a$) → Modified Bessel function of the second kind ($K_\nu$).
19. Boundary continuity field components at $r = a$ → Tangential components $E_z$, $H_z$, $E_\phi$, $H_\phi$.
20. Number of guided modes for $V = 75.78$ in step-index → $2871$.
21. Cutoff wavelength for $a = 4\ \mu\text{m}$, $n_1=1.48$, $\Delta=0.2\%$ → $978\text{ nm}$.
22. Key source compatible with single-mode fibers → Laser Diode (LD).
23. Key disadvantage of step-index multimode fiber → High intermodal dispersion limiting bandwidth.
24. Key advantage of graded-index fiber over step-index MMF → Lower intermodal dispersion.
25. MFD significance → Determines coupling efficiency, splice sensitivity, and microbending losses.

# Chapter 3: Signal Degradation

1. Attenuation definition → Reduction in optical signal power during propagation.
2. Attenuation coefficient ($\alpha$) formula → $\alpha = \frac{10}{L} \log_{10}(P_{in}/P_{out})\dots\text{dB/km}$.
3. Signal dispersion definition → Temporal broadening of light pulses during propagation.
4. Consequence of dispersion on digital transmission → Inter-Symbol Interference (ISI) limiting bandwidth.
5. Dominant scattering mechanism in optical fibers → Rayleigh scattering.
6. Rayleigh scattering coefficient wavelength dependence → $\alpha_{sc} \propto 1/\lambda^4$.
7. Rayleigh scattering physical cause → Microscopic density and composition fluctuations frozen in glass.
8. Intrinsic absorption edges in silica → UV electronic absorption; IR molecular vibrational absorption.
9. Extrinsic absorption causes in fibers → Transition metal impurities and hydroxyl ($\text{OH}^-$) ions.
10. Peak absorption wavelengths of water ($\text{OH}^-$) ions → $950\text{ nm}$, $1240\text{ nm}$, and $1380\text{ nm}$.
11. Attenuation value in first transmission window ($850\text{ nm}$) → $2.0 \text{ to } 3.0\ \text{dB/km}$.
12. Attenuation value in second transmission window ($1310\text{ nm}$) → $0.4\ \text{dB/km}$.
13. Attenuation value in third transmission window ($1550\text{ nm}$) → $0.2\ \text{dB/km}$.
14. Unique dispersion characteristic of standard SMF at $1310\text{ nm}$ → Zero chromatic dispersion.
15. Key advantage of $1550\text{ nm}$ transmission window → Minimum attenuation window matching EDFA band.
16. Macrobending loss cause → Fiber curvature radius of a few centimeters.
17. Microbending loss cause → Microscopic axial deviations from mechanical lateral stress.
18. Cabling primary functions → Mechanical protection, environmental shielding, and microbending mitigation.
19. Intermodal delay difference ($\Delta t_{modal}$) formula for step-index → $\Delta t_{modal} \approx \frac{n_1 L}{c} \Delta$.
20. RMS pulse broadening ($\sigma_{modal}$) formula for step-index MMF → $\sigma_{modal} \approx \frac{n_1 L \Delta}{2\sqrt{3}c}$.
21. Chromatic dispersion components → Material dispersion and waveguide dispersion.
22. Material dispersion formula coefficient ($D_M$) → $D_M = -\frac{\lambda}{c} \frac{d^2 n_1}{d\lambda^2}$.
23. Dispersion-Shifted Fiber (DSF) design objective → Shift zero-dispersion wavelength to $1550\text{ nm}$.
24. Dispersion-Flattened Fiber (DFF) design objective → Keep dispersion low ($< 2\ \text{ps/(nm}\cdot\text{km)}$) across $1300\text{--}1600\text{ nm}$.
25. Preform fabrication dry mixture reactants → $\text{SiCl}_4$, $\text{GeCl}_4$, and $\text{O}_2$.
26. Sintering definition in MCVD → Heating deposited soot to form solid glass layers.
27. Preform fabrication method using concentric inner/outer pots → Double-Crucible method.
28. OTDR full form → Optical Time Domain Reflectometer.
29. OTDR continuous downward slope represents → Rayleigh backscattering attenuation.
30. OTDR sharp upward peaks represent → Fresnel reflections from connectors or faults.
31. Standard method for high-accuracy fiber attenuation measurement → Cut-Back method.
32. GRIN-rod lens diameter range → 0.5 to 2 mm.
33. GRIN-rod lens divergence angle → 1 to 5 degrees.
34. GRIN-rod lens fiber alignment position → Exactly at the focal length of the lens.
35. Typical insertion loss of expanded-beam connector → $0.7\ \text{dB}$.

# Chapter 4: Optical Sources & Detectors

1. LED light emission process → Spontaneous emission of photons.
2. Laser diode light emission process → Stimulated emission of coherent photons.
3. LED spectral width ($\Delta\lambda$) range → Broad ($30 \text{ to } 50\text{ nm}$).
4. Laser diode spectral width ($\Delta\lambda$) range → Narrow ($< 1 \text{ to } 3\text{ nm}$).
5. Condition where excited state population exceeds ground state → Population inversion.
6. Method of achieving population inversion at junction → Heavy doping of both regions under forward bias.
7. Lasing threshold gain ($g_{th}$) formula → $g_{th} = \alpha_t + \frac{1}{2L} \ln\left(\frac{1}{R_1 R_2}\right)$.
8. Reflectivity ($R$) formula at normal incidence → $R = \left(\frac{n-1}{n+1}\right)^2$.
9. Reflectivity of GaAs-air interface ($n=3.6$) → $32\%$ (or $0.32$).
10. Longitudinal mode count ($m$) formula → $m = \frac{2nL}{\lambda}$.
11. Mode count for ruby laser ($L=3\text{ cm}, n=1.6, \lambda=0.43\ \mu\text{m}$) → $2.23 \times 10^5$.
12. Frequency separation of modes ($\Delta f$) formula → $\Delta f = \frac{c}{2nL}$.
13. Mode frequency separation for $L=5\text{ cm}, n=1.8$ → $1.67\text{ GHz}$.
14. Wavelength mode separation ($\Delta\lambda$) formula → $\Delta \lambda = \frac{\lambda^2 \Delta f}{c}$.
15. Mode separation for $\lambda = 0.5\ \mu\text{m}$ and $\Delta f = 2\text{ GHz}$ → $1.67 \times 10^{-12}\text{ m}$.
16. Radiative minority carrier lifetime ($\tau_r$) formula → $\tau_r = \frac{1}{B \cdot p_0}$.
17. Radiative lifetime for $p_0=10^{18}\text{ cm}^{-3}, B=7.21 \times 10^{-10}\text{ cm}^3\text{s}^{-1}$ → $1.39\text{ ns}$.
18. Shorter wavelength semiconductor material system → GaAs/AlGaAs DH.
19. Recombination characteristics of indirect band-gap semiconductors → Slow and heat-producing.
20. PIN photodiode internal gain ($M$) → $M = 1$ (no internal gain).
21. Avalanche Photodiode (APD) gain mechanism → Impact ionization under high reverse bias.
22. APD typical reverse bias operating voltage range → $100 \text{ to } 300\ \text{V}$.
23. Quantum efficiency ($\eta$) definition → Fraction of incident photons generating collected carrier pairs.
24. Responsivity ($R$) definition → Ratio of output photocurrent to incident optical power.
25. Responsivity formula in terms of quantum efficiency and wavelength → $R = \frac{\eta e \lambda}{hc} \approx \frac{\eta \lambda(\mu\text{m})}{1.24}\ \text{A/W}$.
26. Reason Silicon is unsuitable for $1550\text{ nm}$ window → Bandgap too wide ($E_g=1.1\ \text{eV}$), transparent to $1550\text{ nm}$.
27. Preferred photodetector material for $1310/1550\text{ nm}$ windows → Indium Gallium Arsenide (InGaAs).
28. Primary noise sources in digital optical receiver → Shot noise, thermal noise, and amplifier noise.
29. Thermal noise (Johnson noise) mean-square current formula → $\langle i_{thermal}^2 \rangle = \frac{4 k_B T B}{R_L}$.
30. APD shot noise mean-square current formula → $\langle i_{shot}^2 \rangle = 2e(I_p + I_d)M^2 F(M)B$.
31. Link Power Budget equation → $P_T-P_R=\alpha L+N_{sp}\alpha_{sp}+N_c\alpha_c+M_s$.
32. System rise-time ($t_{sys}$) budget equation → $t_{sys}=(t_{tx}^2+t_{mat}^2+t_{mod}^2+t_{rx}^2)^{1/2}$.
33. Maximum rise-time limit for NRZ digital systems → $t_{sys} \le 0.7 T$.
34. Quantum limit of detection for $\text{BER}=10^{-9}$ → Average minimum of $21$ photons per pulse.
35. Recombination lifetime of direct band-gap semiconductors → Nanoseconds.

# Chapter 5: Optical Switches & Amplifiers

1. EDFA full form → Erbium-Doped Fiber Amplifier.
2. EDFA gain medium → Silica fiber doped with Erbium ($\text{Er}^{3+}$) ions.
3. EDFA standard pumping wavelengths → $980\text{ nm}$ and $1480\text{ nm}$.
4. Raman amplifier gain mechanism → Stimulated Raman Scattering (SRS).
5. Raman amplifier gain medium → Standard transmission fiber core (distributed amplification).
6. Raman pump wavelength condition → Must be $\approx 100\text{ nm}$ shorter than signal.
7. Stokes shift frequency value in silica → $\approx 13.2\ \text{THz}$.
8. WDM full form → Wavelength Division Multiplexing.
9. Channel spacing in Coarse WDM (CWDM) → Wide, typically $20\text{ nm}$.
10. Channel spacing in Dense WDM (DWDM) → Narrow, $\le 1.6\text{ nm}$ (typically $0.8\text{ nm}/100\text{ GHz}$).
11. Fused Biconical Taper (FBT) power splitting mechanism → Evanescent wave coupling in tapered region.
12. Symmetric directional coupler power transfer equation ($P_2(z)$) → $P_2(z) = P_0 \sin^2(\kappa z)$.
13. Coupling length ($L_c$) formula for symmetric coupler → $L_c = \frac{\pi}{2\kappa}$.
14. Switch state when directional coupler is phase-matched ($\Delta\beta=0$) → Cross state (100% power transfer).
15. Switch state when phase-mismatch ($\Delta\beta \neq 0$) is induced by voltage → Bar state.
16. Electro-optic switch material substrate → Lithium Niobate ($\text{LiNbO}_3$).
17. Mach-Zehnder Interferometer (MZI) switch switching voltage symbol → $V_\pi$.
18. Four protocol layers of SONET → Photonic, Section, Line, and Path layers.
19. OADM function in optical networks → Selectively drop and add specific wavelengths at nodes.
20. OXC function in optical networks → Route wavelengths dynamically between multiple fiber ports.
21. RWA problem full form → Routing and Wavelength Assignment.
22. Constraint requiring a lightpath to use same wavelength throughout → Wavelength continuity constraint.
23. Device that removes wavelength continuity constraint → Wavelength converter.
24. Typical noise figure of EDFA → $3 \text{ to } 5\ \text{dB}$.
25. Number of fibers required for unidirectional WDM duplex link → Two.

# Chapter 6: Nonlinear Effects

1. Optical Kerr effect definition → Refractive index changes linearly with local optical intensity.
2. Refractive index formula under Kerr effect → $n(I) = n_0 + n_2 I$.
3. Nonlinear refractive index coefficient ($n_2$) of silica → $\approx 2.6 \times 10^{-20}\ \text{m}^2/\text{W}$.
4. Kerr-effect-based nonlinear phenomena → Self-Phase Modulation, Cross-Phase Modulation, Four-Wave Mixing.
5. Inelastic scattering-based nonlinear phenomena → Stimulated Raman Scattering and Stimulated Brillouin Scattering.
6. Physical mechanism of SBS → Light scattering from acoustic density waves (acoustic phonons).
7. Physical mechanism of SRS → Light scattering from optical molecular vibrations (optical phonons).
8. Direction of scattered wave propagation in SBS → Strictly backward (backscattering).
9. Direction of scattered wave propagation in SRS → Both forward and backward directions.
10. Frequency shift value in SBS → Small, $\approx 10 \text{ to } 11\ \text{GHz}$.
11. Frequency shift value in SRS → Large, $\approx 13.2\ \text{THz}$.
12. Typical SBS threshold power level in standard SMF → Very low ($1 \text{ to } 10\ \text{mW}$).
13. Typical SRS threshold power level in standard SMF → Very high ($\approx 1\ \text{W}$).
14. Effective fiber interaction length ($L_{eff}$) formula → $L_{eff} = \frac{1 - e^{-\alpha L}}{\alpha}$.
15. SBS threshold power formula → $P_{th,\text{SBS}} \approx \frac{21 A_{\text{eff}}}{g_B L_{\text{eff}}}$.
16. SRS threshold power formula → $P_{th,\text{SRS}} \approx \frac{16 A_{\text{eff}}}{g_R L_{\text{eff}}}$.
17. Key physical consequence of Self-Phase Modulation (SPM) → Spectral broadening of the pulse.
18. SPM nonlinear phase shift ($\phi_{NL}$) formula → $\phi_{\text{NL}}(t) = \gamma P(t) z$.
19. Fiber nonlinearity parameter ($\gamma$) formula → $\gamma = \frac{2\pi n_2}{\lambda A_{\text{eff}}}$.
20. Cross-Phase Modulation (XPM) definition → Pulse phase modulation induced by co-propagating channel intensities.
21. Four-Wave Mixing (FWM) definition → Third-order parametric process generating sidebands from channel beating.
22. Key condition for efficient FWM generation → Phase-matching condition ($\Delta k \approx 0$).
23. Fiber design type that mitigates FWM in DWDM → Non-Zero Dispersion-Shifted Fiber (NZ-DSF).
24. Optical soliton definition → Pulse that propagates without broadening using GVD and SPM.
25. Balancing mechanism of fundamental solitons → Anomalous dispersion ($D > 0$) GVD cancels SPM red-shift chirp.
26. Pulse shape of fundamental soliton → Hyperbolic secant ($\operatorname{sech}$).
27. Equation governing soliton propagation in fibers → Nonlinear Schrödinger Equation (NLSE).
28. GVD parameter ($\beta_2$) relation to dispersion parameter ($D$) → $D = -\frac{2\pi c}{\lambda^2} \beta_2$.
29. Regime where fundamental solitons can propagate → Anomalous dispersion regime ($\beta_2 < 0$, $D > 0$).
30. Jitter caused by soliton-amplifier noise interaction → Gordon-Haus jitter.
