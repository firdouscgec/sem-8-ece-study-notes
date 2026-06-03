# Flashcards: Unit II - Intelligent Agents

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, environment properties, and architectures of Unit II.

---

### 🎴 Card 1: Definition of Agent Function
*   **Question:** What is the mathematical definition of an Agent Function?
*   **Answer:** A function $f: P^* \rightarrow A$ that maps any given percept sequence $P^*$ (the history of all percepts received to date) to a specific action $A$.

---

### 🎴 Card 2: PEAS framework
*   **Question:** What does PEAS stand for in agent design?
*   **Answer:**
    *   **P:** Performance Measure (success metric)
    *   **E:** Environment (external context)
    *   **A:** Actuators (output devices/manipulators)
    *   **S:** Sensors (input devices/perceivers)

---

### 🎴 Card 3: Automated Taxi PEAS
*   **Question:** What is the PEAS description for an Automated Taxi Driver?
*   **Answer:**
    *   **P:** Safe, fast, legal, comfortable trip, maximized profits.
    *   **E:** Roads, traffic, pedestrians, weather, passengers.
    *   **A:** Steering wheel, accelerator, brakes, horn, displays.
    *   **S:** Cameras, LIDAR, sonar, GPS, speedometer, odometer.

---

### 🎴 Card 4: Simple Reflex Agent
*   **Question:** What is the core working principle and main limitation of a Simple Reflex Agent?
*   **Answer:**
    *   **Principle:** Selects actions based only on the current percept using condition-action rules.
    *   **Limitation:** It is entirely blind to past percepts and fails if the environment is partially observable.

---

### 🎴 Card 5: Model-Based Reflex Agent
*   **Question:** How does a Model-Based Reflex Agent handle partial observability?
*   **Answer:** It maintains an internal **state** (model of the world) which updates based on how the world evolves independently and how the agent's actions affect the world.

---

### 🎴 Card 6: Goal-Based vs. Utility-Based Agents
*   **Question:** What is the difference between a Goal-Based Agent and a Utility-Based Agent?
*   **Answer:**
    *   **Goal-Based Agent:** Focuses on whether a state is a goal state or not (binary view: success/failure).
    *   **Utility-Based Agent:** Measures *how desirable* a state is using a utility function (scalar value). This allows trade-offs between conflicting goals or risk calculations under uncertainty.

---

### 🎴 Card 7: Learning Agent Components
*   **Question:** What are the four main components of a Learning Agent?
*   **Answer:**
    *   **Critic:** Evaluates the agent's performance against an external standard.
    *   **Learning Element:** Uses feedback from the critic to make improvements.
    *   **Performance Element:** The standard agent that selects external actions.
    *   **Problem Generator:** Suggests new exploratory actions to acquire new knowledge.

---

### 🎴 Card 8: Episodic vs. Sequential Environments
*   **Question:** What is the difference between an Episodic and a Sequential environment?
*   **Answer:**
    *   **Episodic:** The agent's experience is divided into independent episodes where the action in one episode does not affect future states (e.g., mail sorting).
    *   **Sequential:** Current decisions affect future states and the utility of future actions (e.g., Chess, driving).

---

### 🎴 Card 9: Static vs. Dynamic vs. Semidynamic Environments
*   **Question:** Differentiate between Static, Dynamic, and Semidynamic environments.
*   **Answer:**
    *   **Static:** The environment doesn't change while the agent is calculating its next action (e.g., crossword).
    *   **Dynamic:** The environment continues to change while the agent is deciding (e.g., driving).
    *   **Semidynamic:** The environment itself doesn't change, but the agent's performance score decreases as time passes (e.g., chess with a clock).