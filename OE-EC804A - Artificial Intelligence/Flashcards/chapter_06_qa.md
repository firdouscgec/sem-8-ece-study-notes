# Flashcards: Unit VI - Adversarial Search

These active recall Question-and-Answer cards are designed to test your memory on the core definitions, algorithms, and pruning rules of Unit VI.

---

### 🎴 Card 1: Zero-Sum Game
*   **Question:** What is a zero-sum game in AI?
*   **Answer:** A game in which the payoff to all players sum to zero at the end of the game. The utility gained by one player is exactly equal to the utility lost by the opponent (e.g., Chess, Tic-Tac-Toe).

---

### 🎴 Card 2: Minimax Algorithm
*   **Question:** What is the core logic of the Minimax algorithm?
*   **Answer:**
    *   It is a recursive algorithm that traverses the game tree in DFS order.
    *   **At MAX nodes:** Selects the maximum value of its successors.
    *   **At MIN nodes:** Selects the minimum value of its successors.
    *   Aims to determine the optimal move for MAX assuming the opponent plays optimally.

---

### 🎴 Card 3: Minimax Complexities
*   **Question:** What are the time and space complexities of the standard Minimax algorithm?
*   **Answer:**
    *   **Time Complexity:** $O(b^d)$ (Exponential).
    *   **Space Complexity:** $O(bd)$ (Linear space, storing the active search path).

---

### 🎴 Card 4: Alpha-Beta Pruning Values
*   **Question:** What do the variables $\alpha$ and $\beta$ represent in Alpha-Beta Pruning?
*   **Answer:**
    *   **Alpha ($\alpha$):** The value of the best (highest-value) choice found so far at any choice point along the path for MAX (initialized to $-\infty$).
    *   **Beta ($\beta$):** The value of the best (lowest-value) choice found so far at any choice point along the path for MIN (initialized to $+\infty$).

---

### 🎴 Card 5: The Pruning Condition
*   **Question:** What is the general mathematical pruning condition in Alpha-Beta search?
*   **Answer:** Pruning occurs whenever $\beta \le \alpha$. Any search branches below this point are cut off because they cannot influence the final decision.

---

### 🎴 Card 6: Alpha-Cutoff vs. Beta-Cutoff
*   **Question:** Differentiate between an Alpha-cutoff and a Beta-cutoff.
*   **Answer:**
    *   **Alpha-cutoff:** Occurs at a **MIN node** when a successor's value is $\le \alpha$ (parent MAX node's value).
    *   **Beta-cutoff:** Occurs at a **MAX node** when a successor's value is $\ge \beta$ (parent MIN node's value).

---

### 🎴 Card 7: Time Complexity with Pruning
*   **Question:** How does Alpha-Beta pruning improve the time complexity of the Minimax algorithm under perfect ordering?
*   **Answer:** With perfect node ordering (expanding best moves first), the time complexity is reduced from $O(b^d)$ to **$O(b^{d/2})$**. This allows the search to look twice as deep in the same amount of time.
