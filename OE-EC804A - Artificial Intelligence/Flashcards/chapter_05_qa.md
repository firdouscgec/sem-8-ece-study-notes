# Flashcards: Unit V - Constraint Satisfaction Problems

These active recall Question-and-Answer cards are designed to test your memory on the core definitions and problem formulations of Unit V.

---

### 🎴 Card 1: Definition of CSP
*   **Question:** What is a Constraint Satisfaction Problem (CSP) and what are its three components?
*   **Answer:** A problem where states are represented as variables that must satisfy specific constraints. The components are:
    1.  **Variables ($V$):** The items to be assigned values.
    2.  **Domains ($D$):** The set of allowed values for each variable.
    3.  **Constraints ($C$):** Restrictions specifying allowed value combinations.

---

### 🎴 Card 2: Standard Search vs. CSP Search
*   **Question:** How does the state representation in a CSP differ from standard state space search?
*   **Answer:**
    *   **Standard Search:** States are atomic "black boxes" (accessible only via successor functions).
    *   **CSP Search:** States have a factored representation (a set of variables and assignments), allowing general heuristics (like MRV or AC-3) to prune search spaces without domain-specific code.

---

### 🎴 Card 3: Australia Map-Coloring Variables
*   **Question:** Define the Variables and Domain for coloring the map of Australia with 3 colors.
*   **Answer:**
    *   **Variables ($V$):** $\{WA, NT, Q, NSW, V, SA, T\}$ (representing the 7 territories).
    *   **Domain ($D$):** $D_i = \{\text{Red}, \text{Green}, \text{Blue}\}$ for each variable.

---

### 🎴 Card 4: Cryptarithmetic Variables
*   **Question:** Formulate the Variables and Domains for the cryptarithmetic puzzle `SEND + MORE = MONEY`.
*   **Answer:**
    *   **Variables ($V$):** $\{S, E, N, D, M, O, R, Y\}$ (unique letters) and $\{C_1, C_2, C_3, C_4\}$ (column carries).
    *   **Domains ($D$):** $D_S, D_M = \{1..9\}$; others = $\{0..9\}$; carries = $\{0, 1\}$.

---

### 🎴 Card 5: M = 1 Deduction
*   **Question:** In the cryptarithmetic sum `SEND + MORE = MONEY`, why is $M$ mathematically forced to be $1$?
*   **Answer:** $M$ is the carry from adding the thousands column ($S + M + \text{carry}$). Since the sum of two single digits plus a carry is at most $9 + 9 + 1 = 19$, the carry to the next digit column ($M$) can only be $1$. Since $M$ cannot be $0$ (leading digit), $M = 1$.

---

### 🎴 Card 6: Backtracking Search in CSP
*   **Question:** What is Backtracking Search in the context of CSPs?
*   **Answer:** A Depth-First Search algorithm that chooses assignments for one variable at a time, checking for constraint violations. If a constraint is violated, it immediately backtracks, avoiding exploration of invalid subtrees.

---

### 🎴 Card 7: Flexible CSPs, Backtracking & Solver Languages (Q5.3)
*   **Question:** What is a Flexible CSP, how is a finite domain CSP typically solved, and which logic language is used for constraint programming?
*   **Answer:**
    *   **Flexible CSP:** A CSP where constraints are soft rather than hard. If no solution satisfies all constraints, it **relaxes constraints** to find an assignment that minimizes penalties or maximizes utility.
    *   **Backtracking Solver:** Finite domain CSPs are solved using **Backtracking Search** (depth-first sequential assignment), which is structurally based on a **LIFO (Last-In, First-Out)** stack and executed via **Recursion**.
    *   **Language:** **Prolog** is the standard programming language used, leveraging built-in backtracking and dedicated solvers like **CLP(FD)** (Constraint Logic Programming over Finite Domains).