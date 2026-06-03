# Chapter 3 Diagrams

---

## 1. TCP/IP Protocol Suite vs OSI Model Mapping
* **File Name:** `tcp_ip_vs_osi.png`

```mermaid
flowchart LR
    subgraph OSI ["OSI Reference Model"]
        direction TB
        OSI7["7. Application Layer"]
        OSI6["6. Presentation Layer"]
        OSI5["5. Session Layer"]
        OSI4["4. Transport Layer"]
        OSI3["3. Network Layer"]
        OSI2["2. Data Link Layer"]
        OSI1["1. Physical Layer"]
    end

    subgraph TCPIP ["TCP/IP Suite"]
        direction TB
        T4["4. Application Layer"]
        T3["3. Transport Layer"]
        T2["2. Internet Layer"]
        T1["1. Network Access Layer"]
    end

    OSI7 -.-> T4
    OSI6 -.-> T4
    OSI5 -.-> T4
    OSI4 -.-> T3
    OSI3 -.-> T2
    OSI2 -.-> T1
    OSI1 -.-> T1

    style OSI fill:none,stroke:#333,stroke-width:1px
    style TCPIP fill:none,stroke:#333,stroke-width:1px
    style T4 fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style T3 fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style T2 fill:#d5e8d4,stroke:#82b366,stroke-width:2px,color:#000
    style T1 fill:#e1d5e7,stroke:#b85450,stroke-width:2px,color:#000
```

---

## 2. DHCP Client-Server DORA Handshake
* **File Name:** `dhcp_handshake.png`

```mermaid
sequenceDiagram
    autonumber
    actor Client as IoT Client
    participant Server as DHCP Server
    
    Note over Client,Server: DORA Handshake Process
    Client->>Server: DHCPDISCOVER (Broadcast)
    Note right of Client: "IP address request. Who is out there?"
    
    Server->>Client: DHCPOFFER (Unicast/Broadcast)
    Note left of Server: "Here is an IP address proposal: 192.168.1.50"
    
    Client->>Server: DHCPREQUEST (Broadcast)
    Note right of Client: "Yes, I would like to lease 192.168.1.50!"
    
    Server->>Client: DHCPACK (Unicast/Broadcast)
    Note left of Server: "Lease confirmed. IP: 192.168.1.50, Subnet: 255.255.255.0, DNS: 8.8.8.8"
```

---

## 3. DNS Resolution Process
* **File Name:** `dns_resolution.png`

```mermaid
sequenceDiagram
    autonumber
    actor Client as IoT Device / Client
    participant Resolver as DNS Resolver (ISP/Router)
    participant Root as Root Nameserver (.)
    participant TLD as TLD Nameserver (.com)
    participant Auth as Authoritative Nameserver (example.com)
    
    Client->>Resolver: 1. Query: example.com
    Resolver->>Root: 2. Ask for example.com
    Root-->>Resolver: 3. Referral: Go to .com TLD Nameserver
    Resolver->>TLD: 4. Ask for example.com
    TLD-->>Resolver: 5. Referral: Go to example.com Authoritative Nameserver
    Resolver->>Auth: 6. Ask for example.com
    Auth-->>Resolver: 7. Answer: example.com is at 93.184.216.34
    Resolver->>Client: 8. Resolved IP: 93.184.216.34
```

---

## 4. TCP 3-Way Handshake vs UDP Transmission
* **File Name:** `tcp_vs_udp.png`

```mermaid
sequenceDiagram
    autonumber
    actor Client as IoT Client
    participant Server as IoT Server / Gateway
    
    rect rgb(240, 248, 255)
        Note over Client,Server: TCP Connection: Reliable 3-Way Handshake
        Client->>Server: SYN (Synchronize Sequence Number)
        Server->>Client: SYN-ACK (Acknowledge + Synchronize)
        Client->>Server: ACK (Acknowledge Connection)
        Note over Client,Server: Connection Established. Safe data transfer starts.
    end
    
    rect rgb(255, 240, 245)
        Note over Client,Server: UDP Connection: Connectionless & Unreliable
        Client->>Server: Data Packet (No handshake, no acknowledgement)
        Note right of Client: Sent directly, lower latency
    end
```

---

## 5. MAC Address Structure
* **File Name:** `mac_address_format.png`

```mermaid
flowchart TD
    MAC["MAC Address: 48-bit (6 Octets) <br> e.g., 00:1A:2B:3C:4D:5E"]
    
    MAC --> OUI["Organizationally Unique Identifier (OUI)<br>First 3 Octets (24 bits)<br>Assigned by IEEE to Manufacturer<br>e.g., 00:1A:2B"]
    MAC --> NIC["Network Interface Controller (NIC) Specific<br>Last 3 Octets (24 bits)<br>Assigned by Manufacturer to Device<br>e.g., 3C:4D:5E"]
    
    OUI --> Bit7["Bit 7: U/L Bit (Universal/Local)<br>0 = Globally Unique<br>1 = Locally Administered"]
    OUI --> Bit8["Bit 8: I/G Bit (Individual/Group)<br>0 = Unicast Address<br>1 = Multicast Address"]
    
    style MAC fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000
    style OUI fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style NIC fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
    style Bit7 fill:#d5e8d4,stroke:#82b366,stroke-width:1px,color:#000
    style Bit8 fill:#e1d5e7,stroke:#b85450,stroke-width:1px,color:#000
```

---

## 6. MQTT Pub/Sub vs CoAP Request/Response Architecture
* **File Name:** `mqtt_vs_coap.png`

```mermaid
flowchart TD
    subgraph MQTT ["MQTT Architecture (Publish/Subscribe - Event-Driven)"]
        direction TB
        Pub["Publisher (IoT Sensor Node)"]
        Sub1["Subscriber A (Dashboard)"]
        Sub2["Subscriber B (Database)"]
        Broker["MQTT Broker (Central Message Server)"]
        
        Pub -->|Publish: 'home/temp' = 24C| Broker
        Broker -->|Route to Subscribed Topic| Sub1
        Broker -->|Route to Subscribed Topic| Sub2
    end
    
    subgraph COAP ["CoAP Architecture (Request/Response - Client/Server)"]
        direction TB
        Client["CoAP Client (Mobile App/Gateway)"]
        CoAPServer["CoAP Server (IoT Actuator Node)"]
        
        Client -->|"GET /sensor/temp (Confirmable/Non-confirmable)"| CoAPServer
        CoAPServer -->|"2.05 Content (Response)"| Client
    end

    style MQTT fill:none,stroke:#666,stroke-width:1px
    style COAP fill:none,stroke:#666,stroke-width:1px
    style Broker fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style CoAPServer fill:#d5e8d4,stroke:#82b366,stroke-width:2px,color:#000
```
