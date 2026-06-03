# Flashcards: Unit II: Design Principles for Connected Devices

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, structures, and systems of Unit II.

---

### 🎴 Card 1:
Q1. What is the primary goal of the design principles discussed in this unit?  
**Ans.** The primary goal is to guide the creation of "calm and ambient technology" where the technology integrates seamlessly into the user's environment, providing value without being intrusive or demanding constant attention. It emphasizes human-centered design.  

---

### 🎴 Card 2:
Q2. How does the concept of "Calm Technology" differ from traditional "Ugly Technology"?  
**Ans.** Ugly/Intrusive Technology is "noisy"—it uses active screens, requires focus, and constantly demands attention (like a constantly pinging smartphone). Calm Technology is "quiet"—it uses peripheral awareness, ambient information display, and subtle cues, allowing users to stay informed without being overwhelmed.  

---

### 🎴 Card 3:
Q3. What is Ambient Technology? Give three classic examples.  
**Ans.** Physical devices that implement Calm Technology by displaying data through subtle, environmental cues (color, light, motion) rather than pixel-based screens.  
**Examples:**  
1. *Ambient Orb:* A frosted ball that changes color based on stock market indices.  
2. *Ambient Umbrella:* An umbrella handle that pulses blue if rain is forecast.  
3. *Water Lamp:* Projects light ripples on the ceiling representing office network activity.

---

### 🎴 Card 4:
Q4. State the five core design rules of Calm Technology.  
**Ans.**  
1. **Peripheral Attention Priority:** Must work in the user's peripheral sensory field.  
2. **Seamless Shift Control:** Must shift easily between the periphery and the center of focus.  
3. **Enhancing Presence:** Must provide a sense of context and presence.  
4. **Peripheral Reach Extension:** Must extend the user's awareness of remote systems.  
5. **Respecting Attention Limits:** Must work in harmony with human attention bandwidth.

---

### 🎴 Card 5:
Q5. Detail the working principle, advantages, and limitations of David Rose's Ambient Orb.  
**Ans.**  
*   **Working Principle:** A frosted sphere receiving stock or traffic data feeds over the internet, changing its internal LED color accordingly (e.g., green for up, red for down).  
*   **Advantage:** Allows instant, non-intrusive, glanceable monitoring in the background of a room.  
*   **Limitation:** Low information density; cannot show exact numeric values.

---

### 🎴 Card 6:
Q6. Explain the concept of "Magic as Metaphor" in IoT design. Give two examples.  
**Ans.** Using magical archetypes (magic wand, crystal ball, enchanted mirror) from myths as design metaphors to explain how invisible, wireless IoT systems operate.  
*   **Examples:**  
    1. *Kymera Magic Wand:* A physical wand that uses gestures to change TV channels.  
    2. *Smart Mirror:* A bathroom mirror that displays digital text on its glass surface, acting like an enchanted mirror.

---

### 🎴 Card 7:
Q7. What are the three primary critiques or limitations of using "Magic as Metaphor"?  
**Ans.**  
1. **Expectation Mismatch:** Users expect infinite magical capabilities, leading to disappointment.  
2. **No Clear Error States (Lack of Debuggability):** Magic does not have error codes. If a gesture fails, the user cannot easily debug if the network is down or the battery is dead.  
3. **Cultural Variance:** Magical myths vary globally, making some metaphors less intuitive in certain markets.

---

### 🎴 Card 8:
Q8. List five distinct advantages of Calm and Ambient Technology.  
**Ans.**  
1. Reduces cognitive fatigue and stress.  
2. Blends naturally into the decor, avoiding screen clutter.  
3. Preserves human-to-human face-to-face interaction.  
4. Fosters ambient awareness of external systems.  
5. High energy efficiency compared to active LCD screens.

---

### 🎴 Card 9:
Q9. List five distinct disadvantages of Calm and Ambient Technology.  
**Ans.**  
1. Low information density (conveys status, not detailed text).  
2. High ambiguity (abstract cues can be misread).  
3. Inappropriate for high-priority critical alerts (e.g., fire alarms).  
4. Difficult to troubleshoot and debug due to lack of screens.  
5. Accessibility issues (color blindness or hearing loss can block cues).

---

### 🎴 Card 10:
Q10. How does "Privacy" in IoT device design extend beyond standard data encryption?  
**Ans.** It focuses on the physical space boundaries:  
1. **Consent & Control:** Offering physical switches to disable sensor recording.  
2. **Contextual Integrity:** Ensuring household data (e.g. thermostat activity) is not sold or repurposed.  
3. **Data Minimization:** Keeping raw data collection to the minimum required.  
4. **Local Processing:** Analyzing voice/images locally at the edge/gateway rather than streaming to the cloud.  
5. **Transparency:** Using hardwired LEDs to show when microphones or cameras are actively powered.

---

### 🎴 Card 11:
Q11. Explain "Web Thinking for Connected Devices" and name three key principles.  
**Ans.** Designing physical IoT architectures using the open, scalable, and standardized principles of the World Wide Web.  
*   **Key Principles:**  
    1. *URIs/URLs for Things:* Every sensor/actuator has a unique address.  
    2. *RESTful APIs:* Devices expose standard HTTP commands (GET/POST/PUT/DELETE) using JSON.  
    3. *Loose Coupling:* Hardware is independent of the applications controlling it.

---

### 🎴 Card 12:
Q12. What is a "Physical Mashup" in the context of Web Thinking? Give an example.  
**Ans.** Linking different physical devices together using standard web APIs and middleware (like IFTTT or Node-RED).  
*   **Example:** "If a smart security camera detects motion, Then send an HTTP command to blink a smart light bulb."

---

### 🎴 Card 13:
Q13. Define "Affordance" and explain the "Clash of Affordances" in IoT.  
**Ans.**  
*   **Affordance:** The physical properties of an object that suggest how to use it (e.g., button invites pushing).  
*   **Clash of Affordances:** A smart object looks like its traditional physical counterpart (e.g., a smart cup), but has hidden digital affordances (Bluetooth pairing, sensors) that are completely invisible.

---

### 🎴 Card 14:
Q14. What are three design solutions to resolve the Clash of Affordances?  
**Ans.**  
1. **Visual Signifiers:** Use subtle indicators like LED rings or textured borders to guide touch.  
2. **Sensory Feedback:** Provide immediate haptic vibes or chirps when a sensor is triggered.  
3. **Graceful Degradation:** Ensure the device still functions as its physical counterpart if the battery dies or Wi-Fi is lost (e.g. a smart lock still opens with a physical key).