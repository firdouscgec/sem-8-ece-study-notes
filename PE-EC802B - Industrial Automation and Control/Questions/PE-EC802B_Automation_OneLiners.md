# PE-EC802B: Industrial Automation and Control - One-Liners

---

# Chapter 1: Sensors & Actuators

1. Active Transducer definition → Generates electrical output directly without external power source.
2. Passive Transducer definition → Requires external electrical source to measure parameter variations.
3. Active transducer examples → Thermocouple, piezoelectric sensor, solar cell.
4. Passive transducer examples → LVDT, RTD, thermistor, strain gauge.
5. LVDT full form → Linear Variable Differential Transformer.
6. LVDT working principle → Mutual inductance.
7. LVDT null voltage cause → Stray capacitances, harmonics, and magnetic leakage.
8. LVDT phase shift across null position → $180^\circ$ phase shift.
9. Thermocouple working principle → Seebeck effect.
10. Seebeck effect definition → Temperature differences at joined dissimilar metals generate voltage.
11. Type K thermocouple materials → Chromel (positive) and Alumel (negative).
12. Type J thermocouple materials → Iron (positive) and Constantan (negative).
13. Thermocouple Cold Junction Compensation necessity → Corrects for fluctuations in reference junction temperature.
14. Ultrasonic sensor distance formula → $d = \frac{v \times t}{2}$.
15. Piezoelectric actuator working principle → Piezoelectric effect.
16. Pneumatic actuator working fluid → Compressed air.
17. Electronic to pneumatic converter (I/P) input/output standards → Converts 4–20 mA current to 3–15 psi pressure.
18. Pneumatic to current converter (P/I) input/output standards → Converts 3–15 psi pressure to 4–20 mA current.
19. Components needed for a 4–20 mA loop → Power supply, transmitter, and wire.
20. Standard SI unit of torque → Newton meter ($\text{N}\cdot\text{m}$).
21. Displacement sensor measuring via plate separation or dielectric → Capacitance sensor.
22. Potentiometer primary measurement target → Linear displacement.
23. Control valve sizing design goals → Avoids undersizing, oversizing, and excess cost.
24. Smart sensor output style → Digital.
25. Radio Frequency Interference acronym → RFI.
26. Actuator type preferred for slow 10s time constant processes → Piston and cylinder.

# Chapter 2: Controller Tuning

1. Proportional (P) controller equation → $p(t) = K_c e(t) + p_s$.
2. P-controller main disadvantage → Steady-state error (offset) persists after load changes.
3. Controller with maximum steady-state offset → P-controller.
4. Integral (I) controller equation → $p(t) = \frac{1}{\tau_I} \int_0^t e(t^*) dt^* + p(0)$.
5. I-controller main advantage → Completely eliminates steady-state offset.
6. I-controller main disadvantages → Introduces phase lag and susceptible to integral windup.
7. Derivative (D) controller equation → $p(t) = \tau_D \frac{de(t)}{dt}$.
8. Reason D-control cannot be used alone → Output is zero under constant error.
9. Relationship between Proportional Band (PB) and Gain ($K_c$) → $K_c = \frac{100}{PB}$.
10. Proportional Band expression units → Percentage.
11. Offset definition in control theory → Steady-state error between setpoint and process variable.
12. Op-amp PI controller feedback path components → Resistor in series with capacitor.
13. Op-amp PD controller feedback path components → Resistor in parallel with capacitor.
14. Parallel electronic PID design minimum op-amp count → 2 operational amplifiers.
15. Ziegler-Nichols (Z-N) tuning definition → Experimental method determining gain factors via critical oscillation.
16. Ziegler-Nichols parameter determination technique → Graphical solution method.
17. In direct-acting controller (CA4 definition), output increases when process measurement → Decreases.
18. In reverse-acting controller, output increases when process measurement → Decreases.
19. Action to reduce overshoots in a PID controller → Increase the derivative time constant.
20. PID controller selection criteria → Offset elimination, small system changes, fast recovery.

# Chapter 3: Automation Systems

1. PLC full form → Programmable Logic Controller.
2. PLC advantages over electromagnetic relays → High flexibility, online diagnostics, small space footprint.
3. Four core PLC hardware modules → CPU, Memory, Power Supply, I/O modules.
4. Steps in a PLC scan cycle → Read inputs, execute program, diagnostics/communication, write outputs.
5. PLC scan time definition → Time taken to execute the entire program.
6. IEC 61131-3 graphical relay-like language → Ladder Diagram (LD).
7. IEC 61131-3 text-based high-level language → Structured Text (ST).
8. IEC 61131-3 assembly-like language → Instruction List (IL).
9. PLC noise immunity to electrical noises → Excellent.
10. SCADA full form → Supervisory Control and Data Acquisition.
11. Four core functions of SCADA → Data acquisition, supervisory control, HMI display, alarm archiving.
12. MTU full form in SCADA → Master Terminal Unit.
13. RTU full form in SCADA → Remote Terminal Unit.
14. HMI full form in SCADA → Human Machine Interface.
15. DCS full form → Distributed Control Systems.
16. PLC vs. DCS control scope → PLC handles local discrete logic; DCS manages plant-wide continuous processes.
17. PLC Instruction turning output ON/OFF after preset time → Timer On Delay (TON).
18. Instruction maintaining timer count on loss of rung power → Retentive Timer (RTO).
19. Non-PLC manufacturer in typical list → Microsoft.
20. Open-loop control system simple everyday example → Automatic toaster.

# Chapter 4: Advanced Control Techniques

1. Feedforward control action style → Proactive/anticipatory control based on measured disturbances.
2. Feedforward control main advantage → Rejects disturbances before process variable deviates.
3. Feedforward control main disadvantage → Only handles measured disturbances, requires precise model.
4. Cascade control loop configuration → Two nested feedback loops (primary outer, secondary inner).
5. Cascade primary controller role → Measures primary variable and outputs secondary controller setpoint.
6. Cascade secondary controller role → Measures intermediate variable and drives control valve.
7. Cascade control primary benefit → Rejects secondary-path disturbances before they affect primary output.
8. Ratio control goal → Maintain flow rate of one stream in fixed proportion to another.
9. Wild flow definition in ratio control → Uncontrolled stream whose flow rate fluctuates freely.
10. Controlled flow calculation formula → $F_{controlled} = R \times F_{wild}$.
11. Override (selective) control purpose → Protective control protecting equipment using High/Low selectors.
12. Split-Range control definition → Single controller output split to operate multiple valves.
13. Split-range jacketed reactor example ranges → 0–50% opens cooling; 50–100% opens heating.
14. Adaptive control definition → System adjusting controller parameters in real-time for changing dynamics.
15. STR full form in adaptive control → Self-Tuning Regulator.
16. MRAC full form in adaptive control → Model Reference Adaptive Control.
17. STR vs. MRAC model parameters estimation → STR estimates process parameters online; MRAC adjusts gains directly.
18. IMC full form → Internal Model Control.
19. IMC core operating concept → Embeds process model in parallel with physical process.
20. Ideal IMC controller design → Mathematical inverse of process model.
