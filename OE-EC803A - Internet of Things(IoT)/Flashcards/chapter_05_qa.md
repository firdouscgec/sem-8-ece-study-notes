# Flashcards: Unit V: Prototyping the Physical Design

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit V.

---

### 🎴 Card 1:
Q1. Explain the working principle of 3D Printing (FDM) in IoT prototyping.  
**Ans.** Fused Deposition Modeling (FDM) melts thermoplastic filament and extrudes it through a nozzle, depositing it layer-by-layer on a build plate based on a sliced 3D CAD model to form a solid enclosure.

---

### 🎴 Card 2:
Q2. What are the main limitations of 3D Printing for physical prototyping?  
**Ans.** Slow build speed (takes hours), anisotropic structural weakness (parts easily snap along layer lines), and rough surface finishes showing layer lines.

---

### 🎴 Card 3:
Q3. What is the primary dimensional constraint of Laser Cutting and how do designers bypass it?  
**Ans.** It is restricted to 2D flat profiles. Designers bypass this by cutting flat sheets with integrated tabs or finger joints, which are then assembled/slotted together to form 3D boxes.

---

### 🎴 Card 4:
Q4. Why must PVC (Polyvinyl Chloride) never be laser cut?  
**Ans.** Laser cutting PVC releases toxic and highly corrosive chlorine gas, which presents extreme safety hazards to operators and corrodes the metal components of the laser machine.

---

### 🎴 Card 5:
Q5. Detail the working principle, main advantage, and main disadvantage of CNC Milling.  
**Ans.** CNC milling is a subtractive process that carves shapes out of a solid block using high-speed rotating cutting tools.  
* *Advantage:* High mechanical strength and precise tolerances.  
* *Disadvantage:* High material waste and complex setup (generating G-code).

---

### 🎴 Card 6:
Q6. What are the advantages and limitations of repurposing off-the-shelf enclosures?  
**Ans.**  
* *Advantages:* Pre-fabricated water resistance (IP-rated project boxes), low cost, and instant availability.  
* *Limitations:* Restricted to pre-existing dimensions and hard to scale or replicate identically.

---

### 🎴 Card 7:
Q7. What is the function of an antenna in an IoT device?  
**Ans.** It acts as a transducer, converting electrical signals from the RF transceiver chip into electromagnetic radio waves for transmission, and capturing incoming waves to convert them back to electrical signals.

---

### 🎴 Card 8:
Q8. Compare PCB Trace and External Whip antennas in terms of unit cost and range.  
**Ans.**  
* **PCB Trace:** Zero unit cost (fabricated as copper traces on the board), moderate range.  
* **External Whip:** High unit cost (requires coax cables and SMA connectors), maximum range and high gain.

---

### 🎴 Card 9:
Q9. How does a metallic enclosure affect an internal antenna, and how is it resolved?  
**Ans.** A metal enclosure acts as a Faraday cage, blocking electromagnetic RF signals. This is resolved by mounting an external antenna outside the enclosure connected to the PCB via an SMA feedthrough.

---

### 🎴 Card 10:
Q10. What is Ground Plane Clearance and why is it necessary for chip antennas?  
**Ans.** It is a design requirement stating that no copper ground planes, traces, or vias should run on any layer of the PCB directly underneath or adjacent to the antenna. This is necessary to prevent detuning the antenna and blocking the RF signal.
