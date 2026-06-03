# Chapter 6 Diagrams

---

## 1. Arduino vs. Raspberry Pi Architecture Comparison
* **File Name:** `arduino_vs_raspberry_pi.png`

```mermaid
flowchart LR
    subgraph Arduino ["Arduino (Microcontroller Platform)"]
        direction TB
        A1["Processor: ATmega328P (8-bit AVR)<br>Clock: 16 MHz"]
        A2["Memory: 2 KB SRAM, 32 KB Flash"]
        A3["OS: None (Bare-metal firmware)"]
        A4["I/O: 14 Digital + 6 Analog GPIO"]
        A5["Power: 5V USB / Battery<br>Ultra-low consumption"]
        
        A1 --> A2 --> A3 --> A4 --> A5
    end
    
    subgraph RPi ["Raspberry Pi (Microprocessor Platform)"]
        direction TB
        R1["Processor: BCM2711 (64-bit ARM Cortex-A72)<br>Clock: 1.5 GHz"]
        R2["Memory: 1-8 GB LPDDR4 RAM"]
        R3["OS: Linux (Raspberry Pi OS, Ubuntu)"]
        R4["I/O: 40-pin GPIO Header (I2C, SPI, UART)"]
        R5["Power: 5V USB-C (3A)<br>Higher consumption"]
        
        R1 --> R2 --> R3 --> R4 --> R5
    end

    style Arduino fill:none,stroke:#82b366,stroke-width:2px
    style RPi fill:none,stroke:#6c8ebf,stroke-width:2px
    style A1 fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style A2 fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style A3 fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style A4 fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style A5 fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style R1 fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style R2 fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style R3 fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style R4 fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style R5 fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
```

---

## 2. Raspberry Pi GPIO Pin Interfaces Mapping
* **File Name:** `rpi_gpio_interfaces.png`

```mermaid
flowchart TD
    Header["Raspberry Pi 40-Pin GPIO Header"]
    
    Header --> Power["Power Pins<br>3.3V (Pin 1, 17) and 5V (Pin 2, 4)"]
    Header --> GND["Ground Pins<br>Pin 6, 9, 14, 20, 25, 30, 34, 39"]
    Header --> DigGPIO["General Purpose I/O<br>28 configurable digital pins<br>Input / Output / PWM"]
    Header --> I2C["I2C Bus<br>SDA (GPIO 2) + SCL (GPIO 3)<br>Multi-device shared bus"]
    Header --> SPI["SPI Bus<br>MOSI, MISO, SCLK, CE0, CE1<br>High-speed peripheral link"]
    Header --> UART["UART Serial<br>TX (GPIO 14) + RX (GPIO 15)<br>Point-to-point serial debug"]
    
    style Header fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style Power fill:#f8cecc,stroke:#b85450,stroke-width:1px,color:#000
    style GND fill:#e1d5e7,stroke:#9673a6,stroke-width:1px,color:#000
    style DigGPIO fill:#e2f0d9,stroke:#385723,stroke-width:1px,color:#000
    style I2C fill:#ffe6cc,stroke:#d79b00,stroke-width:1px,color:#000
    style SPI fill:#dae8fc,stroke:#6c8ebf,stroke-width:1px,color:#000
    style UART fill:#fff2cc,stroke:#d6b656,stroke-width:1px,color:#000
```
