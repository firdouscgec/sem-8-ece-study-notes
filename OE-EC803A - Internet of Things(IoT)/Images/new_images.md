# Proposed Supplementary Diagrams for IoT Syllabus

This document outlines new, helpful diagrams to supplement the notes for the **OE-EC803A - Internet of Things (IoT)** syllabus, complete with their target chapters and copy-ready Mermaid source codes.

---

## 1. IoT Sensor Node Hardware Architecture
* **File Name:** `iot_sensor_node_blocks.png`
* **Chapter Name:** `chapter_06` (Prototyping Embedded Devices)
* **Mermaid Code:**

```mermaid
flowchart TB
    subgraph Node ["Typical IoT Sensor Node Block Diagram"]
        direction TB
        
        %% Power Supply Group
        subgraph Power ["Power Management Unit (PMU)"]
            Bat["Lithium Polymer Battery / USB"]
            Reg["LDO Regulator / Buck Converter (3.3V / 5V)"]
            Bat --> Reg
        end

        %% Central Controller Group
        subgraph MCU ["Microcontroller Unit (MCU / SoC)"]
            CPU["CPU Core (e.g., ARM Cortex-M / AVR)"]
            SRAM["SRAM (Volatile Data)"]
            Flash["Flash Memory (Code/Non-Volatile)"]
            ADC["ADC (Analog-to-Digital Converter)"]
            
            CPU <--> SRAM
            CPU <--> Flash
            CPU <--> ADC
        end

        %% Peripherals
        subgraph Sensors ["Sensors (Inputs)"]
            Temp["Temp & Humidity (I2C)"]
            Light["LDR / Ambient Light (Analog)"]
        end

        subgraph Actuators ["Actuators (Outputs)"]
            Relay["5V Relay Module (GPIO)"]
            LED["Status Indicators (PWM)"]
        end

        %% Communication Transceiver
        subgraph Transceiver ["RF Transceiver (Communication)"]
            RFChip["RF Chip (Wi-Fi / BLE / LoRa)"]
            Match["50 Ohm Pi-Matching Circuit"]
            Ant["Antenna (Chip/Trace/Whip)"]
            
            RFChip --> Match
            Match --> Ant
        end

        %% Interconnections
        Reg -.->|VCC / Power Planes| MCU
        Reg -.->|Power| Sensors
        Reg -.->|Power| Transceiver
        
        Temp <-->|I2C: SDA/SCL| CPU
        Light -->|Analog Voltage| ADC
        CPU -->|GPIO Control| Relay
        CPU -->|PWM| LED
        
        CPU <-->|SPI: MOSI/MISO/SCK/CS| RFChip
    end

    style Node fill:#f9f9f9,stroke:#333,stroke-width:1px
    style MCU fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Power fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Sensors fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Actuators fill:#f8cecc,stroke:#b85450,stroke-width:2px,color:#000
    style Transceiver fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```

---

## 2. IPv4 vs. IPv6 Header Format Comparison
* **File Name:** `ipv4_vs_ipv6_headers.png`
* **Chapter Name:** `chapter_03` (Internet Principles)
* **Mermaid Code:**

```mermaid
flowchart TD
    subgraph IPV4 ["IPv4 Header Format (20-Byte Base Header - Variable Fields)"]
        direction TB
        V4["Version (4b) | IHL (4b) | ToS (8b) | Total Length (16b)"]
        ID["Identification (16b) | Flags (3b) | Fragment Offset (13b)"]
        TTL["TTL (8b) | Protocol (8b) | Header Checksum (16b)"]
        S4["Source IP Address (32 bits)"]
        D4["Destination IP Address (32 bits)"]
        O4["Options & Padding (Variable, 0-40 bytes)"]
        
        V4 --> ID --> TTL --> S4 --> D4 --> O4
    end

    subgraph IPV6 ["IPv6 Header Format (40-Byte Fixed Base Header - Streamlined Fields)"]
        direction TB
        V6["Version (4b) | Traffic Class (8b) | Flow Label (20b)"]
        PL["Payload Length (16b) | Next Header (8b) | Hop Limit (8b)"]
        S6["Source IPv6 Address (128 bits)"]
        D6["Destination IPv6 Address (128 bits)"]
        Ext["Extension Headers (Optional, daisy-chained via Next Header)"]
        
        V6 --> PL --> S6 --> D6 --> Ext
    end

    style IPV4 fill:#fff2cc,stroke:#d6b656,stroke-width:2px,color:#000
    style IPV6 fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```
