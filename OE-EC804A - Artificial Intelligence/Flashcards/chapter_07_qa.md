# Flashcards: Unit VII - Logical Agents

These active recall Question-and-Answer cards are designed to test your memory on the propositional logic terms, inference rules, and Wumpus World properties of Unit VII.

---

### 🎴 Card 1: Tautology, Contradiction, Contingency
*   **Question:** Differentiate between Tautology, Contradiction, and Contingency.
*   **Answer:**
    *   **Tautology:** A sentence that is always True under all truth assignments (e.g., $P \lor \neg P$).
    *   **Contradiction:** A sentence that is always False under all truth assignments (e.g., $P \land \neg P$).
    *   **Contingency:** A sentence that can be either True or False depending on assignments (e.g., $P \land Q$).

---

### 🎴 Card 2: Modus Ponens
*   **Question:** State the syntax and working logic of Modus Ponens.
*   **Answer:**
    *   **Syntax:**
        $$\frac{P, \quad P \rightarrow Q}{Q}$$
    *   **Logic:** If premises $P$ and $P \rightarrow Q$ are true, then the conclusion $Q$ is true.

---

### 🎴 Card 3: Modus Tollens
*   **Question:** State the syntax and working logic of Modus Tollens.
*   **Answer:**
    *   **Syntax:**
        $$\frac{\neg Q, \quad P \rightarrow Q}{\neg P}$$
    *   **Logic:** If $P$ implies $Q$ and $Q$ is false, then $P$ must be false.

---

### 🎴 Card 4: Resolution Rule
*   **Question:** State the general syntax of the Resolution inference rule.
*   **Answer:**
    $$\frac{P \lor Q, \quad \neg P \lor R}{Q \lor R}$$
    Where $P \lor Q$ and $\neg P \lor R$ resolve to the resolvent $Q \lor R$ by eliminating the literal $P$ and its negation $\neg P$.

---

### 🎴 Card 5: TELL and ASK in KB-Agents
*   **Question:** What do the functions `TELL` and `ASK` represent in a Knowledge-Based Agent?
*   **Answer:**
    *   **TELL:** Adds new sentences (percepts or derived facts) to the Knowledge Base (KB).
    *   **ASK:** Queries the Knowledge Base to determine the next best action or confirm logical entailment.

---

### 🎴 Card 6: Wumpus World Sensors
*   **Question:** What are the five sensors of a Wumpus World agent?
*   **Answer:**
    1.  **Stench:** Felt in rooms adjacent to the Wumpus.
    2.  **Breeze:** Felt in rooms adjacent to pits.
    3.  **Glitter:** Felt in the exact room containing the gold.
    4.  **Bump:** Felt when the agent walks into a wall.
    5.  **Scream:** Heard anywhere when the Wumpus is killed.

---

### 🎴 Card 7: Pit and Wumpus logical rules
*   **Question:** Write the logical implications for Breeze and Stench in Wumpus World.
*   **Answer:**
    *   $\text{Breeze}(x,y) \Leftrightarrow \exists (i,j) \in Adjacent(x,y) : \text{Pit}(i,j)$ (Breeze if and only if an adjacent room has a pit).
    *   $\text{Stench}(x,y) \Leftrightarrow \exists (i,j) \in Adjacent(x,y) : \text{Wumpus}(i,j)$ (Stench if and only if adjacent room has the Wumpus).
    *   *No Breeze/Stench* implies *all* adjacent rooms are free of pits/Wumpus.

---

### 🎴 Card 8: Proposition Symbols & Semantics (Q7.4)
*   **Question:** What is the role of semantics in propositional logic, and how many constant proposition symbols exist in AI?
*   **Answer:**
    *   **Semantics:** Defines the rules used to compute the truth value of any sentence in a given model.
    *   **Constant Symbols:** Exactly **2 standard proposition symbols** represent fixed, constant truth values: **True** ($\top$) and **False** ($\bot$). Unlike standard variables, their truth values are immutable.

---

### 🎴 Card 9: Logical Inference Properties (Q7.4)
*   **Question:** How are validity, satisfiability, and logical equivalence used in logical inference algorithms?
*   **Answer:**
    *   **Validity:** A sentence is valid if it is true in all models. Logical entailment $\text{KB} \models \alpha$ is computed by showing that the implication $(\text{KB} \rightarrow \alpha)$ is valid.
    *   **Satisfiability:** A sentence is satisfiable if it is true in at least one model. $\text{KB} \models \alpha$ is proven by showing that $(\text{KB} \land \neg \alpha)$ is unsatisfiable (proof by contradiction).
    *   **Logical Equivalence:** Two sentences are equivalent if they share the same truth values in all models. This allows simplifying sentences or converting them to normal forms.

---

### 🎴 Card 10: CNF Equivalence, Unit Clause, and Resolution (Q7.4)
*   **Question:** Explain CNF conversion equivalence, define a Unit Clause, and explain why resolution is a "single inference rule".
*   **Answer:**
    *   **CNF Equivalence:** Every sentence of propositional logic can be converted to an inferred equivalent Conjunctive Normal Form (CNF) sentence. If the CNF sentence is unsatisfiable, the original statement is also unsatisfiable.
    *   **Unit Clause:** A clause containing exactly **a single literal** (representing a single literal of disjunction). It enables fast unit resolution.
    *   **Single Inference Rule:** Resolution is **refutation-complete**. It is the only inference rule needed to prove logical entailment (by deriving an empty clause/contradiction $\Box$), eliminating the need for multiple manual deduction rules.

