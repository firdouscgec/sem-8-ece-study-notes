# Diagrams Registry: PE-EC801B - Chapter 03

This registry contains copy-ready Mermaid source codes for diagrams related to Chapter 3 (Signal Degradation on Optical Fibers).

---

## 1. OTDR Block Diagram
This block diagram represents the internal components of an Optical Time Domain Reflectometer (OTDR).

* **File Name:** `otdr_block.png`
* **Mermaid Code:**

```mermaid
graph LR
    subgraph OTDR Instrument
        PulseGen["Pulse Generator"] --> Laser["Pulsed Laser Source"]
        Laser --> Circulator["Directional Coupler / Circulator"]
        Circulator --> Detector["Photodetector & APD Receiver"]
        Detector --> SignalProc["Signal Processor & Averager"]
        PulseGen -. Synchronization .-> SignalProc
        SignalProc --> Display["Display / CRT Screen"]
    end
    Circulator <==> LaunchFiber["Launch Fiber / Patch Cord"]
    LaunchFiber <==> TestFiber["Fiber Under Test"]
```

---

## 2. OTDR Trace Waveform
This diagram represents a typical OTDR trace, highlighting the various reflective and non-reflective events along the fiber length.

* **File Name:** `otdr_trace.png`
* **Mermaid Code:**

```mermaid
xychart-beta
    title "Typical OTDR Trace (Power vs Distance)"
    x-axis [0, 1, 2, 3, 4, 5, 6, 7]
    y-axis "Relative Backscattered Power (dB)" 0 --> 40
    line [35, 30, 20, 18, 15, 10, 25, 0]
```
*(Note: For LaTeX rendering, a high-quality vector plot using TikZ or pgfplots will be generated representing:)*
1.  **Start:** Front panel connector Fresnel reflection peak.
2.  **Linear Slope:** Rayleigh backscattering loss.
3.  **Step Down (No peak):** Non-reflective loss event (e.g., fusion splice).
4.  **Sharp Peak + Step Down:** Reflective loss event (e.g., mechanical splice or connector).
5.  **Final Peak + Drop to Noise Floor:** Cleaved fiber end face Fresnel reflection.

---

## 3. Fiber Attenuation vs. Wavelength Curve
This curve details the attenuation bands of silica glass as a function of wavelength, highlighting the three transmission windows and the water absorption peaks.

* **File Name:** `attenuation_curve.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph Attenuation Curve Features
        Peak1["OH- Absorption Peak (950 nm)"]
        Peak2["OH- Absorption Peak (1240 nm)"]
        Peak3["OH- Absorption Peak (1380 nm) (Water Peak)"]
        Rayleigh["Rayleigh Scattering Limit (Decreases as 1/\lambda^4)"]
        IR["Infrared Absorption Tail (Increases at \lambda > 1.6 \mu m)"]
    end
```
*(Note: The LaTeX compilation will represent this as a continuous curve with three highlighted windows:)*
*   **Window I ($850\text{ nm}$):** Attenuation $\approx 2.5\ \text{dB/km}$.
*   **Window II ($1310\text{ nm}$):** Attenuation $\approx 0.4\ \text{dB/km}$, zero chromatic dispersion.
*   **Window III ($1550\text{ nm}$):** Attenuation $\approx 0.2\ \text{dB/km}$, absolute minimum attenuation.

---

## 4. Pulse Broadening and dispersion
This flowchart depicts how light pulses broaden and overlap (Inter-Symbol Interference) as they propagate down a dispersive fiber.

* **File Name:** `pulse_broadening.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph Input ["Input Pulses (Distinct)"]
        P1["Pulse 1: [ | ]"] --- P2["Pulse 2: [ | ]"]
    end
    subgraph Output ["Output Pulses (Overlapped - ISI)"]
        P3["Pulse 1: [ \\_/ ]"] --- P4["Pulse 2: [ \\_/ ]"]
    end
    Input ===>|Propagation along fiber| Output
```

---

## 5. Dispersion Curves
This flowchart represents the dispersion characteristics of standard single-mode fibers vs. dispersion-shifted/flattened fibers.

* **File Name:** `dispersion_curves.png`
* **Mermaid Code:**

```mermaid
graph TD
    SMF["Standard SMF"] --> SMF_Zero["Zero Dispersion @ 1310 nm"]
    SMF --> SMF_Loss["High Dispersion (~17 ps/nm-km) @ 1550 nm (minimum loss)"]
    
    DSF["Dispersion-Shifted Fiber (DSF)"] --> DSF_Zero["Zero Dispersion shifted to 1550 nm (minimum loss & zero dispersion)"]
    
    DFF["Dispersion-Flattened Fiber (DFF)"] --> DFF_Flat["Very low dispersion (< 2 ps/nm-km) from 1300 nm to 1600 nm"]
```

---

## 6. Cut-Back Method Setup
This diagram illustrates the two-step measurement setup of the Cut-Back method for attenuation measurement.

* **File Name:** `cut_back_method.png`
* **Mermaid Code:**

```mermaid
graph TD
    subgraph "Step 1: Measure Long Fiber"
        Source1["Light Source"] ===> Launcher1["Optical Launcher"] ===> LongFiber["Test Fiber (Length L)"] ===> Detector1["Power Detector (Measures P2)"]
    end
    subgraph "Step 2: Cut Back Fiber (Launch conditions undisturbed)"
        Source2["Light Source"] ===> Launcher2["Optical Launcher"] ===> ShortFiber["Short Fiber (Length z ~ 2 m)"] ===> Detector2["Power Detector (Measures P1)"]
    end
```
