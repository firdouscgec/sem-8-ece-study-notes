# Chapter-wise Questions & Repeated Trends: OE-EC804A - Artificial Intelligence

This document organizes past years' MAKAUT exam questions (2014–2019) by syllabus chapter to analyze patterns, repeated trends, and priority areas.

---

## 📅 Unit I: Introduction
*Covers: Overview, Foundations, History, and the State of the Art of AI.*

### 1 Mark Questions (Group A)
*   **[1M][2019]** Artificial Intelligence is:
    *   (a) programming with intelligence
    *   (b) putting more memory to a computer
    *   (c) making machine intelligent
    *   (d) playing games
    *   *Answer:* (c) making machine intelligent
*   **[1M][2019]** What is the full form of STRIPS?
    *   (a) STandard Research Institute Problem Solver
    *   (b) STanford Research Institute Problem Solver
    *   (c) STdard Refinement of Information for Problem Solving
    *   (d) None of these
    *   *Answer:* (b) STanford Research Institute Problem Solver *(Historical Planning System)*

### 5 Mark Questions (Group B)
*   **[5M][★★][2019, Q3]** Describe different components of AI.
*   **[5M][★][2015, Q6]** What is an expert system? Why is it required?

### 15 Mark Questions (Group C)
*   *No standalone 15-mark questions have been asked solely on Unit I. Typically combined with Unit II Agents or search algorithms.*

---

## 📅 Unit II: Intelligent Agents
*Covers: Agents and Environment, Rationality, Nature of Environment, Structure of Agents (PEAS).*

### 1 Mark Questions (Group A)
*   **[1M][2019]** Which element in agent is used for selecting external actions?
    *   (a) Perceive | (b) Performance | (c) Learning | (d) Actuator
    *   *Answer:* (d) Actuator
*   **[1M][2017]** Agents are:
    *   (a) autonomous | (b) adaptive | (c) both (a) and (b) | (d) none of these
    *   *Answer:* (c) both (a) and (b)

### 5 Mark Questions (Group B)
*   **[5M][★★★★][2018, Q3 / 2017, Q3]** What is an agent in AI? What are the types of agent? Discuss about environment for agent.
*   **[5M][★★★][2016, Q3]** What is an agent? Describe various agent types.

### 15 Mark Questions (Group C)
*   **[15M][★★★][2017, Q9 / 2016, Q9]** Multi-part questions involving agents:
    *   **(a)** What is percept sequence? `[3M]`
    *   **(b)** What is agent system / Describe goal-based agent system? `[4M]`
    *   **(c)** What do you mean by a table-driven agent? What is the problem of this agent? `[4M]`

---

## 📅 Unit III: Solving Problems by Searching (Uninformed Search)
*Covers: Problem Formulation, State Space, BFS, DFS, DLS, IDDFS, Uniform-Cost Search (UCS).*

### 1 Mark Questions (Group A)
*   **[1M][2019]** When do we call the states are safely explorable?
    *   (a) A goal state is unreachable from any state
    *   (b) A goal state is denied access
    *   (c) A goal state is reachable from every state
    *   (d) None of the mentioned
    *   *Answer:* (c) A goal state is reachable from every state
*   **[1M][2019]** An algorithm is complete if:
    *   (a) it terminates with a solution when one exists
    *   (b) it starts with a solution
    *   (c) it does not terminate with a solution
    *   (d) it has a loop
    *   *Answer:* (a) it terminates with a solution when one exists
*   **[1M][2018 / 2017 / 2015]** Uninformed search is also known as:
    *   (a) Brute force search | (b) Hill climbing search | (c) Worst case search | (d) Blind search
    *   *Answer:* (d) Blind search
*   **[1M][2018 / 2017]** Depth first search procedure uses:
    *   (a) AND graph | (b) OR graph | (c) AND-OR graph | (d) none of these
    *   *Answer:* (b) OR graph
*   **[1M][2016]** Which search method takes less memory?
    *   (a) Depth-First Search | (b) Breadth-First Search | (c) Both (a) and (b) | (d) Linear Search
    *   *Answer:* (a) Depth-First Search

### 5 Mark Questions (Group B)
*   **[5M][★★★][2019, Q5]** Describe depth limited search.
*   **[5M][★★★★][2018, Q4 / 2017, Q4]** What is blind search technique? Explain with examples.
*   **[5M][★★★][2018, Q6]** Write iterative deepening algorithm with example.
*   **[5M][★★][2016, Q4]** A problem solving search can proceed either in the forward or the backward direction. Justify.
*   **[5M][★★★][2015, Q4]** What do you mean by completeness of a search? Why is DFS not always complete?

### 15 Mark Questions (Group C)
*   **[15M][★★★★★][2019, Q7]** Describe DFS. Does DFS always ensure completeness and optimality? Justify. Consider the arrangement and solve the 4-puzzle problem applying DFS.
*   **[15M][★★★★★][2019, Q10]** Describe state space search. What are the advantages of BFS over DFS and vice-versa? Does uniform cost search ensure completeness and optimality? Justify.
*   **[15M][★★★★★][2018, Q7]** Suppose you have the following search space (A $\rightarrow$ B cost 4, etc.). Assume that the initial state is A and the goal state is G. Show how each of the following search strategies would create a search tree to find a path and the cost: (i) BFS, (ii) DFS, (iii) Iterative deepening search.
*   **[15M][★★★★][2017, Q10]** Multi-part search question:
    *   **(a)** Is BFS identical to uniform cost search? Justify your answer. `[4M]`
    *   **(b)** Three missionaries and three cannibals river crossing problem: state space representation, production rules, and solution. `[7M]`
*   **[15M][★★★★][2016, Q10]** Multi-part search question:
    *   **(a)** When does BFS give optimal solution? `[3M]`
    *   **(b)** You are given two jugs, a 4-gallon one and a 3-gallon one. Neither have any measuring markers. Give the state-space diagram, production rules, and a possible solution to get exactly 2 gallons of water into the 4-gallon jug. `[8M]`

---

## 📅 Unit IV: Informed Search & Exploration
*Covers: Heuristic Functions, A* Search, Greedy Best-First Search, Hill-Climbing, Simulated Annealing, AO*.*

### 1 Mark Questions (Group A)
*   **[1M][2019]** Heuristic function h(n) is defined as the:
    *   (a) Lowest path cost
    *   (b) Cheapest path from root to goal node
    *   (c) Estimated cost of cheapest path from root to goal node
    *   (d) Average path cost
    *   *Answer:* (c) Estimated cost of cheapest path from root to goal node
*   **[1M][2019]** In many problems the path to goal is irrelevant, this class of problems can be solved using:
    *   (a) informed search | (b) uninformed search | (c) local search | (d) only (a) and (b)
    *   *Answer:* (c) local search techniques
*   **[1M][2018 / 2017]** An algorithm that gives optimal solution is:
    *   (a) Hill climbing | (b) BFS | (c) Blind search | (d) A*
    *   *Answer:* (d) A*
*   **[1M][2016]** A* algorithm is based on:
    *   (a) Breadth-first-search | (b) Depth-first-search | (c) Best-first-search | (d) Hill climbing
    *   *Answer:* (c) Best-first-search
*   **[1M][2016]** Which search agent operates by interleaving computation and action?
    *   (a) Offline search | (b) Online search | (c) Breadth-first search | (d) Depth-first search
    *   *Answer:* (b) Online search
*   **[1M][2015]** Which is NOT a heuristic search?
    *   (a) A* search | (b) steepest ascent Hill-climbing | (c) Simulated annealing | (d) Depth first search
    *   *Answer:* (d) Depth first search

### 5 Mark Questions (Group B)
*   **[5M][★★★★][2019, Q2]** Explain the working principle of simulated annealing algorithm.
*   **[5M][★★★★][2018, Q2]** Compare and contrast Best-First and Hill climbing search.
*   **[5M][★★★★][2015, Q2]** Multi-part heuristic questions:
    *   **(a)** What is the difference between Greedy best-first search and A* search? `[2M]`
    *   **(b)** Under what condition is breadth-first search optimal? `[1.5M]`
    *   **(c)** Show that any monotonic heuristic is admissible. `[1.5M]`

### 15 Mark Questions (Group C)
*   **[15M][★★★★★][2017, Q7 / 2016, Q7]** Core A* and Heuristic Analysis:
    *   **(a)** What do you mean by consistency/monotonicity of a heuristic? `[4M]`
    *   **(b)** Show that if a heuristic is consistent then f(n) is monotonically non-decreasing along any path. `[4M]`
    *   **(c)** Solve 8-puzzle using A* search from given Initial to Final state. Define state space, operations, heuristic, admissibility, and show the solution tree. `[7M]`
*   **[15M][★★★★][2018, Q10]** Heuristics and NLP:
    *   **(c)** Explain AO* algorithm with a suitable example. `[5M]`
*   **[15M][★★★★][2015, Q7]** Puzzle and A* Admissibility:
    *   **(a)** Solve the 3-puzzle problem using BFS, DFS, and A* search (with the heuristic being the number of misplaced tiles). `[10M]`
    *   **(b)** Prove that A* is admissible. `[5M]`
*   **[15M][★★★][2015, Q8]** Justifications:
    *   **(b)** Justify each of the following statements: (i) BFS is a special case of Uniform-Cost search, (ii) Uniform-Cost search is a special case of A* search. `[5M]`

---

## 📅 Unit V: Constraint Satisfaction Problems
*Covers: CSP formulation, Backtracking, Cryptarithmetic Problems, Local Search for CSPs.*

### 1 Mark Questions (Group A)
*   **[1M][2019]** Which type of mathematical problems are defined as a set of objects whose state must satisfy a number of constraints or limitations?
    *   (a) Constraints satisfaction Problems | (b) Uninformed Search | (c) Local Search | (d) Only (a) and (b)
    *   *Answer:* (a) Constraints satisfaction Problems

### 5 Mark Questions (Group B)
*   *No standalone 5-mark questions have been asked solely on CSPs (usually given as 10-mark numeric/cryptography problems in Group C).*

### 15 Mark Questions (Group C)
*   **[15M][★★★★★][2018, Q8]** Cryptarithmetic CSP:
    *   **(a)** What do you mean by constraint satisfaction problem? Solve the following cryptography problem using constraint satisfaction search: `SEND + MORE = MONEY`. `[10M]`

---

## 📅 Unit VI: Adversarial Search
*Covers: Game Playing, Minimax Algorithm, Alpha-Beta Pruning.*

### 1 Mark Questions (Group A)
*   **[1M][2018 / 2017]** Minimax algorithm search process obeys:
    *   (a) breadth first search fashion
    *   (b) depth first search fashion
    *   (c) best first search fashion
    *   (d) blind search fashion
    *   *Answer:* (b) depth first search fashion

### 5 Mark Questions (Group B)
*   *No standalone 5-mark questions have been asked solely on Adversarial Search.*

### 15 Mark Questions (Group C)
*   **[15M][★★★★★][2019, Q8]** Describe local beam search. Describe minimax procedure. Describe alpha-beta pruning procedure. `[15M]`
*   **[15M][★★★★★][2017, Q8]** Adversarial search and Fuzzy sets:
    *   **(a)** Consider the game tree where evaluation values at leaf nodes are given. Maximizer starts. (i) Apply minimax to determine moves, (ii) Show how many nodes will be pruned using alpha-beta pruning. `[8M]`
*   **[15M][★★★★★][2015, Q8]** Game Tree execution:
    *   **(a)** Consider the game tree (MAX at root, B/C/D next, etc., leaf values: 4, 3, 6, 2, 2, 1, 9, 5, 3, 1, 5, 4, 7, 5). (i) Using Minimax, determine moves, (ii) Execute Alpha-Beta pruning, count examined leaf nodes, and specify cutoffs. `[10M]`

---

## 📅 Unit VII: Logical Agents
*Covers: Knowledge-Based Agents, Propositional Logic, Syntax & Semantics, Tautology, Contradiction, Contingency, Modus Ponens, Resolution.*

### 1 Mark Questions (Group A)
*   **[1M][2019]** $P \lor \neg P$ is a:
    *   (a) tautology | (b) contradiction | (c) all false proposition | (d) none of these
    *   *Answer:* (a) tautology
*   **[1M][2015]** For a given proposition q, $q \lor \neg q$ is a:
    *   (a) tautology | (b) contradiction | (c) satisfiable formula | (d) none of these
    *   *Answer:* (a) tautology

### 5 Mark Questions (Group B)
*   **[5M][★★★★★][2018, Q5 / 2017, Q5]** What is tautology? Prove that $(((P \rightarrow Q) \rightarrow P) \rightarrow P)$ is a tautology. What are Modus Ponens and Modus Tollens?
*   **[5M][★★★][2016, Q2]** What do you mean by contradiction and contingency? Explain semantic network with proper example.

### 15 Mark Questions (Group C)
*   **[15M][★★★★][2017, Q11]** Tautologies and FOL proofs:
    *   **(a)** Prove that $P \lor \neg P$ is a Tautology. `[3M]`
    *   **(b)** What is contradiction? `[2M]`

---

## 📅 Unit VIII: First-Order Logic & Knowledge Representation
*Covers: FOL Syntax & Semantics, Clausal Form Conversion, Resolution Refutation, PROLOG, Semantic Nets, Frames, Conceptual Graphs, Neural Networks, Genetic Algorithms, Fuzzy Logic.*

### 1 Mark Questions (Group A)
*   **[1M][2019 / 2018 / 2017 / 2015]** Inheritable knowledge is best represented by:
    *   (a) semantic net | (b) FOPL | (c) database | (d) none of these
    *   *Answer:* (a) semantic net
*   **[1M][2019]** Resolution system can be used for:
    *   (a) question answering | (b) theorem proving | (c) both (a) and (b) | (d) none of these
    *   *Answer:* (c) both (a) and (b)
*   **[1M][2018 / 2017]** Frame is a collection of:
    *   (a) Slots | (b) Fillers/Filler | (c) Resolutions | (d) Knowledges
    *   *Answer:* (a) Slots
*   **[1M][2018 / 2017 / 2015]** A Bayesian network is a:
    *   (a) tree | (b) directed graph | (c) undirected graph | (d) none of these
    *   *Answer:* (b) directed graph
*   **[1M][2018 / 2017]** Horn clause is a clause with ____________ positive literals.
    *   (a) at most one | (b) at most two | (c) at least one | (d) at most four
    *   *Answer:* (a) at most one
*   **[1M][2018 / 2017]** The process of eliminating existential quantifiers is known as:
    *   (a) Resolution | (b) Skolemisation | (c) Unification | (d) None of these
    *   *Answer:* (b) Skolemisation
*   **[1M][2018 / 2017]** The rule used to change weight in Neural Network (NN) is:
    *   (a) Kirchoff's rule | (b) Hebb's rule | (c) Boehm's rule | (d) None of these
    *   *Answer:* (b) Hebb's rule
*   **[1M][2017]** MYCIN is an example of:
    *   (a) expert system | (b) knowledge base | (c) conceptual graph | (d) semantic net
    *   *Answer:* (a) expert system
*   **[1M][2016]** How the new states are generated in genetic algorithm?
    *   (a) Composition | (b) Mutation | (c) Cross-over | (d) Both (b) and (c)
    *   *Answer:* (d) Both (b) and (c)
*   **[1M][2016]** How do you represent "all dogs have tails"?
    *   (a) $\forall x : \text{dog}(x) \rightarrow \text{has\_tail}(x)$ | (b) $\forall x : \text{dog}(x) \rightarrow \text{has\_tail}(y)$
    *   *Answer:* (a) $\forall x : \text{dog}(x) \rightarrow \text{has\_tail}(x)$
*   **[1M][2016]** Which condition is used to cease the growth of forward chaining?
    *   (a) Atomic sentences | (b) Complex sentences | (c) No further inference | (d) All of the mentioned
    *   *Answer:* (c) No further inference
*   **[1M][2016]** Which is the most straight forward approach for planning algorithm?
    *   (a) Best-first search | (b) State-space search | (c) Depth-first search | (d) Hill-climbing search
    *   *Answer:* (b) State-space search
*   **[1M][2016]** Fuzzy logic is a form of:
    *   (a) Two-valued logic | (b) Crisp set logic | (c) Many-valued logic | (d) Binary set logic
    *   *Answer:* (c) Many-valued logic
*   **[1M][2016]** The truth values of traditional set theory is \_\_\_\_\_\_\_ and that fuzzy set is \_\_\_\_\_\_\_
    *   (a) Either 0 or 1, between 0 \& 1
    *   *Answer:* (a) Either 0 or 1, between 0 \& 1
*   **[1M][2015]** Which of the following is there in Prolog?
    *   (a) Existential quantifier | (b) Universal quantifier | (c) Conjunction | (d) Disjunction
    *   *Answer:* (b) Universal quantifier
*   **[1M][2015]** The first order logic is:
    *   (a) both sound and complete
    *   (b) sound but not complete
    *   (c) complete but not sound
    *   (d) neither sound nor complete
    *   *Answer:* (a) both sound and complete
*   **[1M][2015]** If in a problem the number of initial states is much more than the number of final states we should use:
    *   (a) backward reasoning | (b) forward reasoning | (c) both | (d) none
    *   *Answer:* (a) backward reasoning
*   **[1M][2015]** Which of the following is NOT a conflict resolution strategy in production system?
    *   (a) Production rules | (b) Recency | (c) Refraction | (d) Specificity
    *   *Answer:* (a) Production rules

### 5 Mark Questions (Group B)
*   **[5M][★★★][2019, Q6]** Describe neural network based learning.
*   **[5M][★★★][2018, Q8]** Write a program in PROLOG to compute the GCD of two numbers.
*   **[5M][★★★★][2017, Q6]** What do you mean by natural language processing (NLP)? What is parsing in NLP? What are the types of parsing? Draw the parsed tree of the sentence "The white dog crossed the road".
*   **[5M][★★★][2017, Q2]** Write a program in PROLOG or LISP to find GCD of N numbers. (OUT OF SYLLABUS)
*   **[5M][★★★][2016, Q5]** Write a prolog program to find out the Factorial of a number. (OUT OF SYLLABUS)
*   **[5M][★★★★][2016, Q6]** Distinguish between Declarative and Procedural Knowledge. What is a production system?

### 15 Mark Questions (Group C)
*   **[15M][★★★★★][2019, Q9]** Convert the following into clausal form and explain each step: $(\forall x)(P(x) \Rightarrow ((\forall y)(P(y) \Rightarrow P(f(x, y))) \land \neg (\forall y)(Q(x, y) \Rightarrow P(y))))$.
*   **[15M][★★★★★][2019, Q11]** Knowledge representation and Bayesian probability:
    *   **(a)** Briefly describe the issues in knowledge representation. `[5M]`
    *   **(b)** Given $P(A|B) = 0.20, P(A| \neg B) = 0.65, P(\neg A|B) = 0.12, P(\neg A| \neg B) = 0.03$. Now find $P(\neg A|B)$. `[5M]`
*   **[15M][★★★★★][2018, Q9]** FOL and Semantic Nets:
    *   **(a)** What is 'Horn Clause'? `[3M]`
    *   **(b)** What is Skolemisation? `[3M]`
    *   **(c)** Given text: "Everyone who enters in a theatre has to buy a ticket. Person who doesn't have money can't buy a ticket. Vinod enters a theatre." Prove by resolution that "Vinod has money". `[5M]`
    *   **(d)** With the help of semantic net, prove that Sourav is 6 feet tall and he is taller than Sachin. `[4M]`
*   **[15M][★★★★★][2018, Q10]** NLP steps and Parse tree:
    *   **(a)** Briefly explain the steps of Natural language Processing. `[5M]`
    *   **(b)** Generate the parse tree for the sentence 'The boy went to School'. `[5M]`
*   **[15M][★★★★★][2018, Q11]** Short notes (Conceptual Graph, Clausal Form steps). `[10M]`
*   **[15M][★★★★★][2017, Q8]** Fuzzy set operations:
    *   **(b)** Describe the fuzzy set operations like: union, intersection and complement. `[4M]`
*   **[15M][★★★★★][2017, Q9]** Genetic Algorithms and Agent systems:
    *   **(a)** Write the advantages of Genetic algorithm. `[3M]`
*   **[15M][★★★★★][2017, Q11]** Predicate logic resolution proof:
    *   **(c)** Represent the sentences using Predicate logic (X is Indian, Y Indian, Indian is man, Y assassinated X). Conclude Y hated X. `[10M]`
*   **[15M][★★★★★][2016, Q8]** Predicate Logic Proof:
    *   By using the predicate logic principles prove that "Marcus hated Caesar" (Marcus Pompeian, Romans, ruler, tried to assassinate Caesar). `[15M]`
*   **[15M][★★★★][2016, Q9]** Genetic Algorithms:
    *   **(c)** Write down the advantages and disadvantages of Genetic Algorithm. `[4M]`
*   **[15M][★★★★][2016, Q11]** Predicate representations:
    *   **(b)** Write predicate logic representations: (i) If it is bird, it can fly, (ii) Every father is parent, (iii) Every man has beaten the thief, (iv) Every person in the party loves every child. `[8M]`
    *   **(c)** What is horn clause? Show that $p \rightarrow q$ is a horn clause. `[3M]`
*   **[15M][★★★★★][2015, Q9]** Bayes network and reasoning:
    *   **(a)** Convert sentences into first order predicate logic: Everyone likes Ram, No one is perfect, Someone ate everything, All basketball players are tall. `[4M]`
    *   **(b)** Calculate $P(A|D)$ from the given Bayes network probabilities (Applicant qualified A, admitted D, GPA B, recommendation C). `[6M]`
    *   **(c)** Compare and Contrast between: (i) Forward and Backward reasoning, (ii) Inheritable knowledge and inferential knowledge. `[5M]`
*   **[15M][★★★★★][2015, Q10]** Clausal form and PROLOG:
    *   **(a)** Translate the formula into clausal form. `[5M]`
    *   **(b)** Prove by resolution "Vinod buys a ticket". `[5M]`
    *   **(c)** Write a program in PROLOG or LISP clause for having DOUBLE (L, LL). `[5M]`
*   **[15M][★★★★][2015, Q11]** Short notes on Genetic Algorithm, Semantic net, Neural Network, Fuzzy set. `[12M]`
