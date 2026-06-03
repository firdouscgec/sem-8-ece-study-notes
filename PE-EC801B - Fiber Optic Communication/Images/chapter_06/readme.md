# Diagrams Registry: PE-EC801B - Chapter 06

This registry contains copy-ready Mermaid source codes for diagrams related to Chapter 6 (Nonlinear Effects).

---

## 1. Stimulated Scattering Processes (SRS vs. SBS)
This diagram illustrates the difference between Stimulated Raman Scattering (SRS) and Stimulated Brillouin Scattering (SBS) in terms of their physical mechanisms, phonon interactions, and propagation directions.

* **File Name:** `srs_vs_sbs.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "Stimulated Raman Scattering (SRS)"
        Pump1["Pump Photon (omega_p)"] --> Molecule["Interaction with Molecular Vibrations"]
        Molecule --> Stokes1["Stokes Photon (omega_s = omega_p - Omega_v)"]
        Molecule --> Phonon1["Optical Phonon (High Energy, Localized)"]
        Stokes1 -->|Direction| ForwardBackward["Forward & Backward Directions"]
    end
    subgraph "Stimulated Brillouin Scattering (SBS)"
        Pump2["Pump Photon (omega_p)"] --> Acoustic["Interaction with Acoustic Waves (Density Fluctuations)"]
        Acoustic --> Stokes2["Stokes Photon (omega_s = omega_p - Omega_a)"]
        Acoustic --> Phonon2["Acoustic Phonon (Low Energy, Traveling)"]
        Stokes2 -->|Direction| BackwardOnly["Strictly Backward Direction (Dominant)"]
    end
    
    style Pump1 fill:#dae8fc,stroke:#6c8ebf,color:#000
    style Pump2 fill:#dae8fc,stroke:#6c8ebf,color:#000
    style Stokes1 fill:#d5e8d4,stroke:#82b1ff,color:#000
    style Stokes2 fill:#d5e8d4,stroke:#82b1ff,color:#000
```

---

## 2. Self-Phase Modulation (SPM) Frequency Chirping
This block diagram outlines the step-by-step physical process of Self-Phase Modulation (SPM) showing how a pulse's intensity profile induces refractive index changes, phase shifts, and resulting frequency chirp.

* **File Name:** `spm_chirp.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "Self-Phase Modulation (SPM) Mechanism"
        Intensity["Pulse Intensity Profile I(t)<br>(Gaussian / Secant Hyperbolic Shape)"] -->|"Kerr Effect: n(t) = n_0 + n_2 I(t)"| Index["Refractive Index Variation n(t)"]
        Index -->|"Phase: phi(t) = omega_0 t - (2 pi / lambda) n(t) z"| Phase["Time-Dependent Phase Shift phi_NL(t)"]
        Phase -->|"Chirp: delta_omega(t) = - d(phi_NL)/dt"| Chirp["Frequency Chirping delta_omega(t)"]
        
        Chirp --> LeadingEdge["Leading Edge (dI/dt > 0) -> delta_omega < 0 (Red Shift)"]
        Chirp --> TrailingEdge["Trailing Edge (dI/dt < 0) -> delta_omega > 0 (Blue Shift)"]
    end
    
    style Intensity fill:#ffe6cc,stroke:#d79b00,color:#000
    style Phase fill:#dae8fc,stroke:#6c8ebf,color:#000
    style Chirp fill:#f8cecc,stroke:#b85450,color:#000
```

---

## 3. Four-Wave Mixing (FWM) Frequency Generation
This diagram shows the third-order nonlinear interaction in Four-Wave Mixing (FWM), where three signals beat together to generate new intermodulation products.

* **File Name:** `fwm_frequencies.png`
* **Mermaid Code:**

```mermaid
graph LR
    subgraph "Four-Wave Mixing (FWM)"
        f1["Frequency f_1"] --> FWM_Proc["Nonlinear Medium<br>(Third-order susceptibility chi^(3))"]
        f2["Frequency f_2"] --> FWM_Proc
        f3["Frequency f_3"] --> FWM_Proc
        FWM_Proc --> NewFreqs["Generated Intermodulation Frequencies<br>f_ijk = f_i + f_j - f_k"]
        NewFreqs --> Ex1["f_123 = f_1 + f_2 - f_3"]
        NewFreqs --> Ex2["f_213 = f_2 + f_1 - f_3"]
    end
    
    style f1 fill:#dae8fc,stroke:#6c8ebf,color:#000
    style f2 fill:#dae8fc,stroke:#6c8ebf,color:#000
    style f3 fill:#dae8fc,stroke:#6c8ebf,color:#000
    style NewFreqs fill:#ffe6cc,stroke:#d79b00,color:#000
```

---

## 4. Soliton Propagation Balance
This diagram explains the physical mechanism of fundamental soliton propagation in optical fibers, where the chirp introduced by anomalous Group Velocity Dispersion (GVD) is exactly counteracted by the chirp of Self-Phase Modulation (SPM).

* **File Name:** `soliton_balance.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "Optical Soliton Balance Mechanism"
        SPM_Chirp["Self-Phase Modulation (SPM) Chirp:<br>- Leading Edge: Red Shift (Lower Frequencies)<br>- Trailing Edge: Blue Shift (Higher Frequencies)"]
        GVD_Anomalous["Anomalous GVD (D > 0, beta_2 < 0):<br>- Red Shift (Lower Frequencies) travels SLOWER<br>- Blue Shift (Higher Frequencies) travels FASTER"]
        
        SPM_Chirp -->|Interaction| Balance["Opposite Chirp Effects Cancel Out"]
        GVD_Anomalous -->|Interaction| Balance
        
        Balance -->|"Result: Stable Envelope"| Soliton["Fundamental Soliton Wave (N = 1)<br>Shape: sech(t) shape is preserved indefinitely"]
    end
    
    style SPM_Chirp fill:#f8cecc,stroke:#b85450,color:#000
    style GVD_Anomalous fill:#dae8fc,stroke:#6c8ebf,color:#000
    style Soliton fill:#d5e8d4,stroke:#82b1ff,color:#000
```
