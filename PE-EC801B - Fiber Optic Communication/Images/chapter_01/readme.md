# Diagrams Registry: PE-EC801B - Chapter 01

This document contains copy-ready Mermaid source codes for the diagrams referenced in the Chapter 1 notes. These codes can be rendered to PNGs using the local Mermaid editor.

---

## 1. General Communication System Block Diagram
* **File Name:** `general_comm_block.png`
* **Mermaid Code:**

```mermaid
flowchart LR
    Source["[1] Information Source<br>(Voice, Data, Video)"]
    Tx["[2] Transmitter<br>(Processor / Modulator)"]
    Channel["[3] Channel (Medium)<br>(Copper, Coaxial, Free Space)"]
    Rx["[4] Receiver<br>(Demodulator / Amplifier)"]
    Dest["[5] Destination<br>(User Device)"]
    Noise["External Noise & Attenuation"]

    Source --> Tx
    Tx --> Channel
    Channel --> Rx
    Rx --> Dest
    Noise -.->|Distortion| Channel

    style Source fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Tx fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Channel fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
    style Rx fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Dest fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Noise fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. Fiber Optic Communication System Block Diagram
* **File Name:** `fiber_comm_block.png`
* **Mermaid Code:**

```mermaid
flowchart TD
    %% Transmitter Section
    subgraph TxGroup ["Transmitter Side"]
        direction LR
        Source["Info Source"]
        ElecTx["Electrical Tx<br>(Coder / Mux)"]
        Driver["Drive Circuit"]
        OptSrc["Optical Source<br>(LED / Laser)"]
        
        Source --> ElecTx --> Driver --> OptSrc
    end

    %% Channel Section
    subgraph ChannelGroup ["Optical Channel"]
        Fiber["Optical Fiber Cable<br>(Glass Waveguide - TIR)"]
    end

    %% Receiver Section
    subgraph RxGroup ["Receiver Side"]
        direction LR
        Detector["Optical Detector<br>(PIN / APD)"]
        ElecRx["Electrical Rx<br>(Amplifier / Demod)"]
        Dest["Destination"]
        
        Detector --> ElecRx --> Dest
    end

    %% Optical Links
    OptSrc -->|Light Pulses| Fiber
    Fiber -->|Attenuated Light| Detector

    %% Styling
    style TxGroup fill:#fdf6e3,stroke:#b58900,stroke-width:2px,color:#000
    style ChannelGroup fill:#eee8d5,stroke:#586e75,stroke-width:2px,color:#000
    style RxGroup fill:#fdf6e3,stroke:#2aa198,stroke-width:2px,color:#000
    
    style Source fill:#fff,stroke:#333
    style ElecTx fill:#fff,stroke:#333
    style Driver fill:#fff,stroke:#333
    style OptSrc fill:#ffd2d2,stroke:#ff3333,stroke-width:2px,color:#000
    style Fiber fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style Detector fill:#d2ffd2,stroke:#33cc33,stroke-width:2px,color:#000
    style ElecRx fill:#fff,stroke:#333
    style Dest fill:#fff,stroke:#333
```

---

## 3. Ray Propagation & Acceptance Angle Geometry
* **File Name:** `ray_propagation.png`
* **Mermaid Code:**

```mermaid
flowchart TD
    subgraph Geom ["Light Launching & Total Internal Reflection Geometry"]
        direction TB
        Axis["Fiber Axis (Centerline)"]
        Launch["Launch Medium (Air, n0)"]
        Core["Core (n1)"]
        Clad["Cladding (n2)"]
        
        %% Geometric Points
        A["Point A: Launch Interface (Snell's Law)<br>n0 sin(theta_i) = n1 sin(theta_r)"]
        B["Point B: Core-Cladding Boundary (TIR)<br>phi = 90 - theta_r >= theta_c"]
        
        Axis -.->|Reference Axis| A
        Launch --->|Incident Ray @ theta_i| A
        A --->|Refracted Ray @ theta_r| B
        B --->|Totally Internally Reflected Ray @ phi| Core
        
        style Axis stroke:#999,stroke-dasharray: 5 5
        style Core fill:#e8f4f8,stroke:#4a90e2,stroke-width:2px,color:#000
        style Clad fill:#f4f4f4,stroke:#999,stroke-width:1px,color:#000
        style Launch fill:#fff,stroke:#666
    end
```
