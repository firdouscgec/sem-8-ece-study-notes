# Chapter 4 Diagrams

---

## 1. Cost vs. Ease of Prototyping Curve
* **File Name:** `cost_vs_ease.png`

```mermaid
flowchart TD
    S1["[1] Sketching & Paper Mockups<br>Cost: Near Zero<br>Ease: Infinite<br>Flexibility: Maximum"]
    S2["[2] Breadboarding (Arduino/Pi)<br>Cost: Low<br>Ease: High<br>Flexibility: High"]
    S3["[3] Engineering Prototype (3D Print + PCB)<br>Cost: Medium<br>Ease: Medium<br>Flexibility: Moderate"]
    S4["[4] Pilot/Pre-Production Run<br>Cost: High<br>Ease: Low<br>Flexibility: Low"]
    S5["[5] Mass Manufacture (Injection Molding)<br>Cost: Extreme<br>Ease: Zero (Rigid)<br>Flexibility: Zero"]
    
    S1 -->|Validate Concept| S2
    S2 -->|Refine Electronics| S3
    S3 -->|Field Trials| S4
    S4 -->|Tooling & Production Freeze| S5

    style S1 fill:#d5e8d4,stroke:#82b366,stroke-width:2px,color:#000
    style S2 fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style S3 fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style S4 fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style S5 fill:#e1d5e7,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. Open Source vs. Closed Source Prototyping Ecosystems
* **File Name:** `open_vs_closed_source.png`

```mermaid
flowchart LR
    subgraph OpenSource ["Open-Source Prototyping"]
        direction TB
        OH["Open Hardware<br>(Arduino, ESP32, Raspberry Pi)"]
        OS["Open Software<br>(Linux OS, GitHub, FreeRTOS)"]
        OC["Community Support<br>(Forums, Open Libraries, Stack Overflow)"]
        
        OH <--> OS
        OS <--> OC
    end
    
    subgraph ClosedSource ["Closed-Source Prototyping"]
        direction TB
        PH["Proprietary Hardware<br>(Custom Silicon, NDA Modules)"]
        PS["Proprietary Software<br>(Commercial SDKs, Licensed IDEs)"]
        PC["Vendor Support<br>(Direct SLA, NDA Technical Teams)"]
        
        PH <--> PS
        PS <--> PC
    end

    style OpenSource fill:none,stroke:#82b366,stroke-width:2px
    style ClosedSource fill:none,stroke:#b85450,stroke-width:2px
    style OH fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style OS fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style OC fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style PH fill:#f8cecc,stroke:#b85450,stroke-width:1px,color:#000
    style PS fill:#f8cecc,stroke:#b85450,stroke-width:1px,color:#000
    style PC fill:#f8cecc,stroke:#b85450,stroke-width:1px,color:#000
```
