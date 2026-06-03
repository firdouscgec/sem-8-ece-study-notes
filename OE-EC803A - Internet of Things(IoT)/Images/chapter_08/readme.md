# Chapter 8 Diagrams

---

## 1. Business Model Canvas for IoT Startups
* **File Name:** `business_model_canvas.png`

```mermaid
flowchart TD
    subgraph Canvas ["Business Model Canvas"]
        direction TB
        KP["Key Partners<br>Component suppliers, Cloud providers,<br>Contract manufacturers"]
        KA["Key Activities<br>Firmware development, Hardware design,<br>Cloud platform maintenance"]
        KR["Key Resources<br>Engineering team, IP/Patents,<br>Prototyping lab"]
        VP["Value Proposition<br>What unique problem does<br>the IoT product solve?"]
        CR["Customer Relationships<br>Self-service app, Community forums,<br>Dedicated support"]
        CH["Channels<br>Online store, Retail partners,<br>Direct B2B sales"]
        CS["Customer Segments<br>Consumer, Enterprise,<br>Industrial"]
        COST["Cost Structure<br>R&D, Manufacturing, Cloud hosting,<br>Certification, Marketing"]
        REV["Revenue Streams<br>Hardware sales, Subscription SaaS,<br>Data licensing, Freemium"]
    end

    KP --> KA
    KA --> VP
    KR --> VP
    VP --> CR
    VP --> CH
    CR --> CS
    CH --> CS
    CS --> REV
    KP --> COST
    KA --> COST

    style Canvas fill:none,stroke:#333,stroke-width:1px
    style VP fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style CS fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style REV fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style COST fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. Embedded Code Optimization Priorities
* **File Name:** `embedded_optimization.png`

```mermaid
flowchart LR
    subgraph Priorities ["Embedded Code Optimization Priorities"]
        direction TB
        MEM["Memory Management<br>- Stack vs Heap allocation<br>- Avoid malloc/free in loops<br>- Use fixed-size buffers"]
        PERF["Performance<br>- Minimize blocking delays<br>- Use interrupt-driven I/O<br>- Optimize hot loops"]
        BAT["Battery / Power<br>- Deep sleep modes<br>- Reduce radio duty cycle<br>- Lower clock speed when idle"]
        LIB["Library Selection<br>- Prefer lightweight libs<br>- Avoid bloated frameworks<br>- Audit memory footprint"]
    end

    MEM --> PERF --> BAT --> LIB

    style Priorities fill:none,stroke:#666,stroke-width:1px
    style MEM fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style PERF fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style BAT fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style LIB fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```
