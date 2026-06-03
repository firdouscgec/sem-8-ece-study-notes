# Diagrams Registry: PE-EC801B - Chapter 05

This registry contains copy-ready Mermaid source codes for diagrams related to Chapter 5 (Optical Switches & Amplifiers).

---

## 1. EDFA Block Diagram
This block diagram represents the physical layout of an Erbium-Doped Fiber Amplifier (EDFA), showing the input signal, optical isolators, WDM coupler, pump laser, and the Erbium-doped fiber spool.

* **File Name:** `edfa_block.png`
* **Mermaid Code:**

```mermaid
graph LR
    Input["Signal Input"] --> Isolator1["Optical Isolator 1"]
    Isolator1 --> WDMCoupler["WDM Coupler"]
    PumpLaser["Pump Laser (980 / 1480 nm)"] --> WDMCoupler
    WDMCoupler --> EDF["Erbium-Doped Fiber (EDF)"]
    EDF --> Isolator2["Optical Isolator 2"]
    Isolator2 --> Output["Amplified Signal Output"]
    
    style WDMCoupler fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style EDF fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Isolator1 fill:#f5f5f5,stroke:#666,stroke-width:1px,color:#000
    style Isolator2 fill:#f5f5f5,stroke:#666,stroke-width:1px,color:#000
```

---

## 2. Directional Coupler Switch States
This diagram illustrates the cross state (zero applied voltage) and bar state (voltage applied) of a symmetric directional coupler switch.

* **File Name:** `directional_coupler.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "Cross State (Zero Voltage: L = Lc)"
        In1["Input 1"] ===>|100% Coupling| Out2["Output 2"]
        In2["Input 2"] ===>|100% Coupling| Out1["Output 1"]
    end
    subgraph "Bar State (Applied Voltage: Delta-beta mismatch)"
        In3["Input 1"] ===>|No Coupling| Out3["Output 1"]
        In4["Input 2"] ===>|No Coupling| Out4["Output 2"]
    end
```

---

## 3. MZI Switch Layout
This diagram details the layout of a Mach-Zehnder Interferometer (MZI) switch on Lithium Niobate ($\text{LiNbO}_3$), showing Y-junction splitters/combiners and the parallel arms.

* **File Name:** `mzi_switch.png`
* **Mermaid Code:**

```mermaid
graph LR
    Input["Input Guide"] --> YSplit["Y-Splitter"]
    YSplit --> Arm1["Interferometer Arm 1 (Electrode V)"]
    YSplit --> Arm2["Interferometer Arm 2 (Reference)"]
    Arm1 --> YCombine["Y-Combiner / Junction"]
    Arm2 --> YCombine
    YCombine --> Output["Output Guide"]
    
    style Arm1 fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Arm2 fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
```

---

## 4. OADM Architecture Block Diagram
This diagram represents the block diagram of a generic Optical Add-Drop Multiplexer (OADM), showing demuxing, switching, and muxing stages.

* **File Name:** `oadm_block.png`
* **Mermaid Code:**

```mermaid
graph LR
    Input["Multiplexed Input (lambda 1..n)"] --> Demux["Demultiplexer"]
    Demux --> DropSwitch["Drop Switches (Extract lambda_d)"]
    DropSwitch --> AddSwitch["Add Switches (Insert new lambda_a)"]
    AddSwitch --> Mux["Multiplexer"]
    Mux --> Output["Multiplexed Output"]
    
    DropSwitch ===>|Drop Port| Dropped["Dropped Channels"]
    Added["Added Channels"] ===>|Add Port| AddSwitch
    
    style Demux fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style Mux fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style DropSwitch fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style AddSwitch fill:#d2ffd2,stroke:#33cc33,stroke-width:2px,color:#000
```

---

## 5. OXC Wavelength Routing Architecture
This diagram illustrates an Optical Cross-Connect (OXC) mesh node, routing channels across multiple incoming and outgoing fibers.

* **File Name:** `oxc_routing.png`
* **Mermaid Code:**

```mermaid
graph LR
    FiberIn1["Fiber In 1"] --> Demux1["Demux"]
    FiberIn2["Fiber In 2"] --> Demux2["Demux"]
    
    Demux1 --> Crossbar["Optical Switch Fabric (OXC Space Switch Matrix)"]
    Demux2 --> Crossbar
    
    Crossbar --> Mux1["Mux"]
    Crossbar --> Mux2["Mux"]
    
    Mux1 --> FiberOut1["Fiber Out 1"]
    Mux2 --> FiberOut2["Fiber Out 2"]
    
    style Crossbar fill:#f9f7ed,stroke:#d79b00,stroke-width:2px,color:#000
```

---

## 6. SONET Protocol Layer Stack
This diagram shows the four-layer protocol stack of SONET, from the Path layer down to the Photonic layer.

* **File Name:** `sonet_layers.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "SONET Protocol Stack"
        Path["Path Layer (End-to-End Payload Assembly)"]
        Line["Line Layer (Multiplexing & Protection)"]
        Section["Section Layer (Framing & Scrambling)"]
        Photonic["Photonic Layer (Physical/Optical Transceiver)"]
        
        Path ===> Line ===> Section ===> Photonic
    end
    
    style Path fill:#dae8fc,stroke:#6c8ebf,color:#000
    style Line fill:#ffe6cc,stroke:#d79b00,color:#000
    style Section fill:#e2f0d9,stroke:#385723,color:#000
    style Photonic fill:#f8cecc,stroke:#b85450,color:#000
```
