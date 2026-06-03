# Chapter 3 Diagrams: Automation Systems

This file contains the Mermaid diagram codes for Chapter 3. These codes can be rendered in the Mermaid Editor (local or online) to export high-quality PNGs to this directory.

---

## 1. PLC Hardware Architecture Block Diagram
* **File Name:** `plc_architecture.png`

```mermaid
graph TD
    subgraph PLC ["Programmable Logic Controller (PLC) Hardware System"]
        CPU["Central Processing Unit (CPU) <br> (Microprocessor & Control Logic)"]
        
        subgraph Mem ["Memory Unit"]
            SystemMem["System Memory <br> (OS / Firmware)"]
            UserMem["User Memory <br> (Program & Data Registers)"]
        end
        
        subgraph Power ["Power Supply"]
            PS["AC/DC Converter <br> (Provides 5V, 24V DC)"]
        end
        
        subgraph IO ["I/O Modules"]
            InputModule["Input Module <br> (Optoisolated Inputs)"]
            OutputModule["Output Module <br> (Relay/Triac/Transistor)"]
        end
        
        Loader["Programming Device <br> (PC / Handheld Terminal)"]
    end
    
    FieldSensors["Field Inputs <br> (Switches, Sensors)"] -->|24V DC / 120V AC| InputModule
    InputModule -->|Read Input Status| CPU
    CPU <-->|Read/Write Program & Data| UserMem
    CPU <-->|System Execution| SystemMem
    Loader <-->|Download / Monitor Code| CPU
    PS -->|Power Bus| CPU
    PS -->|Power Bus| IO
    CPU -->|Write Output Status| OutputModule
    OutputModule -->|Control Action| FieldActuators["Field Outputs <br> (Motors, Solenoid Valves)"]

    style PLC fill:none,stroke:#333,stroke-width:2px
    style CPU fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Mem fill:#ffffe6,stroke:#cccc00,stroke-width:1px,color:#000
    style IO fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
```

---

## 2. PLC Motor Start/Stop Latching Control (Ladder Logic)
* **File Name:** `motor_latch.png`

```mermaid
flowchart LR
    subgraph Ladder ["Motor Start/Stop Latching Logic (Rung 1)"]
        L1["Left Rail (L1)"]
        R1["Right Rail (L2)"]
        
        NC_Stop["NC Stop Button <br> [ ]/[ ] <br> I:0/1"]
        NO_Start["NO Start Button <br> [ ] <br> I:0/2"]
        NC_OL["NC Overload (OL) <br> [ ]/[ ] <br> I:0/3"]
        NC_Estop["NC Emergency Stop <br> [ ]/[ ] <br> I:0/0"]
        Coil["Motor Output Coil <br> ( ) <br> O:0/1"]
        Latch["NO Motor Latch Contact <br> [ ] <br> O:0/1"]
        
        L1 --> NC_Estop
        NC_Estop --> NC_Stop
        NC_Stop --> NO_Start
        NC_Stop --> Latch
        
        NO_Start --> NC_OL
        Latch --> NC_OL
        NC_OL --> Coil
        Coil --> R1
    end

    style Ladder fill:none,stroke:#333,stroke-width:2px
    style Coil fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 3. PLC EX-OR Gate Implementation (Ladder Logic)
* **File Name:** `xor_ladder.png`

```mermaid
flowchart LR
    subgraph XOR_Logic ["EX-OR Logic realization: Y = (A * NC B) + (NC A * B)"]
        L1["Left Rail (L1)"]
        R1["Right Rail (L2)"]
        
        subgraph Branch1 ["Branch 1 (A * NC B)"]
            A_NO["NO Contact A <br> [ ] <br> I:0/1"]
            B_NC["NC Contact B <br> [ ]/[ ] <br> I:0/2"]
        end
        
        subgraph Branch2 ["Branch 2 (NC A * B)"]
            A_NC["NC Contact A <br> [ ]/[ ] <br> I:0/1"]
            B_NO["NO Contact B <br> [ ] <br> I:0/2"]
        end
        
        Coil["Output Coil Y <br> ( ) <br> O:0/1"]
        
        L1 --> A_NO
        L1 --> A_NC
        
        A_NO --> B_NC
        A_NC --> B_NO
        
        B_NC --> Coil
        B_NO --> Coil
        Coil --> R1
    end

    style XOR_Logic fill:none,stroke:#333,stroke-width:2px
    style Coil fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 4. PLC Tank Level Control System (Ladder Logic)
* **File Name:** `tank_level_ladder.png`

```mermaid
flowchart LR
    subgraph LevelControl ["Tank Auto-Filling Logic: Start Pump on Low Level, Stop on High Level"]
        L1["Left Rail (L1)"]
        R1["Right Rail (L2)"]
        
        LowSens["NO Low Sensor (L) <br> [ ] <br> I:0/1 <br> (Closes when tank empty)"]
        HighSens["NC High Sensor (H) <br> [ ]/[ ] <br> I:0/2 <br> (Opens when tank full)"]
        PumpCoil["Pump Motor Output <br> ( ) <br> O:0/1"]
        PumpLatch["NO Pump Latch Contact <br> [ ] <br> O:0/1"]
        
        L1 --> LowSens
        L1 --> PumpLatch
        
        LowSens --> HighSens
        PumpLatch --> HighSens
        HighSens --> PumpCoil
        PumpCoil --> R1
    end

    style LevelControl fill:none,stroke:#333,stroke-width:2px
    style PumpCoil fill:#e6ffe6,stroke:#009900,stroke-width:2px,color:#000
```

---

## 5. PLC NAND & NOR Logic Gate Realizations
* **File Name:** `nand_nor_gates.png`

```mermaid
flowchart TD
    subgraph NAND ["NAND Gate Realization (Parallel NC Contacts)"]
        L1_NAND["Left Rail"]
        R1_NAND["Right Rail"]
        
        A_NC["NC Contact A <br> [ ]/[ ]"]
        B_NC["NC Contact B <br> [ ]/[ ]"]
        Coil_NAND["Output Coil Y <br> ( )"]
        
        L1_NAND --> A_NC
        L1_NAND --> B_NC
        A_NC --> Coil_NAND
        B_NC --> Coil_NAND
        Coil_NAND --> R1_NAND
    end

    subgraph NOR ["NOR Gate Realization (Series NC Contacts)"]
        L1_NOR["Left Rail"]
        R1_NOR["Right Rail"]
        
        A_NC2["NC Contact A <br> [ ]/[ ]"]
        B_NC2["NC Contact B <br> [ ]/[ ]"]
        Coil_NOR["Output Coil Y <br> ( )"]
        
        L1_NOR --> A_NC2
        A_NC2 --> B_NC2
        B_NC2 --> Coil_NOR
        Coil_NOR --> R1_NOR
    end

    style NAND fill:none,stroke:#0066cc,stroke-width:1px
    style NOR fill:none,stroke:#009900,stroke-width:1px
```

---

## 6. Distributed Control System (DCS) Hierarchical Levels
* **File Name:** `dcs_hierarchy.png`

```mermaid
graph TD
    subgraph DCS_Hierarchy ["Distributed Control System (DCS) Levels"]
        L4["Level 4: Enterprise Level <br> (ERP, Business Planning, Long-term Scheduler)"]
        L3["Level 3: Operations & Management Level <br> (MES, Database Server, Production Reports)"]
        L2["Level 2: Supervisory & Console Level <br> (HMI Stations, Operator Desks, Engineering PC)"]
        L1["Level 1: Direct Control Level <br> (Distributed LCUs, PLCs, Controller Units)"]
        L0["Level 0: Field Level <br> (Sensors, Actuators, Smart Instruments, Valves)"]
    end
    
    L4 --> L3
    L3 --> L2
    L2 --> L1
    L1 --> L0
    L0 -->|Raw Data / Feedback| L1
    L1 -->|Status Updates| L2
    L2 -->|Aggregated Logs| L3
    L3 -->|Business Analytics| L4

    style DCS_Hierarchy fill:none,stroke:#333,stroke-width:2px
    style L4 fill:#f2f2f2,stroke:#666,color:#000
    style L3 fill:#ffffe6,stroke:#cccc00,color:#000
    style L2 fill:#e6f2ff,stroke:#0066cc,color:#000
    style L1 fill:#e6ffe6,stroke:#009900,color:#000
    style L0 fill:#ffe6e6,stroke:#cc0000,color:#000
```

---

## 7. DCS Functional Block Architecture
* **File Name:** `dcs_architecture.png`

```mermaid
graph TD
    subgraph DCS_System ["Distributed Control System (DCS) Network Component Nodes"]
        EngStation["Engineering Workstation <br> (System configuration, graphics, I/O mapping)"]
        OperatorStation["Operator Console (HMI) <br> (Alarms, trends, process operation panels)"]
        DataServer["Historical Data Server <br> (DCS Database, production logs)"]
        
        HighSpeedBus["High-Speed Control Network Bus (redundant Ethernet/Coaxial)"]
        
        LCU1["Local Control Unit 1 (LCU)"]
        LCU2["Local Control Unit 2 (LCU)"]
        
        FieldBus1["Fieldbus Network (Profibus/Foundation Fieldbus)"]
        FieldBus2["Fieldbus Network (Profibus/Foundation Fieldbus)"]
    end
    
    EngStation <--> HighSpeedBus
    OperatorStation <--> HighSpeedBus
    DataServer <--> HighSpeedBus
    
    HighSpeedBus <--> LCU1
    HighSpeedBus <--> LCU2
    
    LCU1 <--> FieldBus1
    LCU2 <--> FieldBus2
    
    FieldBus1 <--> FieldDevices1["Field Devices (Sensors & Actuators in Plant Area 1)"]
    FieldBus2 <--> FieldDevices2["Field Devices (Sensors & Actuators in Plant Area 2)"]

    style DCS_System fill:none,stroke:#333,stroke-width:2px
    style HighSpeedBus fill:#ffe6e6,stroke:#cc0000,stroke-width:3px,color:#000
    style LCU1 fill:#e6f2ff,stroke:#0066cc,color:#000
    style LCU2 fill:#e6f2ff,stroke:#0066cc,color:#000
```

---

## 8. SCADA System Topology Block Diagram
* **File Name:** `scada_architecture.png`

```mermaid
graph TD
    subgraph SCADA ["SCADA Supervisory & Data Acquisition Network"]
        subgraph ControlCenter ["Supervisory Station (Control Room)"]
            MTU["Master Terminal Unit (MTU) <br> (Central Host Server)"]
            HMI["Human Machine Interface (HMI) <br> (Operator Console Screens)"]
            Hist["Historian DB Server"]
            
            MTU <--> HMI
            MTU <--> Hist
        end
        
        CommWAN["WAN Communication Network <br> (Radio Modems, Optical Fiber, GSM/GPRS, Satellite)"]
        
        subgraph RTU_Sites ["Remote Field Sites"]
            RTU1["Remote Terminal Unit 1 (RTU)"]
            PLC1["Programmable Logic Controller (PLC)"]
            RTU2["Remote Terminal Unit 2 (RTU)"]
        end
    end
    
    MTU <--> CommWAN
    CommWAN <--> RTU1
    CommWAN <--> PLC1
    CommWAN <--> RTU2
    
    RTU1 <--> Field1["Field Instruments (Pipeline Station A)"]
    PLC1 <--> Field2["Field Instruments (Pump Station B)"]
    RTU2 <--> Field3["Field Instruments (Substation C)"]

    style SCADA fill:none,stroke:#333,stroke-width:2px
    style ControlCenter fill:#e6f2ff,stroke:#0066cc,stroke-width:1px
    style CommWAN fill:#ffe6e6,stroke:#cc0000,stroke-width:2px,color:#000
    style RTU_Sites fill:#e6ffe6,stroke:#009900,stroke-width:1px
```

---

## 9. Control Valve Structural Component Assembly
* **File Name:** `control_valve.png`

```mermaid
graph TD
    subgraph ValveAssembly ["Control Valve Anatomy"]
        Actuator["Pneumatic / Electric Actuator <br> (Generates stem force)"]
        Yoke["Yoke <br> (Structural mount connecting actuator to body)"]
        Bonnet["Bonnet <br> (Houses packing seals to prevent leak)"]
        
        subgraph Body ["Valve Body (Fluid Throttling Zone)"]
            Stem["Valve Stem"]
            Plug["Valve Plug <br> (Throttling element)"]
            Seat["Valve Seat Ring <br> (Mating surface)"]
        end
    end
    
    Actuator -->|Pushes / Pulls| Stem
    Stem --> Bonnet
    Bonnet --> Yoke
    Stem --> Plug
    Plug -->|Seat Contact = Fully Closed| Seat

    style ValveAssembly fill:none,stroke:#333,stroke-width:2px
    style Actuator fill:#e6f2ff,stroke:#0066cc,stroke-width:2px,color:#000
    style Body fill:#e6ffe6,stroke:#009900,stroke-width:1px,color:#000
    style Plug fill:#ffe6e6,stroke:#cc0000,color:#000
```

---

## 10. Electromagnetic Relay Panel vs. PLC Scan Cycle
* **File Name:** `relay_vs_plc.png`

```mermaid
graph TD
    subgraph RelayPanel ["Conventional Relay Logic"]
        Wire["Hardwired Copper Cables"] --> Contacts["Coils & Contacts in Parallel"]
        Contacts --> Instant["Instantaneous electrical propagation <br> (Subject to coil contact wear)"]
    end

    subgraph PLCScan ["PLC Cycle Scanning Method"]
        S1["1. Read Inputs <br> (Copy physical input status to Image Table)"] --> S2["2. Execute Program <br> (Solve ladder logic sequentially from top-to-bottom)"]
        S2 --> S3["3. Diagnostics & Comm <br> (Check system health, handle loader queries)"]
        S3 --> S4["4. Update Outputs <br> (Write Output Image Table status to physical terminals)"]
        S4 --> S1
    end

    style RelayPanel fill:#ffe6e6,stroke:#cc0000,stroke-width:1px
    style PLCScan fill:#e6f2ff,stroke:#0066cc,stroke-width:1px
```
