# Flashcards: Unit VIII - FOL & Knowledge Representation

These active recall Question-and-Answer cards are designed to test your memory on the First-Order Logic rules, clausal conversions, and knowledge representation models of Unit VIII.

---

### 🎴 Card 1: Declarative vs. Procedural Knowledge
*   **Question:** What is the core difference between Declarative and Procedural knowledge?
*   **Answer:**
    *   **Declarative ("Knowing What"):** Static facts, assertions, and descriptions (e.g., $Man(Marcus)$). Easily modifiable but needs an interpreter.
    *   **Procedural ("Knowing How"):** Active rules, steps, and procedures (e.g., sorting algorithms). Executed directly but hard to modify.

---

### 🎴 Card 2: Definite Horn Clause
*   **Question:** What is a Horn Clause? Why is the implication $p \rightarrow q$ a Horn Clause?
*   **Answer:**
    *   **Horn Clause:** A disjunction of literals with at most one positive literal.
    *   **Implication:** $p \rightarrow q \equiv \neg p \lor q$. This contains exactly one positive literal ($q$), satisfying the Horn clause definition (a definite clause).

---

### 🎴 Card 3: Skolemisation
*   **Question:** What is Skolemisation, and how does it handle existentials inside universal quantifiers?
*   **Answer:**
    *   **Skolemisation:** The process of eliminating existential quantifiers ($\exists$) in FOPL.
    *   **Scope Rules:** If an existential variable $y$ is within the scope of universal variable $x$ (e.g., $\forall x \exists y P(x, y)$), $y$ is replaced by a Skolem function of $x$ (e.g., $P(x, f(x))$). Otherwise, it is replaced by a Skolem constant (e.g., $P(A)$).

---

### 🎴 Card 4: FOPL to CNF Conversion Steps
*   **Question:** Outline the 7 main steps to convert a FOL formula into Conjunctive Normal Form (CNF).
*   **Answer:**
    1.  Eliminate implications ($A \Rightarrow B \equiv \neg A \lor B$).
    2.  Move negations inward (De Morgan's).
    3.  Standardize variables (rename overlaps).
    4.  Skolemise existential quantifiers.
    5.  Drop universal quantifiers ($\forall$).
    6.  Distribute OR ($\lor$) over AND ($\land$).
    7.  Isolate clauses (each conjunct is a separate clause).

---

### 🎴 Card 5: Fuzzy Set Operations
*   **Question:** Write the mathematical expressions for Fuzzy Union, Intersection, and Complement.
*   **Answer:**
    *   **Union ($\cup$):** $\mu_{A \cup B}(x) = \max(\mu_A(x), \mu_B(x))$
    *   **Intersection ($\cap$):** $\mu_{A \cap B}(x) = \min(\mu_A(x), \mu_B(x))$
    *   **Complement ($\bar{A}$):** $\mu_{\bar{A}}(x) = 1 - \mu_A(x)$

---

### 🎴 Card 6: Crisp vs. Fuzzy Set
*   **Question:** Differentiate between a Crisp Set and a Fuzzy Set.
*   **Answer:**
    *   **Crisp Set:** Binary membership. An element is either completely in the set or not ($\mu(x) \in \{0, 1\}$).
    *   **Fuzzy Set:** Continuous membership. An element has a degree of membership between 0 and 1 ($\mu(x) \in [0, 1]$).

---

### 🎴 Card 7: Hebbian Learning
*   **Question:** What is Hebb's rule in neural networks and what is its equation?
*   **Answer:**
    *   **Rule:** The connection weight between two neurons increases if both neurons are active at the same time ("Neurons that fire together, wire together").
    *   **Equation:** $\Delta w_{ij} = \eta \times a_i \times a_j$ (where $\eta$ is learning rate, $a_i, a_j$ are activations).

---

### 🎴 Card 8: Genetic Algorithm Crossover vs. Mutation
*   **Question:** Compare Crossover and Mutation in Genetic Algorithms.
*   **Answer:**
    *   **Crossover:** Combines genetic code from two parent chromosomes to spawn new offspring (drives exploitation).
    *   **Mutation:** Randomly flips gene bits in a chromosome with low probability (drives exploration and diversity).
