# Chapter 1 Diagrams: Sensors, Actuators & Signal Conditioning

This file contains the Mermaid diagram codes for Chapter 1. These codes can be rendered in the Mermaid Editor (local or online) to export high-quality PNGs to this directory.

---

## 1. LVDT Electro-Mechanical Schematic
* **File Name:** `lvdt_schematic.png`

```mermaid
graph TD
    subgraph LVDT ["Linear Variable Differential Transformer (LVDT) Structure"]
        Core["Magnetic Core (Movable Shaft)"]
        
        subgraph Windings ["Coil Windings"]
            P["Primary Winding (V_in: AC Excitation)"]
            S1["Secondary Winding 1 (V_S1)"]
            S2["Secondary Winding 2 (V_S2)"]
        end
        
        Output["Differential Output: V_out = V_S1 - V_S2"]
    end
    
    Core -.->|Displacement x| Windings
    P -->|Magnetic Coupling| S1
    P -->|Magnetic Coupling| S2
    S1 --> Output
    S2 -->|Series Opposition| Output

    style LVDT fill:none,stroke:#333,stroke-width:2px
    style Core fill:#ffcccc,stroke:#cc0000,stroke-width:2px,color:#000
    style Windings fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style Output fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 2. LVDT Transfer Characteristics
* **File Name:** `lvdt_transfer_char.png`

```mermaid
flowchart TD
    subgraph Graph ["LVDT Output Magnitude & Phase vs. Position"]
        A["-x (Max Left Displacement)"] <-->|"V_out In-Phase with V_in"| B["0 (Null Position: V_out = 0)"]
        B <-->|"V_out Out-of-Phase (180 deg)"| C["+x (Max Right Displacement)"]
        
        subgraph Behavior ["Transfer Response"]
            Direction1["Core Left: V_S1 > V_S2 <br> V_out = V_S1 - V_S2 (In-phase)"]
            Direction2["Core Center: V_S1 = V_S2 <br> V_out = 0 (Residual Null Voltage)"]
            Direction3["Core Right: V_S2 > V_S1 <br> V_out = V_S2 - V_S1 (180 deg out-of-phase)"]
        end
    end
    
    A --- Direction1
    B --- Direction2
    C --- Direction3
    
    style Graph fill:none,stroke:#333,stroke-width:2px
    style Behavior fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
```

---

## 3. Thermocouple & Cold Junction Compensation
* **File Name:** `thermocouple_compensation.png`

```mermaid
graph LR
    subgraph TC_Comp ["Thermocouple Cold Junction Compensation Circuit"]
        subgraph Hot ["Hot Junction (T_h)"]
            J_meas["Measuring Junction <br> (Metal A / Metal B Join)"]
        end
        
        subgraph Cold ["Cold Junction (T_c)"]
            J_ref1["Reference Junction 1"]
            J_ref2["Reference Junction 2"]
        end
        
        Comp["Compensating Circuit <br> (RTD / Thermistor / IC Sensor) <br> Generates V_comp = V(T_c - T_0)"]
        Meter["Measuring Instrument <br> (V_net = V_TC + V_comp <br> Proportional to T_h relative to 0 °C)"]
    end
    
    J_meas -->|Metal A| J_ref1
    J_meas -->|Metal B| J_ref2
    J_ref1 --> Meter
    J_ref2 --> Comp
    Comp --> Meter
    
    style TC_Comp fill:none,stroke:#333,stroke-width:2px
    style Hot fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style Cold fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Comp fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
    style Meter fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 4. Ultrasonic Sensor Working Principle
* **File Name:** `ultrasonic_working.png`

```mermaid
flowchart LR
    subgraph Sensor ["Ultrasonic Transducer (10-65 kHz)"]
        TX["Transmitter <br> (Piezoelectric Crystal)"]
        RX["Receiver <br> (Piezoelectric Crystal)"]
    end
    
    subgraph Target ["Target Object"]
        Surface["Reflecting Surface"]
    end
    
    TX -->|1. Ultrasonic Pulse Burst| Surface
    Surface -->|2. Reflected Echo Wavelength| RX
    
    Note["Distance: D = (v * t) / 2 <br> v = Speed of Sound (~343 m/s) <br> t = Time-of-flight"]
    Sensor --- Note
    
    style Sensor fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Target fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style Note fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
```

---

## 5. Stepper Motor Drive Step Modes
* **File Name:** `stepper_half_micro.png`

```mermaid
graph TD
    subgraph StepModes ["Stepper Motor Excitation Modes"]
        subgraph FS ["Full-Step (2-Phase ON)"]
            A1["Step 1: AB (ON)"] --> A2["Step 2: BC (ON)"]
            A2 --> A3["Step 3: CD (ON)"]
            A3 --> A4["Step 4: DA (ON)"]
            A4 --> A1
        end
        
        subgraph HS ["Half-Step (1-Phase / 2-Phase Alternate)"]
            B1["Step 1: A"] --> B2["Step 2: AB"]
            B2 --> B3["Step 3: B"]
            B3 --> B4["Step 4: BC"]
            B4 --> B5["Step 5: C"]
            B5 --> B6["Step 6: CD"]
            B6 --> B7["Step 7: D"]
            B7 --> B8["Step 8: DA"]
            B8 --> B1
        end
        
        subgraph MS ["Micro-Stepping (Sine/Cosine Control)"]
            C1["Stator Current is modulated sinusoidally"]
            C2["Smooth rotation, high resolution, reduced resonance"]
            C1 --- C2
        end
    end
    
    style StepModes fill:none,stroke:#333,stroke-width:2px
    style FS fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style HS fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
    style MS fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
```

---

## 6. Pneumatic Spring-Diaphragm Actuator
* **File Name:** `pneumatic_actuator.png`

```mermaid
graph TD
    subgraph PA ["Pneumatic Actuator Assembly"]
        AirInlet["Control Air Pressure <br> (3 - 15 psi)"]
        Diaphragm["Flexible Diaphragm <br> (Converts Pressure to Force)"]
        Spring["Range Spring <br> (Opposes Diaphragm Motion)"]
        Stem["Actuator Stem <br> (Transfers Linear Displacement)"]
        Plug["Valve Plug & Seat <br> (Throttles Process Fluid)"]
    end
    
    AirInlet -->|Force = P * A| Diaphragm
    Diaphragm -->|Linear Movement| Stem
    Spring -.->|Opposes Force: F = k*x| Diaphragm
    Stem -->|Positions| Plug
    
    style PA fill:none,stroke:#333,stroke-width:2px
    style AirInlet fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Diaphragm fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
    style Spring fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style Stem fill:#f2f2f2,stroke:#666,stroke-width:2px,color:#000
    style Plug fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 7. Signal Conditioning Functional Architecture
* **File Name:** `signal_conditioning_block.png`

```mermaid
flowchart LR
    subgraph Input ["Physical Stage"]
        PV["Process Variable"]
        Sens["Sensor / Transducer"]
    end
    
    subgraph Conditioning ["Signal Conditioning Stage"]
        Prot["Protection <br> (Clamps/Fuses)"]
        Filt["Filtering <br> (LPF/HPF Active)"]
        Amp["Amplification <br> (Instrumentation Amp)"]
        Iso["Electrical Isolation <br> (Optocouplers)"]
    end
    
    subgraph Output ["Processing & Transmission"]
        ADC["ADC Converter"]
        MCU["Digital Controller <br> (PLC / DCS / PID)"]
    end
    
    PV --> Sens
    Sens -->|Low-level Signal| Prot
    Prot --> Filt
    Filt --> Amp
    Amp --> Iso
    Iso -->|Conditioned Analog| ADC
    ADC -->|Digital Bits| MCU
    
    style Input fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style Conditioning fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Output fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 8. Active Filter Circuit Topologies
* **File Name:** `opamp_filters.png`

```mermaid
graph TD
    subgraph Filters ["Active Filters (using OP-AMPs)"]
        LPF["Active LPF <br> (RC Low-Pass + Non-inverting Amplifier) <br> Passes f < f_c"]
        HPF["Active HPF <br> (CR High-Pass + Non-inverting Amplifier) <br> Passes f > f_c"]
        BPF["Active BPF <br> (Cascaded HPF + LPF or Multiple Feedback) <br> Passes f_L < f < f_H"]
        BRF["Active BRF (Notch) <br> (Parallel HPF/LPF Summer or Twin-T) <br> Rejects specific band"]
    end
    
    style LPF fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
    style HPF fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style BPF fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
    style BRF fill:#ffffe6,stroke:#cccc00,stroke-width:1px,color:#000
```

---

## 9. Sensor Protection Circuits
* **File Name:** `sensor_protection.png`

```mermaid
graph LR
    subgraph Protection ["Sensor Protection Schematics"]
        subgraph VClamp ["Overvoltage Protection"]
            In_V["High Voltage Spike"] --> Fuse["Fast-Blow Fuse / Resistor"]
            Fuse --> Zener["Zener Diode <br> (Clamps to V_z)"]
            Zener --> Out_Safe["Safe Voltage Output"]
            style Zener fill:#ffcccc,stroke:#cc0000,color:#000
        end
        
        subgraph Isol ["Galvanic Isolation"]
            TX_Sig["Sensor Current"] --> Opto_LED["Optocoupler LED <br> (Electrical to Light)"]
            Opto_LED -.->|Optical Path| Opto_Photo["Phototransistor <br> (Light to Electrical)"]
            Opto_Photo --> RX_Sig["Controller Input"]
            style Opto_LED fill:#e6f2ff,stroke:#0066cc,color:#000
            style Opto_Photo fill:#e6ffe6,stroke:#009900,color:#000
        end
    end
    
    style Protection fill:none,stroke:#333,stroke-width:2px
```

---

## 10. Measurement Error Taxonomy
* **File Name:** `error_classification.png`

```mermaid
graph TD
    Error["Total Measurement Error"]
    
    Error --> Systematic["Systematic Errors <br> (Determinate / Predictable)"]
    Error --> Random["Random Errors <br> (Indeterminate / Statistical)"]
    
    Systematic --> Inst["Instrumental Errors <br> (Calibration offset, wear)"]
    Systematic --> Env["Environmental Errors <br> (Temp, pressure, humidity effects)"]
    Systematic --> Obs["Observational Errors <br> (Parallax, incorrect reading)"]
    
    Random --> Noise["Electrical Noise & Fluctuations"]
    Random --> Quant["Resolution & Quantization Limits"]
    
    style Error fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style Systematic fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Random fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
```
