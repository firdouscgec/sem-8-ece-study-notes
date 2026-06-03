# Chapter 5 Diagrams

---

## 1. Comparison of Physical Prototyping Methods
* **File Name:** `physical_prototyping_methods.png`

```mermaid
flowchart TD
    Methods["Physical Prototyping Methods"]
    
    Methods --> Additive["Additive Manufacturing"]
    Methods --> Subtractive25D["Subtractive (2.5D)"]
    Methods --> Subtractive3D["Subtractive (3D)"]
    Methods --> NonDigital["Non-Digital / Manual"]
    
    Additive --> TDPrint["3D Printing (FDM / SLA)<br>- Adds material layer-by-layer<br>- Complex internal voids<br>- PLA, ABS, Resin"]
    Subtractive25D --> LC["Laser Cutting<br>- Cuts flat sheets via laser beam<br>- Fast assembly of slot-boxes<br>- Acrylic, MDF, Cardboard"]
    Subtractive3D --> CNC["CNC Milling<br>- Carves 3D shapes from block<br>- Heavy tolerance & strength<br>- Aluminum, Wood, Delrin"]
    NonDigital --> RR["Repurposing / Recycling<br>- Adapts existing casings<br>- Fast, cheap, eco-friendly<br>- Plastic boxes, old toys"]
    
    style Methods fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style Additive fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Subtractive25D fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Subtractive3D fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style NonDigital fill:#e1d5e7,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. IoT Antenna Types & Placement Selection Criteria
* **File Name:** `iot_antenna_types.png`

```mermaid
flowchart TD
    Antenna["IoT Antenna Types"]
    
    Antenna --> Chip["1. Ceramic Chip Antenna<br>- Size: Ultra-compact (mm size)<br>- Cost: Low<br>- Range: Short-to-Medium<br>- Ideal: Wearables, space-constrained"]
    
    Antenna --> Trace["2. PCB Trace Antenna<br>- Size: Medium (board area)<br>- Cost: Zero (copper trace)<br>- Range: Medium<br>- Ideal: High-volume consumer IoT"]
    
    Antenna --> Wire["3. Simple Wire Antenna<br>- Size: Protruding (1/4 wavelength)<br>- Cost: Extremely Low (soldered wire)<br>- Range: Medium<br>- Ideal: Basic smart home nodes"]
    
    Antenna --> Whip["4. External Whip/SMA Antenna<br>- Size: Large (external mount)<br>- Cost: High<br>- Range: Maximum (high gain)<br>- Ideal: Gateways, outdoor nodes"]
    
    subgraph Selection ["Selection & Placement Criteria"]
        direction TB
        C1["Ground Plane Clearance (Required for Chip/Trace)"]
        C2["Avoid Metal Enclosures & Batteries (Blocks RF)"]
        C3["Select matching impedance (typically 50 Ohms)"]
        C4["Orientation/Polarization alignment"]
    end
    
    Chip --> Selection
    Trace --> Selection
    Wire --> Selection
    Whip --> Selection
    
    style Antenna fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style Chip fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Trace fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Wire fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style Whip fill:#e1d5e7,stroke:#b85450,stroke-width:2px,color:#000
    style Selection fill:#f2f2f2,stroke:#666,stroke-width:1px
```
