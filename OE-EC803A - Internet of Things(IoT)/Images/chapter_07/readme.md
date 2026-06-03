# Chapter 7 Diagrams

---

## 1. Cloud Computing in IoT Architecture
* **File Name:** `cloud_iot_architecture.png`

```mermaid
flowchart TD
    subgraph Devices ["IoT Device Layer"]
        direction LR
        S1["Sensor Node A"]
        S2["Sensor Node B"]
        GW["Edge Gateway"]
        S1 --> GW
        S2 --> GW
    end
    
    subgraph Cloud ["Cloud Computing Layer"]
        direction TB
        Ingest["Data Ingestion<br>MQTT Broker / REST API"]
        Store["Cloud Storage<br>NoSQL DB / Time-Series DB"]
        Compute["Cloud Compute<br>Analytics Engine / ML Models"]
        Dashboard["Dashboard / Visualization<br>Web App / Mobile App"]
        
        Ingest --> Store
        Store --> Compute
        Compute --> Dashboard
    end
    
    subgraph SmartGrid ["Smart Grid Application"]
        direction TB
        Meter["Smart Meter<br>Power consumption readings"]
        Grid["Grid Controller<br>Load balancing and peak shaving"]
        Consumer["Consumer App<br>Real-time billing and usage alerts"]
    end
    
    GW -->|"MQTT / HTTPS"| Ingest
    Compute -->|"Control Commands"| Grid
    Dashboard -->|"Usage Data"| Consumer
    Meter -->|"Metering Data"| GW

    style Devices fill:none,stroke:#82b366,stroke-width:2px
    style Cloud fill:none,stroke:#6c8ebf,stroke-width:2px
    style SmartGrid fill:none,stroke:#d79b00,stroke-width:2px
    style Ingest fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style Store fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style Compute fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style Dashboard fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
```

---

## 2. Big Data Analytics Pipeline for IoT
* **File Name:** `big_data_analytics.png`

```mermaid
flowchart LR
    Raw["Raw IoT<br>Data Streams"]
    
    Raw --> Desc["Descriptive Analytics<br>What happened?<br>Dashboards, Summaries"]
    Desc --> Diag["Diagnostic Analytics<br>Why did it happen?<br>Root Cause Analysis"]
    Diag --> Pred["Predictive Analytics<br>What will happen?<br>ML Models, Forecasting"]
    Pred --> Presc["Prescriptive Analytics<br>What should we do?<br>Automated Actions"]
    
    style Raw fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style Desc fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Diag fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Pred fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Presc fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```
