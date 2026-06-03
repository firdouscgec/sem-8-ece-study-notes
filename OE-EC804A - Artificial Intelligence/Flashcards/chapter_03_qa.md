# Flashcards: Unit III - Solving Problems by Searching

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, algorithms, and puzzle formulations of Unit III.

---

### 🎴 Card 1: Components of Problem Formulation
*   **Question:** What are the 5 core components of a formal problem formulation?
*   **Answer:**
    1.  **Initial State:** Where the agent starts.
    2.  **Actions:** Set of legal moves available in a state.
    3.  **Transition Model:** Specifies the outcome state $Result(s, a)$ of taking action $a$ in state $s$.
    4.  **Goal Test:** Condition checking if a state is the goal.
    5.  **Path Cost:** Metric tracking total step cost $g(n)$ from the start.

---

### 🎴 Card 2: Evaluation Criteria
*   **Question:** What are the four evaluation criteria for search algorithms?
*   **Answer:**
    1.  **Completeness:** Does it find a solution if one exists?
    2.  **Time Complexity:** How many nodes are generated/steps taken?
    3.  **Space Complexity:** How much memory is needed?
    4.  **Optimality:** Does it find the lowest path cost solution?

---

### 🎴 Card 3: BFS vs. DFS Space Complexity
*   **Question:** Contrast the space complexities of BFS and DFS. Explain the reason.
*   **Answer:**
    *   **BFS:** $O(b^d)$ (requires storing all generated frontier nodes at the current level in a queue).
    *   **DFS:** $O(bm)$ (only needs to store nodes along the single active path from root to leaf in a stack).

---

### 🎴 Card 4: DFS Incompleteness
*   **Question:** Why is DFS not complete?
*   **Answer:** Because DFS can get trapped in an infinite branch or a cycle. If this occurs on a branch to the left of the goal state, DFS will traverse down that infinite path forever and never backtrack to explore the goal.

---

### 🎴 Card 5: IDDFS Search Strategy
*   **Question:** What is the core strategy of Iterative Deepening DFS (IDDFS)?
*   **Answer:** It performs Depth-Limited DFS (DLS) repeatedly with increasing depth limits ($l = 0, 1, 2, \dots$) until a goal is found. It achieves BFS completeness and optimality ($O(b^d)$ time) with DFS space efficiency ($O(bd)$ space).

---

### 🎴 Card 6: Uniform-Cost Search (UCS) Order
*   **Question:** In what order does Uniform-Cost Search (UCS) expand nodes, and what data structure does it use?
*   **Answer:**
    *   **Order:** Expands the node with the lowest accumulated path cost $g(n)$ first.
    *   **Data Structure:** A **Priority Queue** ordered by path cost.

---

### 🎴 Card 7: Missionaries & Cannibals State Formulation
*   **Question:** Formulate the State tuple and safety constraints for the 3 Missionaries and 3 Cannibals problem.
*   **Answer:**
    *   **State:** $(M, C, B)$, where $M, C$ are the counts of missionaries and cannibals on the left bank, and $B$ is the boat location (1=left, 0=right).
    *   **Safety Constraints:** Left bank ($M \ge C$ if $M > 0$) AND Right bank ($(3-M) \ge (3-C)$ if $(3-M) > 0$).

---

### 🎴 Card 8: Water Jug State Formulation
*   **Question:** Formulate the State tuple, Initial State, and Goal State for the Water Jug problem (4-Gal and 3-Gal jugs).
*   **Answer:**
    *   **State:** $(x, y)$, where $x$ is water in 4-Gal jug, $y$ is water in 3-Gal jug.
    *   **Initial State:** $(0, 0)$
    *   **Goal State:** $(2, y)$, where $y$ is any amount.
