# Chapter 1 Diagrams

---

## 1. WWW vs. IoT Comparison
* **File Name:** `www_vs_iot.png`

```mermaid
flowchart LR
    %% WWW Section
    subgraph WWW ["World Wide Web (WWW) - Human Centric"]
        H[Human] <-->|Browser / HTTP| PC[Computer / Server]
        style WWW fill:none,stroke:#8a8aff,stroke-width:2px
    end

    %% IoT Section
    subgraph IoT ["Internet of Things (IoT) - Machine Centric"]
        D1[Physical Device / Sensor] <-->|API / CoAP / MQTT| D2[Device / Gateway / Cloud]
        style IoT fill:none,stroke:#8aff8a,stroke-width:2px
    end
    
    classDef default fill:#fff,stroke:#333,stroke-width:1px,color:#000;
```

---

## 2. ETSI M2M Functional Architecture
* **File Name:** `etsi_m2m_architecture.png`

```mermaid
graph TD
    %% Application Layer
    subgraph APP ["Application Layer"]
        DA[Device/Gateway Application]
        NA[Network Application]
    end

    %% Service Capability Layer
    subgraph SCL ["Service Capability Layer (SCL)"]
        subgraph NSCL_Box ["Network SCL"]
            NSCL["Services: SEC, DMS, TR, DIA, COM"]
        end
    end

    %% Device/Gateway Layer
    subgraph DEV ["Device / Gateway Layer"]
        MD[M2M Device]
        MG[M2M Gateway]
    end

    %% Connections
    DA -- "dIa Interface" --> NSCL
    NA -- "mIa Interface" --> NSCL
    MD -- "mId Interface" --> NSCL
    MG -- "mId Interface" --> NSCL
    MD <-->|Local Link| MG

    %% Styling
    style APP fill:none,stroke:#ff9933,stroke-width:2px
    style SCL fill:none,stroke:#3399ff,stroke-width:2px
    style DEV fill:none,stroke:#6666ff,stroke-width:2px
```

---

## 3. OGC Functional Architecture
* **File Name:** `ogc_architecture.png`

```mermaid
graph TD
    SOS["Sensor Observation Service (SOS) <br> (API Layer / XML Requests)"]
    SensorML["Sensor Model Language (SensorML) <br> (Metadata & Configuration Schemas)"]
    Sensors["Sensing Layer Node <br> (Physical Sensors in the Field)"]

    SOS -->|Queries Sensor Description| SensorML
    SensorML -->|Defines Schema for| Sensors
    Sensors -->|Sends Raw Sensor Data| SOS
    
    style SOS fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
    style SensorML fill:#ffffe6,stroke:#cccc00,stroke-width:2px,color:#000
    style Sensors fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
```

---

## 4. Information-Driven Value Chain
* **File Name:** `information_value_chain.png`

```mermaid
flowchart LR
    PW["[1] Physical World<br>(Raw State: Temp/Press)"]
    S["[2] Sense<br>(Sensors: Digitalize Signal)"]
    T["[3] Transmit<br>(Networks: Data Packets)"]
    SA["[4] Store/Analyze<br>(Cloud: DB & Analytics)"]
    DA["[5] Decide/Act<br>(Actuators: Valves/Alarms)"]

    PW --> S
    S --> T
    T --> SA
    SA --> DA

    style PW fill:#f2f2f2,stroke:#666,stroke-width:2px,color:#000
    style S fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style T fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style SA fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    style DA fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
```
