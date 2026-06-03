# Diagrams Registry: PE-EC801B - Chapter 04

This registry contains copy-ready Mermaid source codes for diagrams related to Chapter 4 (Optical Sources & Detectors).

---

## 1. Fabry-Perot Laser Cavity
This diagram illustrates the structure of a semiconductor Fabry-Perot cavity laser, highlighting the active region, cleaved facet mirrors, and output beam.

* **File Name:** `laser_cavity.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph FP_Laser ["Fabry-Perot Semiconductor Laser"]
        Mirror1["Cleaved Facet Mirror (Reflectivity R1)"]
        Active["Active Layer / Gain Medium (Length L)"]
        Mirror2["Cleaved Facet Mirror (Reflectivity R2)"]
        
        Mirror1 <== Gain & Feedback ==> Active
        Active <== Gain & Feedback ==> Mirror2
    end
    Mirror2 ===>|Laser Beam output| Output["Coherent Laser Light"]
    
    style Mirror1 fill:#d5e8d4,stroke:#82b1ff,stroke-width:2px,color:#000
    style Active fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Mirror2 fill:#d5e8d4,stroke:#82b1ff,stroke-width:2px,color:#000
    style Output fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. Digital Optical Receiver
This diagram represents the block diagram of a digital optical receiver, showing the conversion from optical signal to decision outputs.

* **File Name:** `optical_receiver.png`
* **Mermaid Code:**

```mermaid
graph LR
    Input["Optical Input Signal"] --> Detector["Photodetector (PIN / APD)"]
    Detector -->|Photocurrent| PreAmp["Preamplifier (TIA)"]
    PreAmp -->|Voltage| MainAmp["Linear Amp / Equalizer"]
    MainAmp --> Filter["Low-Pass Filter"]
    Filter --> Decision["Decision Circuit / Comparator"]
    Decision --> OutputData["Digital Data Out"]
    
    Filter -.-> Clock["Clock Recovery Circuit"]
    Clock -. Sampling clock .-> Decision
    
    style Detector fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style PreAmp fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style MainAmp fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Filter fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Decision fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 3. PIN vs. APD Structure Comparison
This diagram details the difference in physical structures and depletion regions between a standard PIN photodiode and an Avalanche Photodiode (APD).

* **File Name:** `detector_structures.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph PIN ["PIN Photodiode Layers"]
        P_pin["p+ Layer"] === I_pin["Intrinsic (I) absorption region"]
        I_pin === N_pin["n+ Layer"]
    end
    
    subgraph APD ["APD Layers (Reach-Through Structure)"]
        P_apd["p+ Layer"] === I_apd["Intrinsic (I) absorption region"]
        I_apd === P_mult["p Layer (Multiplication field)"]
        P_mult === N_apd["n+ Layer"]
    end
    
    style I_pin fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style I_apd fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style P_mult fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```
*(Note: For LaTeX output, this will be represented as a labeled cross-sectional schematic diagram showing the electric field profiles.)*
