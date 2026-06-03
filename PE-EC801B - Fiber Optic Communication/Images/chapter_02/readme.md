# Diagrams Registry: PE-EC801B - Chapter 02

This document contains copy-ready Mermaid source codes for the diagrams referenced in the Chapter 2 notes. These codes can be rendered to PNGs using the local Mermaid editor.

---

## 1. Refractive Index Profiles (Step-Index vs. Graded-Index)
* **File Name:** `index_profiles.png`
* **Mermaid Code:**

```mermaid
flowchart TD
    subgraph ProfileSI ["Step-Index (SI) Profile"]
        direction TB
        SI_Line["Flat Core (n1) | Abrupt Drop | Flat Clad (n2)"]
    end

    subgraph ProfileGI ["Graded-Index (GI) Profile"]
        direction TB
        GI_Line["Parabolic Core Curve (n(r)) | Smooth Drop | Flat Clad (n2)"]
    end

    style ProfileSI fill:#fff2cc,stroke:#d6b656,stroke-width:2px,color:#000
    style ProfileGI fill:#e1d5e7,stroke:#9673a6,stroke-width:2px,color:#000
```

---

## 2. Cylindrical Coordinate Boundaries
* **File Name:** `cylindrical_coords.png`
* **Mermaid Code:**

```mermaid
graph TD
    Axis["Z-Axis (Direction of Propagation)"]
    Radius["Radius r (r = a at core interface)"]
    Angle["Azimuthal Angle phi"]
    
    Axis <-->|Cylindrical Waveguide Coordinates| Radius
    Radius <--> Angle
    
    style Axis fill:#ffe6cc,stroke:#d79b00,stroke-width:2px,color:#000
    style Radius fill:#e2f0d9,stroke:#385723,stroke-width:2px,color:#000
    style Angle fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px,color:#000
```
