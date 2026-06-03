# Chapter 2 Diagrams: Controller Tuning & Implementation

This file contains the Mermaid diagram codes for Chapter 2. These codes can be rendered in the Mermaid Editor (local or online) to export high-quality PNGs to this directory.

---

## 1. Servo vs. Regulatory Control Loops
* **File Name:** `servo_regulatory.png`

```mermaid
flowchart TD
    subgraph ServoLoop ["Servo Operation: Setpoint (SP) Tracking"]
        SP1["Setpoint Change: R(s)"] --> Sum1(( ))
        PV1[Process Variable] -->|Feedback| Sum1
        Sum1 -->|"Error E(s)"| Ctrl1[Controller]
        Ctrl1 --> Act1[Control Valve]
        Act1 --> Proc1[Process G_p]
        Proc1 --> PV1
    end

    subgraph RegLoop ["Regulatory Operation: Disturbance Rejection"]
        SP2["Constant Setpoint: R(s)"] --> Sum2(( ))
        PV2[Process Variable] -->|Feedback| Sum2
        Sum2 --> Error2[Error]
        Error2 --> Ctrl2[Controller]
        Ctrl2 --> Act2[Control Valve]
        Dist["Load Disturbance: D(s)"] --> SumDist((+))
        Act2 --> SumDist
        SumDist --> Proc2[Process G_p]
        Proc2 --> PV2
    end

    style ServoLoop fill:none,stroke:#0066cc,stroke-width:2px
    style RegLoop fill:none,stroke:#009900,stroke-width:2px
    style Dist fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
```

---

## 2. Inverting OP-AMP Proportional (P) Controller
* **File Name:** `opamp_p_controller.png`

```mermaid
graph LR
    subgraph P_Ctrl ["Proportional Controller Circuit"]
        Vin["Input Voltage: V_in"] -->|R_in| Nodes(( ))
        Nodes -->|Inverting Input| OpAmp["OP-AMP (-/+)"]
        Gnd["Ground (Non-inverting Input)"] -->|0 V| OpAmp
        OpAmp --> Vout["Output Voltage: V_out = -(R_f/R_in) * V_in"]
        Nodes <-->|R_f| Vout
    end

    style P_Ctrl fill:none,stroke:#333,stroke-width:2px
    style OpAmp fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 3. Integrating OP-AMP Integral (I) Controller
* **File Name:** `opamp_i_controller.png`

```mermaid
graph LR
    subgraph I_Ctrl ["Integral Controller Circuit"]
        Vin["Input Voltage: V_in"] -->|R| Nodes(( ))
        Nodes -->|Inverting Input| OpAmp["OP-AMP (-/+)"]
        Gnd["Ground (Non-inverting Input)"] -->|0 V| OpAmp
        OpAmp --> Vout["Output Voltage: V_out = -1/(R*C) * integral(V_in dt)"]
        Nodes <-->|C| Vout
    end

    style I_Ctrl fill:none,stroke:#333,stroke-width:2px
    style OpAmp fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 4. Differentiating OP-AMP Derivative (D) Controller
* **File Name:** `opamp_d_controller.png`

```mermaid
graph LR
    subgraph D_Ctrl ["Derivative Controller Circuit"]
        Vin["Input Voltage: V_in"] -->|C| Nodes(( ))
        Nodes -->|Inverting Input| OpAmp["OP-AMP (-/+)"]
        Gnd["Ground (Non-inverting Input)"] -->|0 V| OpAmp
        OpAmp --> Vout["Output Voltage: V_out = -R*C * (dV_in/dt)"]
        Nodes <-->|R| Vout
    end

    style D_Ctrl fill:none,stroke:#333,stroke-width:2px
    style OpAmp fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 5. OP-AMP Proportional-Integral (PI) Controller
* **File Name:** `opamp_pi_controller.png`

```mermaid
graph LR
    subgraph PI_Ctrl ["PI Controller Circuit"]
        Vin["Input Voltage: V_in"] -->|R_1| Nodes(( ))
        Nodes -->|Inverting Input| OpAmp["OP-AMP (-/+)"]
        Gnd["Ground (Non-inverting Input)"] -->|0 V| OpAmp
        OpAmp --> Vout["Output Voltage: V_out"]
        Nodes <-->|R_f in series with C_f| Vout
    end

    style PI_Ctrl fill:none,stroke:#333,stroke-width:2px
    style OpAmp fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 6. OP-AMP Proportional-Derivative (PD) Controller
* **File Name:** `opamp_pd_controller.png`

```mermaid
graph LR
    subgraph PD_Ctrl ["PD Controller Circuit"]
        Vin["Input Voltage: V_in"] -->|R_1 in parallel with C_1| Nodes(( ))
        Nodes -->|Inverting Input| OpAmp["OP-AMP (-/+)"]
        Gnd["Ground (Non-inverting Input)"] -->|0 V| OpAmp
        OpAmp --> Vout["Output Voltage: V_out"]
        Nodes <-->|R_f| Vout
    end

    style PD_Ctrl fill:none,stroke:#333,stroke-width:2px
    style OpAmp fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 7. Parallel OP-AMP PID Controller
* **File Name:** `opamp_pid_parallel.png`

```mermaid
graph TD
    subgraph PID_Parallel ["Parallel OP-AMP PID Controller Structure"]
        Vin["Error Input Voltage: V_in"]
        
        Vin --> P_Stage["Proportional Stage <br> (Inverting Amp: -K_p)"]
        Vin --> I_Stage["Integral Stage <br> (Integrator Amp: -1/s*tau_I)"]
        Vin --> D_Stage["Derivative Stage <br> (Differentiator Amp: -s*tau_D)"]
        
        P_Stage --> Sum["Summing Amplifier <br> (Adds and Inverts to restore phase)"]
        I_Stage --> Sum
        D_Stage --> Sum
        
        Sum --> Vout["PID Output Voltage: V_out"]
    end

    style PID_Parallel fill:none,stroke:#333,stroke-width:2px
    style Sum fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style P_Stage fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style I_Stage fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style D_Stage fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
```

---

## 8. Pneumatic PID Controller Architecture
* **File Name:** `pneumatic_pid.png`

```mermaid
graph TD
    subgraph PneumaticPID ["Pneumatic PID Flapper-Nozzle System"]
        Error["Input Deviation (Displacement)"] --> Baffle["Flapper / Baffle Position"]
        Nozzle["Nozzle Pressure"] --> Relay["Booster Volume Relay"]
        Relay --> Output["Pneumatic Control Output (3 - 15 psi)"]
        
        Output --> PropBellows["Proportional feedback bellows"]
        Output --> ResetBellows["Reset feedback bellows <br> (connected via adjustable restriction R)"]
        
        PropBellows -.->|"Negative Feedback (Opposes Baffle)"| Baffle
        ResetBellows -.->|"Positive Feedback (Cancels Prop)"| Baffle
    end

    Baffle <-->|"Nozzle-Flapper Gap"| Nozzle
    
    style PneumaticPID fill:none,stroke:#333,stroke-width:2px
    style Relay fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style PropBellows fill:#e6f2ff,stroke:#0066cc,stroke-width:1px,color:#000
    style ResetBellows fill:#ffffe6,stroke:#cccc00,stroke-width:1px,color:#000
```

---

## 9. Ziegler-Nichols Process Reaction Curve (Open Loop)
* **File Name:** `zn_open_loop.png`

```mermaid
flowchart TD
    subgraph PRC ["Open Loop Step Response (Process Reaction Curve)"]
        Start["Step Input Applied at t=0"] --> S_Curve["S-Shaped Response of PV"]
        S_Curve --> Tangent["Inflection Point Tangent Line"]
        
        subgraph Params ["Extracted Tuning Parameters"]
            L["Dead Time (L): Tangent intercept with time axis"]
            T["Time Constant (T): Tangent intercept with final value"]
            R["Reaction Rate (R = dPV/dt): Slope of tangent"]
        end
    end

    Tangent --- Params
    
    style PRC fill:none,stroke:#333,stroke-width:2px
    style Params fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
```

---

## 10. Ziegler-Nichols Ultimate Gain Method (Closed Loop)
* **File Name:** `zn_closed_loop.png`

```mermaid
flowchart TD
    subgraph UltimateMethod ["Closed Loop Ultimate Gain Method"]
        P_Only["1. Set Controller to Proportional-Only (I=0, D=0)"]
        IncreaseGain["2. Increase Gain K_c until sustained oscillations occur"]
        
        subgraph Params ["Extracted Tuning Parameters"]
            Ku["Ultimate Gain (K_u): Gain that caused sustained oscillation"]
            Pu["Ultimate Period (P_u): Time period of one full oscillation cycle"]
        end
        
        P_Only --> IncreaseGain
        IncreaseGain --> Params
    end

    style UltimateMethod fill:none,stroke:#333,stroke-width:2px
    style Params fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
```

---

## 11. Quarter-Amplitude Decay Waveform
* **File Name:** `quarter_decay.png`

```mermaid
graph TD
    subgraph DecayWave ["Quarter-Amplitude Decay Response"]
        Peak1["Peak 1: Amplitude = A1"] --> Decay["Damped Transient Oscillations"]
        Decay --> Peak2["Peak 2: Amplitude = A2"]
        
        Ratio["Decay Ratio: A2 / A1 = 1 / 4"]
    end
    
    Peak1 --- Ratio
    Peak2 --- Ratio

    style DecayWave fill:none,stroke:#333,stroke-width:2px
    style Ratio fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
```

---

## 12. Parallel PID Control Loop Block Diagram
* **File Name:** `pid_block_diagram.png`

```mermaid
flowchart LR
    SP["Setpoint: R(s)"] --> Sum(( ))
    PV["Process Variable: Y(s)"] -->|Feedback| Sum
    
    Sum -->|"Error E(s)"| P_Branch["Proportional: K_c"]
    Sum -->|"Error E(s)"| I_Branch["Integral: K_c / (s * tau_I)"]
    Sum -->|"Error E(s)"| D_Branch["Derivative: K_c * s * tau_D"]
    
    P_Branch --> SumPID((+))
    I_Branch --> SumPID
    D_Branch --> SumPID
    
    SumPID -->|"Control Value U(s)"| Process["Process G_p(s)"]
    Process --> PV

    style Sum fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style SumPID fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style Process fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```
