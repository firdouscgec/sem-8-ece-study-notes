# Quick Revision: OE-EC804A - Artificial Intelligence

This high-yield index contains key definitions, formulas, repeated questions, practice diagrams, and last-minute revision points to review before exams.

---

## 📝 Unit I: Introduction

### 1. Important Definitions
*   **Artificial Intelligence:** Autonomous systems performing cognitive tasks that typically require human intelligence.
*   **Rational Agent:** An agent that acts to achieve the best possible (or best expected) outcome based on its inputs and knowledge.
*   **Turing Test:** An operational test where a computer is considered intelligent if a human interrogator cannot distinguish it from a human in textual conversations.
*   **Expert System:** Specialized interactive software emulating a human expert's decision-making in a narrow domain.
*   **Inference Engine:** The reasoning logic in an Expert System that applies facts/rules to draw conclusions.
*   **Forward Chaining:** Data-driven reasoning starting from known facts to reach a conclusion.
*   **Backward Chaining:** Goal-driven reasoning starting from a hypothesis/goal to find supporting facts.
*   **Knowledge Acquisition Bottleneck:** The slow, difficult task of extracting human expertise into rigid computer rules.

### 🧮 Key Formulas
*   *None for Unit I. (Note: Search complexities and Bayes probability formulas appear in later units).*

### ❓ Frequently Asked Questions
1.  **"Describe different components of AI." [5M][★★★★]**
    *   *Core point:* Focus on NLP, Machine Learning, Computer Vision, Robotics, and Expert Systems. Include the Sensing $\rightarrow$ Reasoning $\rightarrow$ Learning $\rightarrow$ Acting functional diagram.
2.  **"What is an Expert System? Explain its components." [10M][★★★]**
    *   *Core point:* Define ES. Draw the Knowledge Base $\leftrightarrow$ Inference Engine $\leftrightarrow$ User Interface block diagram. Detail forward/backward chaining. List 5 advantages and 5 disadvantages.

### 🎨 Diagrams to Practice
1.  **The Turing Test Setup:**  
    ![Turing Test Setup](../Images/chapter_01/turing_test_setup.png)
2.  **Expert System Block Diagram:**  
    ![Expert System Architecture](../Images/chapter_01/expert_system_arch.png)

### ⚡ One-Line Revision
*   AI is divided into 4 views: Thinking/Acting Humanly (behavioral) and Thinking/Acting Rationally (performance-driven).
*   Acting Rationally (Rational Agent approach) is the standard modern paradigm of AI studies.
*   The Turing Test requires NLP, Knowledge Representation, Automated Reasoning, and Machine Learning.
*   The Total Turing Test adds Computer Vision and Robotics.
*   Expert Systems use rigid **IF-THEN production rules** for representation.
*   Forward Chaining is **data-driven**; Backward Chaining is **goal-driven**.

---

## 📝 Unit II: Intelligent Agents

### 1. Important Definitions
*   **Agent:** Anything that perceives its environment through sensors and acts upon it through actuators.
*   **Percept Sequence:** The complete history of all percepts received by the agent to date.
*   **Agent Function ($f$):** A mathematical mapping $f: P^* \rightarrow A$ from any percept sequence to an action.
*   **Agent Program:** The concrete implementation of the agent function running on the physical architecture.
*   **PEAS:** Performance measure, Environment, Actuators, Sensors. Used to specify the task environment.
*   **Rational Agent:** An agent that selects actions to maximize its expected performance measure given its percept history and knowledge.
*   **Autonomy:** An agent behaves with autonomy if its behavior is determined by its own experience rather than depending solely on built-in designer knowledge.

### 🧮 Key Formulas
*   $\text{Agent} = \text{Architecture} + \text{Program}$
*   $f: P^* \rightarrow A$ (Agent Function mapping percept history to action)

### ❓ Frequently Asked Questions
1.  **"Define PEAS description for an automated taxi driver." [5M][★★★★★]**
    *   *Core point:* P: Safety, speed, comfort, profits. E: Roads, traffic, pedestrians. A: Steering, gas, brakes, display. S: Cameras, LIDAR, GPS, speedometer.
2.  **"Explain the five basic agent structures." [15M][★★★★★]**
    *   *Core point:* Simple Reflex (percept-action rules), Model-Based (uses state to track unobserved world), Goal-Based (uses goals to plan), Utility-Based (uses utility function for state preference), Learning Agent (Critic, Learning Element, Performance Element, Problem Generator).

### 🎨 Diagrams to Practice
1.  **Simple Reflex and Model-Based Agents:**  
    ![Simple Reflex Agent Structure](../Images/chapter_02/simple_reflex_agent.png)
    ![Model-Based Reflex Agent Structure](../Images/chapter_02/model_based_agent.png)
2.  **Learning Agent Architecture:**  
    ![Learning Agent Structure](../Images/chapter_02/learning_agent.png)

### ⚡ One-Line Revision
*   An agent acts using actuators and senses using sensors.
*   A simple reflex agent uses current percepts only; model-based reflex agents use internal states to track the unobserved environment.
*   Goal-based agents plan to achieve goals; utility-based agents maximize a real-valued performance metric.
*   A learning agent separates the critic (evaluator) from the learning element (improver) and the problem generator (explorer).
*   Environments can be fully/partially observable, deterministic/stochastic, episodic/sequential, static/dynamic, discrete/continuous, single/multi-agent.

---

## 📝 Unit III: Solving Problems by Searching (Uninformed Search)

### 1. Important Definitions
*   **Uninformed Search (Blind Search):** Search algorithms that do not use any problem-specific knowledge (heuristics) to guide the search process. They only use the problem definition to explore the state space.
*   **State Space:** The set of all possible configurations (states) the problem can be in.
*   **Initial State:** The starting configuration of the problem.
*   **Goal State:** The desired configuration that the search aims to find.
*   **Operators (Successor Function):** Actions that can be applied to a state to transition to a new state.
*   **Path:** A sequence of states from the initial state to a goal state.
*   **Cost:** The cost associated with applying an operator (usually 1 for unweighted graphs).

### 2. Characteristics of Uninformed Search
*   **No Heuristics:** Does not use any problem-specific knowledge to guide the search.
*   **Systematic Exploration:** Explores the state space systematically to find a solution.
*   **Completeness:** Guaranteed to find a solution if one exists (depending on the algorithm).
*   **Optimality:** Guaranteed to find the optimal (lowest cost) solution if one exists (depending on the algorithm).
*   **Memory Usage:** Can be memory-intensive as it may need to store large portions of the state space.

### 3. Important Search Algorithms
1.  **Breadth-First Search (BFS):** 
    *   **Principle:** Explores the state space level by level. It expands all nodes at the current depth before moving to the next depth level. Uses a queue data structure.
    *   **Completeness:** Yes, if a solution exists and the branching factor is finite.
    *   **Optimality:** Yes, if the cost of each step is uniform (e.g., 1). Finds the shortest path in terms of number of edges.
    *   **Time/Space Complexity:** $O(b^d)$, where $b$ is branching factor and $d$ is depth.
2.  **Depth-First Search (DFS):**
    *   **Principle:** Explores as far as possible along each branch before backtracking. Uses a stack data structure.
    *   **Completeness:** No, fails in infinite paths or cycles.
    *   **Optimality:** No.
    *   **Time/Space Complexity:** Time: $O(b^m)$, Space: $O(bm)$ (where $m$ is max depth).
3.  **Depth-Limited Search (DLS):**
    *   **Principle:** DFS with a depth limit $l$ imposed.
4.  **Iterative Deepening Search (IDDFS):**
    *   **Principle:** Performs DLS with increasing limits $l = 0, 1, 2...$ Combines DFS space efficiency $O(bd)$ with BFS completeness and optimality.
5.  **Uniform Cost Search (UCS):**
    *   **Principle:** Expands the node with the lowest path cost $g(n)$ using a priority queue. Optimal for arbitrary step costs.

### 4. Algorithm Properties
| Property | BFS | DFS | DLS | IDDFS | UCS |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Completeness** | Yes | No | No | Yes | Yes |
| **Time Complexity** | $O(b^d)$ | $O(b^m)$ | $O(b^l)$ | $O(b^d)$ | $O(b^{1 + \lfloor C^*/\epsilon \rfloor})$ |
| **Space Complexity** | $O(b^d)$ | $O(bm)$ | $O(bl)$ | $O(bd)$ | $O(b^{1 + \lfloor C^*/\epsilon \rfloor})$ |
| **Optimality** | Yes (uniform) | No | No | Yes (uniform) | Yes |

### 🎨 Diagrams to Practice
1.  **Water Jug Solution Path:**  
    ![Water Jug Traced Solution Path](../Images/chapter_03/water_jug_trace.png)

---

## 📝 Unit IV: Informed Search & Exploration

### 1. Important Definitions
*   **Informed Search (Heuristic Search):** Search algorithms that use problem-specific knowledge (heuristics) to guide the search process. They use an evaluation function to estimate the cost from the current state to the goal state.
*   **Heuristic Function ($h(n)$):** An informed guess about the cost from the current state to the goal state. It is used to guide the search process.
*   **Evaluation Function ($f(n)$):** A function that evaluates the cost of a state. It is used to guide the search process.

### 2. Important Algorithms
1.  **Greedy Best-First Search:**
    *   **Principle:** Expands the node that appears to be closest to the goal state, as estimated by the heuristic function.
    *   **Evaluation Function:** $f(n) = h(n)$
    *   **Completeness/Optimality:** No.
2.  **A* Search:**
    *   **Principle:** Expands the node that appears to be closest to the goal state, as estimated by the evaluation function $f(n)$.
    *   **Evaluation Function:** $f(n) = g(n) + h(n)$, where $g(n)$ is the cost from the start state to the current state, and $h(n)$ is the estimated cost from the current state to the goal state.
    *   **Completeness/Optimality:** Yes, if $h(n)$ is admissible (tree search) or consistent (graph search).
3.  **Local Search and Optimization Techniques:**
    *   **Hill-Climbing Search:** Greedy algorithm that moves to the neighboring state with the highest heuristic value. Fails at local maxima, ridges, and plateaus.
    *   **Local Beam Search:** Tracks $k$ states instead of just one, expanding all successors and keeping the best $k$.
    *   **AO* Search:** Used for search trees representing AND-OR graphs (decomposable problems).

### 🎨 Diagrams to Practice
1.  **Heuristic Consistency Triangle:**  
    ![Heuristic Consistency Inequality Triangle](../Images/chapter_04/consistency_triangle.png)
2.  **AND-OR Graph Decompositions:**  
    ![AND-OR Graph Decompositions](../Images/chapter_04/and_or_graph.png)

---

## 📝 Unit V: Constraint Satisfaction Problems

### 1. Important Definitions
*   **Constraint Satisfaction Problem (CSP):** A problem defined by a set of variables, domains (allowed values), and constraints restricting value combinations.
*   **Backtracking Search:** DFS-based search for CSPs where variables are assigned sequentially and reverted on constraint violation.
*   **Alldifferent Constraint:** A global constraint specifying that all variables in a set must be assigned unique values.

### ❓ Frequently Asked Questions
1.  **"Solve the cryptarithmetic problem: SEND + MORE = MONEY." [15M][★★★★★]**
    *   *Core point:* Set up variables, domains, and column carry constraints. Solve sequentially: $M=1$ (carry), $O=0$, $S=9$, $C_3=0$, $C_2=1$, $N=E+1$. Find remaining digits: $R=7$, $E=5$, $N=6$, $D=8$, $Y=3$.

### 🎨 Diagrams to Practice
1.  **Australia Constraint Graph:**  
    ![Australia Map-Coloring Outline](../Images/chapter_05/australia_map.png)

### ⚡ One-Line Revision
*   CSPs use a factored state representation (variables and constraints) instead of atomic black boxes.
*   Backtracking is the standard complete search algorithm for CSPs.

---

## 📝 Unit VI: Adversarial Search

### 1. Important Definitions
*   **Adversarial Search:** Search algorithms used in competitive, multi-agent environments (games).
*   **Minimax Algorithm:** A recursive algorithm that calculates optimal moves in zero-sum games by maximizing for MAX and minimizing for MIN.
*   **Alpha-Beta Pruning:** An optimization that skips evaluating subtrees that cannot possibly affect the final minimax decision.
    *   *Alpha ($\alpha$):* The best (highest) utility value found so far for MAX.
    *   *Beta ($\beta$):* The best (lowest) utility value found so far for MIN.

### ❓ Frequently Asked Questions
1.  **"Explain Alpha-Beta Pruning with a trace." [15M][★★★★★]**
    *   *Core point:* Explain $\alpha$ and $\beta$. Prune branches whenever $\beta \le \alpha$ (alpha-cutoff at MIN node, beta-cutoff at MAX node). Show a sample tree with leaf evaluations and marked cutoffs.

### 🎨 Diagrams to Practice
1.  **Pruned Game Tree:**  
    ![Alpha-Beta Pruning Game Tree](../Images/chapter_06/alphabeta_tree.png)

### ⚡ One-Line Revision
*   Standard minimax has time complexity $O(b^d)$, which is reduced to $O(b^{d/2})$ with perfect alpha-beta pruning.
*   Pruning does not change the optimal move selection; it only speeds up the search.

---

## 📝 Unit VII: Logical Agents

### 1. Important Definitions
*   **Propositional Logic:** A logic system dealing with propositions (T/F statements) and connectives ($\land, \lor, \neg, \rightarrow, \leftrightarrow$).
*   **Soundness:** An inference rule is sound if it only derives true sentences from true premises.
*   **Completeness:** An inference rule is complete if it can derive all sentences entailed by the premises.
*   **Tautology:** A sentence that is True under all truth assignments (e.g., Peirce's Law: $(((P \rightarrow Q) \rightarrow P) \rightarrow P)$).
*   **Modus Ponens:** Inference rule of form: $\frac{P, \quad P \rightarrow Q}{Q}$.
*   **Modus Tollens:** Inference rule of form: $\frac{\neg Q, \quad P \rightarrow Q}{\neg P}$.

### ❓ Frequently Asked Questions
1.  **"Prove that Peirce's Law is a Tautology." [5M][★★★★★]**
    *   *Core point:* Construct a 4-row truth table for $P, Q$. Compute column-wise: $P \rightarrow Q$, $(P \rightarrow Q) \rightarrow P$, and the final implication, proving all rows are True.
2.  **"Explain Wumpus World environment." [10M][★★★★]**
    *   *Core point:* State PEAS components. Show how Breeze maps to Pit and Stench to Wumpus, and trace safety reasoning.

### 🎨 Diagrams to Practice
1.  **Wumpus World Grid:**  
    ![Wumpus World Grid Layout](../Images/chapter_07/wumpus_world_grid.png)

### ⚡ One-Line Revision
*   Knowledge-based agents query the KB with `ASK` and insert facts/percepts with `TELL`.
*   Propositional logic is monotonic but lacks variables and quantifiers.

---

## 📝 Unit VIII: First-Order Logic & Knowledge Representation

### 1. Important Definitions
*   **First-Order Logic (FOL):** Logic system representing objects, properties, relations, and quantifiers ($\forall, \exists$).
*   **Horn Clause:** A clause containing at most one positive literal. Basis of PROLOG.
*   **Skolemisation:** Eliminating existential quantifiers by replacing them with unique constants or functions (when inside universal scopes).
*   **Semantic Network:** A graph with concept nodes and directed, labeled relation edges.
*   **Fuzzy Logic:** A multi-valued logic representing degrees of membership in a set using real numbers in $[0, 1]$.

### ❓ Frequently Asked Questions
1.  **"Convert a FOL formula into Clausal Form (CNF)." [15M][★★★★★]**
    *   *Core point:* Follow the 7 steps: eliminate implications, move negations inward, standardize variables, Skolemise, drop $\forall$, distribute $\lor$ over $\land$, isolate clauses.
2.  **"Prove Marcus hated Caesar using Resolution Refutation." [15M][★★★★★]**
    *   *Core point:* Translate statements into FOPL clauses. Negate the goal ($\neg Hate(Marcus, Caesar)$). Apply resolution to derive the empty clause ($\Box$).

### 🎨 Diagrams to Practice
1.  **Semantic Net Diagram:**  
    ![Semantic Network](../Images/chapter_08/semantic_network.png)
2.  **Resolution Refutation Proof Tree:**  
    ![Resolution Refutation Proof Tree](../Images/chapter_08/resolution_steps.png)

### ⚡ One-Line Revision
*   Fuzzy union uses $\max$ and intersection uses $\min$ of membership functions.
*   Hebbian learning in NN adjusts weights according to $\Delta w_{ij} = \eta a_i a_j$.
*   Genetic algorithms search using populations, selection, crossover, and mutation.