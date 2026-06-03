# Chapter 9 Diagrams

---

## 1. PCB Design to Mass Manufacturing Pipeline
* **File Name:** `pcb_manufacturing_pipeline.png`

```mermaid
flowchart TD
    S1["[1] Schematic Capture<br>Define components and connections<br>in EDA tool"]
    S2["[2] PCB Layout<br>Route copper traces, place<br>components, define layers"]
    S3["[3] Design Rule Check<br>Validate trace widths, clearances,<br>and via sizes"]
    S4["[4] Gerber File Generation<br>Export manufacturing files<br>for each PCB layer"]
    S5["[5] PCB Fabrication<br>Etching, drilling, solder mask,<br>silkscreen printing"]
    S6["[6] Component Assembly<br>SMT pick-and-place, reflow<br>soldering, through-hole wave"]
    S7["[7] Testing and QA<br>AOI, ICT, functional test,<br>burn-in validation"]

    S1 --> S2 --> S3 --> S4 --> S5 --> S6 --> S7

    style S1 fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style S2 fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style S3 fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style S4 fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style S5 fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style S6 fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style S7 fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. IoT Product Testing Pyramid
* **File Name:** `iot_testing_pyramid.png`

```mermaid
flowchart TD
    Top["IoT Product Testing"]
    
    Top --> HW["Hardware Testing<br>- ESD/EMI susceptibility<br>- Thermal cycling<br>- Drop/vibration tests"]
    Top --> SW["Software/Firmware Testing<br>- Unit tests (sensor drivers)<br>- Integration tests (full stack)<br>- Regression tests"]
    Top --> CONN["Connectivity Testing<br>- Wi-Fi range and throughput<br>- BLE pairing stability<br>- MQTT QoS delivery"]
    Top --> SEC["Security Testing<br>- Penetration testing<br>- Firmware binary analysis<br>- TLS certificate validation"]
    Top --> UAT["User Acceptance Testing<br>- Onboarding flow usability<br>- Mobile app UX evaluation<br>- Real-world field trials"]

    style Top fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style HW fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style SW fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style CONN fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style SEC fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style UAT fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```
