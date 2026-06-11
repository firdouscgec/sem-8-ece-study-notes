# Final Questions for Answering: OE-EC804A - Artificial Intelligence

This document lists the master set of study questions compiled to cover all core syllabus concepts, mapped to mark values and priority levels. Writing comprehensive answers to these questions will ensure complete exam readiness.

---

## 📅 Unit I: Introduction

### 📄 Short Answers (5 Marks)
*   **[5M][★★★] Q1.1:** What is Artificial Intelligence? Describe the four conceptual approaches to defining AI (Thinking Humanly, Thinking Rationally, Acting Humanly, Acting Rationally).
*   **[5M][★★] Q1.2:** Explain the **Turing Test** as a benchmark for human-like intelligence. What are the key capabilities a machine needs to pass the test?
*   **[5M][★★★] Q1.3:** Outline the major foundational disciplines that have contributed to the development of Artificial Intelligence (e.g., Philosophy, Mathematics, Economics, Neuroscience, Psychology, Control Theory).

### 📄 Long Answers (10 to 15 Marks)
*   **[10M][★★★★] Q1.4:** Discuss the different **components/sub-fields** of Artificial Intelligence in detail. Explain how they interact to build an autonomous system.
*   **[10M][★★★] Q1.5:** What is an **Expert System**? Explain its working principle, detailed architecture (including Knowledge Base, Inference Engine, and User Interface), and discuss its core advantages and limitations.

---

## 📅 Unit II: Intelligent Agents

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★] Q2.1:** What is an Agent in Artificial Intelligence? Discuss the difference between an Agent, its environment, and its percept sequence.
*   **[5M][★★★★★] Q2.2:** Define **PEAS** (Performance, Environment, Actuators, Sensors) description for an agent. Give a PEAS description for an automated taxi driver or an automated medical diagnosis system.

### 📄 Long Answers (10 to 15 Marks)
*   **[15M][★★★★★] Q2.3:** Discuss the five basic **agent structures** in detail. Draw a neat architectural block diagram for each, explain their working principles, and compare their capabilities:
    1.  Simple Reflex Agents
    2.  Model-Based Reflex Agents
    3.  Goal-Based Agents
    4.  Utility-Based Agents
    5.  Learning Agents
*   **[10M][★★★★] Q2.4:** What do you mean by the **nature of environments** in AI? Explain the following environment properties with examples:
    *   Accessible vs. Inaccessible (Fully vs. Partially Observable)
    *   Deterministic vs. Stochastic (Strategic)
    *   Episodic vs. Sequential
    *   Static vs. Dynamic
    *   Discrete vs. Continuous
    *   Single-agent vs. Multi-agent

---

## 📅 Unit III: Solving Problems by Searching (Uninformed Search)

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★] Q3.1:** What is a problem-solving agent? Define the steps involved in problem formulation and state space representation.
*   **[5M][★★★] Q3.2:** What are the four evaluation criteria for search algorithms? Define **Completeness**, **Time Complexity**, **Space Complexity**, and **Optimality**.
*   **[5M][★★★★] Q3.3:** Compare and contrast **Breadth-First Search (BFS)** and **Depth-First Search (DFS)** in a detailed feature table. Why is DFS not always complete?

### 📄 Long Answers (10 to 15 Marks)
*   **[15M][★★★★★] Q3.4:** Describe the working principle and write the step-by-step algorithms for **Iterative Deepening Depth-First Search (IDDFS)** and **Uniform-Cost Search (UCS)**. Discuss their completeness, time/space complexity, and optimality.
*   **[15M][★★★★★] Q3.5:** Formulate the state-space and draw search tree representations for the following classic puzzles:
    *   **3-Puzzle / 8-Puzzle Problem:** Show how the search space expands and how BFS, DFS, and UCS explore the nodes.
    *   **The Missionaries and Cannibals Problem (3M, 3C):** Define the state representation, valid operators, constraints, and show a step-by-step solution path.
    *   **The Water Jug Problem (4-gallon and 3-gallon jugs):** Formulate the state space, write the production rules, and trace the sequence of steps to obtain exactly 2 gallons of water in the 4-gallon jug.

---

## 📅 Unit IV: Informed Search & Exploration

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★★] Q4.1:** Differentiate between **Greedy Best-First Search** and **A* Search**. Under what conditions is A* search optimal and complete?
*   **[5M][★★★★] Q4.2:** Explain the terms **admissibility** and **consistency (monotonicity)** of a heuristic function. Show that any consistent heuristic is admissible.
*   **[5M][★★★] Q4.3:** Explain the **simulated annealing** search algorithm. How does the "cooling schedule" affect its probability of finding an optimal solution?
*   **[5M][★★★★] Q4.7:** **Greedy & Linear Space Search:** Explain why Greedy Best-First Search expands the node estimated to be closest to the goal and state its space complexity ($O(b^l)$). Explain how **Recursive Best-First Search (RBFS)** operates in linear space ($O(bd)$) to solve pathfinding problems.

### 📄 Long Answers (10 to 15 Marks)
*   **[10M][★★★★★] Q4.4:** Mathematical proofs in informed search:
    *   **(a)** Prove that A* search is **admissible** (optimal) when using an admissible heuristic on a tree search.
    *   **(b)** Prove that if a heuristic $h(n)$ is consistent, the $f$-value of nodes ($f(n) = g(n) + h(n)$) is monotonically non-decreasing along any path.
*   **[15M][★★★★★] Q4.5:** Solve the **8-Puzzle problem** from a given Initial State to a Goal State using **A* Search**. Define the state space, operators, step-by-step $g(n)$, $h(n)$ (using Manhattan distance or misplaced tiles), and draw the full search tree showing the final solution path.
*   **[10M][★★★★] Q4.6:** Discuss local search and optimization techniques:
    *   **Hill-Climbing Search:** Explain the algorithm and discuss its three major limitations (Local Maxima, Plateaus, and Ridges) and how to overcome them.
    *   **Local Beam Search:** Explain how it works and compare it to ordinary Hill-Climbing.
    *   **AO* Search:** Explain how it differs from A* search and provide a suitable example.

---

## 📅 Unit V: Constraint Satisfaction Problems

*   **[5M][★★★★] Q5.1:** What is a **Constraint Satisfaction Problem (CSP)**? Define the three core components of a CSP: Variables ($V$), Domains ($D$), and Constraints ($C$). Give a simple map-coloring example.
*   **[5M][★★★★] Q5.3:** **Flexible CSPs & Solver Languages:** What is a Flexible CSP and what does it relax? Explain the backtracking search logic for finite domain CSPs, and name the languages (e.g., Prolog) commonly used for Constraint Programming.

### 📄 Long Answers (10 to 15 Marks)
*   **[15M][★★★★★] Q5.2:** Solve the classic **Cryptarithmetic Problem** using Constraint Satisfaction Search:
    ```text
       SEND
     + MORE
     ------
      MONEY
    ```
    Clearly state all variables, domains, initial constraints, auxiliary variables (carries), and show the step-by-step deduction/backtracking process to assign unique digits (0-9) to each letter.

---

## 📅 Unit VI: Adversarial Search

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★] Q6.1:** Describe the **Minimax** game-playing procedure for two-player, zero-sum, perfect-information games. What is its time and space complexity?

### 📄 Long Answers (10 to 15 Marks)
*   **[15M][★★★★★] Q6.2:** Minimax and Alpha-Beta Pruning Execution:
    *   **(a)** Explain **Alpha-Beta Pruning**. What do $\alpha$ and $\beta$ represent, and how do they determine cutoffs?
    *   **(b)** Consider the game tree below. The Maximizer starts at the root node. 
        1.  Determine the minimax value at each node and state the optimal opening move.
        2.  Trace the execution of **Alpha-Beta Pruning** from left to right. Identify which branches are pruned, specify the type of cutoff ($\alpha$-cutoff or $\beta$-cutoff), and state the total number of terminal leaves examined.
        *(Note: Practice on a standard 3-level branching tree with leaves like [4, 3, 6, 2, 2, 1, 9, 5, 3, 1, 5, 4, 7, 5]).*

---

## 📅 Unit VII: Logical Agents

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★★] Q7.1:** Define **Tautology**, **Contradiction**, and **Contingency** in propositional logic. Prove that the formula $(((P \rightarrow Q) \rightarrow P) \rightarrow P)$ is a Tautology using a truth table.
*   **[5M][★★★★] Q7.2:** Explain the following logical inference rules with truth tables and syntax:
    *   Modus Ponens
    *   Modus Tollens
    *   Resolution Rule
*   **[5M][★★★★] Q7.4:** **Propositional Inference & Semantics:** Explain how the validity, satisfiability, and logical equivalence properties are used to compute logical inference. Define proposition symbols (specifying the two constant symbols: True and False) and semantics in propositional logic. Explain the unit clause concept, inferred equivalent CNF conversion, and why resolution is called a single inference rule.

### 📄 Long Answers (10 to 15 Marks)
*   **[10M][★★★★] Q7.3:** What is a **Knowledge-Based Agent**? Discuss the role of the Knowledge Base (KB) and the `KB-Agent` working loop (TELL, ASK). Describe the **Wumpus World** environment and explain how a logical agent reasons safely in it.

---

## 📅 Unit VIII: First-Order Logic & Knowledge Representation

### 📄 Short Answers (5 Marks)
*   **[5M][★★★★] Q8.1:** Differentiate between Declarative Knowledge and Procedural Knowledge. What is a **Production System** in knowledge representation?
*   **[5M][★★★★★] Q8.2:** Explain **Horn Clause** and **Skolemisation** in First-Order Logic:
    *   Define a Horn Clause. Show that the implication $p \rightarrow q$ is a Horn Clause.
    *   Define Skolemisation and explain how existential quantifiers ($\exists$) are eliminated using Skolem constants and functions.
*   **[5M][★★] Q8.3:** Write a simple recursive **PROLOG** program to compute the Greatest Common Divisor (GCD) or the Factorial of a number.

### 📄 Long Answers (10 to 15 Marks)
*   **[15M][★★★★★] Q8.4:** Conversion to **Clausal Form (CNF)** and **Resolution Refutation Proofs**:
    *   **(a)** List the step-by-step procedure to transform an arbitrary First-Order Logic formula into Clausal Form (CNF) (e.g., eliminating implications, moving negations inward, standardizing variables, Skolemisation, dropping universal quantifiers).
    *   **(b)** Convert the following logical formula into CNF: 
        \[ (\forall x)(P(x) \Rightarrow ((\forall y)(P(y) \Rightarrow P(f(x, y))) \land \neg (\forall y)(Q(x, y) \Rightarrow P(y)))) \]
    *   **(c)** Represent the following statements in First-Order Predicate Logic (FOPL) and prove the target goal using **Resolution Refutation**:
        *   *Statements:* "Everyone who enters in a theatre has bought a ticket. Person who does not have money can't buy a ticket. Vinod enters a theatre."
        *   *Goal:* Prove that "Vinod has money".
*   **[15M][★★★★★] Q8.5:** Predicate Logic Representation Case Study:
    *   **(a)** Translate the following facts into First-Order Predicate Logic (FOPL):
        1. Marcus was a man.
        2. Marcus was Pompeian.
        3. All Pompeians were Romans.
        4. Caesar was a ruler.
        5. All Romans were either loyal to Caesar or hated him.
        6. Everyone is loyal to someone.
        7. People only try to assassinate rulers they are not loyal to.
        8. Marcus tried to assassinate Caesar.
    *   **(b)** Prove that **"Marcus hated Caesar"** using Resolution Refutation. Draw the full resolution tree.
*   **[15M][★★★★] Q8.6:** Knowledge Representation Techniques (Short Notes & Architectural Overviews):
    *   **Semantic Networks:** Define semantic nets. Draw a semantic network to represent: "Sourav is 6 feet tall and is taller than Sachin."
    *   **Frames:** Explain slots, fillers, and inheritance in frame-based representation.
    *   **Fuzzy Logic:** Define a fuzzy set. Describe standard fuzzy set operations (Union, Intersection, Complement) with mathematical expressions. Differentiate between traditional crisp sets and fuzzy sets.
    *   **Neural Networks & Genetic Algorithms:** Discuss Hebb's rule for weight adjustments in Neural Networks and explain crossover/mutation mechanisms in Genetic Algorithms.
