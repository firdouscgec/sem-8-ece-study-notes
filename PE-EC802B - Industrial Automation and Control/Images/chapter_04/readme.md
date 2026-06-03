# Chapter 4 Diagrams: Advanced Control Techniques

This file contains the Mermaid diagram codes for Chapter 4. These codes can be rendered in the Mermaid Editor (local or online) to export high-quality PNGs to this directory.

---

## 1. Feedforward Control System Block Diagram
* **File Name:** `feedforward_block.png`

```mermaid
flowchart LR
    Dist["Load Disturbance: D(s)"] --> G_d["Disturbance Dynamics: G_d(s)"]
    Dist --> G_ff["Feedforward Controller: G_ff(s)"]
    
    G_ff -->|"Control Action U_ff(s)"| Sum((+))
    SP["Setpoint: R(s)"] --> Sum
    
    Sum -->|"Valves Control Signal"| G_v["Control Valve: G_v(s)"]
    G_v --> G_p["Process Dynamics: G_p(s)"]
    
    G_p --> SumProcess((+))
    G_d --> SumProcess
    
    SumProcess --> PV["Controlled Variable: Y(s)"]

    style Sum fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style SumProcess fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style Dist fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
```

---

## 2. Feedback vs. Feedforward Control Loop Comparison
* **File Name:** `feedback_vs_feedforward.png`

```mermaid
flowchart TD
    subgraph Feedback ["Feedback Control (Reactive/Post-error)"]
        Sens1[Sensor] -->|"Measure Output Y(s)"| Ctrl1[Feedback Controller]
        Ctrl1 -->|"Adjust Valve Output"| Valve1[Valve]
        Valve1 --> Proc1[Process]
        Proc1 -->|"Error occurs first!"| Sens1
        Dist1["Disturbance D(s)"] --> Proc1
    end

    subgraph Feedforward ["Feedforward Control (Proactive/Pre-error)"]
        Dist2["Disturbance D(s)"] -->|"Measure Disturbance"| Sens2[Disturbance Sensor]
        Sens2 --> Ctrl2[Feedforward Controller]
        Ctrl2 -->|"Adjust Valve before error"| Valve2[Valve]
        Valve2 --> Proc2[Process]
        Dist2 --> Proc2
    end

    style Feedback fill:none,stroke:#0066cc,stroke-width:2px
    style Feedforward fill:none,stroke:#009900,stroke-width:2px
    style Dist2 fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
```

---

## 3. Cascade Control Loop Block Diagram
* **File Name:** `cascade_block.png`

```mermaid
flowchart TD
    SP["Primary Setpoint: R_1(s)"] --> Sum1(( ))
    PV1["Primary Process Variable: Y_1(s)"] -->|Outer Feedback| Sum1
    
    Sum1 -->|"Primary Error"| Ctrl1["Master (Primary) Controller: G_c1(s)"]
    
    Ctrl1 -->|"Secondary Setpoint: R_2(s)"| Sum2(( ))
    PV2["Secondary Process Variable: Y_2(s)"] -->|"Inner Feedback"| Sum2
    
    Sum2 -->|"Secondary Error"| Ctrl2["Slave (Secondary) Controller: G_c2(s)"]
    
    Ctrl2 --> Valve["Control Valve / Actuator"]
    
    Dist2["Inner Disturbance: D_2(s)"] --> SumDist((+))
    Valve --> SumDist
    SumDist --> Proc2["Secondary Process: G_p2(s)"]
    Proc2 --> PV2
    
    Dist1["Outer Disturbance: D_1(s)"] --> SumDistOuter((+))
    Proc2 --> SumDistOuter
    SumDistOuter --> Proc1["Primary Process: G_p1(s)"]
    Proc1 --> PV1

    style Sum1 fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style Sum2 fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style Dist2 fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
```

---

## 4. Ratio Control System (Multiplier Scheme)
* **File Name:** `ratio_control.png`

```mermaid
flowchart TD
    WildFlow["Uncontrolled 'Wild' Flow: F_W"] --> FT1["Flow Transmitter 1"]
    FT1 -->|"Wild Flow Signal (F_W)"| Multiplier["Ratio Station (x R)"]
    
    Multiplier -->|"Controlled Setpoint: F_C* = R * F_W"| Ctrl["Controlled Flow Controller"]
    
    ContFlow["Controlled Flow: F_C"] --> FT2["Flow Transmitter 2"]
    FT2 -->|"Controlled Flow Signal (F_C)"| Ctrl
    
    Ctrl -->|"Valve Control Signal"| Valve["Control Valve"]
    Valve --> ContFlow

    style Multiplier fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
    style Ctrl fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
```

---

## 5. Split-Range (Duplex) Control Loop Graph
* **File Name:** `split_range.png`

```mermaid
flowchart TD
    subgraph SplitRanges ["Split-Range Valve Response to Controller Output (CO)"]
        A["CO: 0% to 50%"] -->|"Valve A (Heating) Closes: 100% to 0% <br> Valve B (Cooling) remains Closed (0%)"| Output1["Heating Range"]
        B["CO: 50% to 100%"] -->|"Valve A (Heating) remains Closed (0%) <br> Valve B (Cooling) Opens: 0% to 100%"| Output2["Cooling Range"]
    end

    style SplitRanges fill:none,stroke:#333,stroke-width:2px
    style Output1 fill:#ffe6e6,stroke:#cc0000,color:#000
    style Output2 fill:#e6f2ff,stroke:#0066cc,color:#000
```

---

## 6. Override (Selective) Control Loop
* **File Name:** `override_control.png`

```mermaid
flowchart LR
    PV_Flow["Flow Variable"] --> FlowCtrl["Flow Controller (FIC)"]
    PV_Press["Discharge Pressure"] --> PressCtrl["Pressure Controller (PIC) <br> (High Safety Override)"]
    
    FlowSP["Flow Setpoint"] --> FlowCtrl
    PressSP["Pressure Safety Limit"] --> PressCtrl
    
    FlowCtrl -->|"Normal Command: CO_1"| LowSelector{"Low Selector (LS)"}
    PressCtrl -->|"Override Command: CO_2"| LowSelector
    
    LowSelector -->|"Lowest Signal wins"| Valve["Discharge Control Valve"]
    Valve -->|"Throttles Flow & Pressure"| Output["Process Pipeline"]
    
    style LowSelector fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style PressCtrl fill:#ffffe6,stroke:#cccc00,stroke-width:1px,color:#000
```

---

## 7. Model Reference Adaptive Control (MRAC)
* **File Name:** `mrac_block.png`

```mermaid
graph TD
    subgraph MRAC_Loop ["Model Reference Adaptive Control Architecture"]
        Setpoint["Setpoint: R(s)"]
        RefModel["Reference Model: G_m(s) <br> (Specifies ideal process response)"]
        Controller["Adjustable Controller"]
        Process["Actual Process: G_p(s)"]
        
        SumDiff(( ))
        AdjMechanism["Adjustment Mechanism <br> (Parameter adaptation algorithm)"]
    end
    
    Setpoint --> RefModel
    Setpoint --> Controller
    Controller --> Process
    
    RefModel -->|"Ideal Y_m"| SumDiff
    Process -->|"Actual Y"| SumDiff
    SumDiff -->|"Error e_m = Y - Y_m"| AdjMechanism
    
    AdjMechanism -->|"Update Controller Gains"| Controller

    style MRAC_Loop fill:none,stroke:#333,stroke-width:2px
    style RefModel fill:#e6f2ff,stroke:#0066cc,color:#000
    style AdjMechanism fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
```

---

## 8. Self-Tuning Regulator (STR)
* **File Name:** `str_block.png`

```mermaid
graph TD
    subgraph STR_Loop ["Self-Tuning Regulator (STR) Architecture"]
        Setpoint["Setpoint: R(s)"]
        Controller["Adjustable Controller"]
        Process["Actual Process: G_p(s)"]
        
        Estimator["Parameter Estimator <br> (Recursive Least Squares - RLS)"]
        DesignCalc["Controller Design Block <br> (Re-calculates gains dynamically)"]
    end
    
    Setpoint --> Controller
    Controller -->|"Control Value u(t)"| Process
    Process -->|"Output y(t)"| Estimator
    Controller -->|"Input u(t)"| Estimator
    
    Estimator -->|"Estimated Process Parameters"| DesignCalc
    DesignCalc -->|"Adjust Controller Parameters"| Controller

    style STR_Loop fill:none,stroke:#333,stroke-width:2px
    style Estimator fill:#ffe6e6,stroke:#cc0000,color:#000
    style DesignCalc fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
```

---

## 9. Internal Model Control (IMC) Block Diagram
* **File Name:** `imc_block.png`

```mermaid
flowchart LR
    SP["Setpoint: R(s)"] --> SumOuter(( ))
    
    SumOuter -->|"Adjusted Setpoint"| Controller["IMC Controller: Q(s)"]
    Controller -->|"Control Value U(s)"| Process["Actual Process: G_p(s)"]
    Controller -->|"Control Value U(s)"| Model["Internal Process Model: Gm(s)"]
    
    Process -->|"Actual Y(s)"| SumDist((+))
    Dist["Disturbance: D(s)"] --> SumDist
    
    Model -->|"Predicted Ym(s)"| SumFeedback(( ))
    SumDist -->|"Actual Output Y"| SumFeedback
    
    SumFeedback -->|"Estimated Disturbance: d"| SumOuter
    
    style SumOuter fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style SumFeedback fill:#ffe6e6,stroke:#cc0000,stroke-width:1px,color:#000
    style Model fill:#ffffe6,stroke:#cccc00,stroke-width:1px,color:#000
```
