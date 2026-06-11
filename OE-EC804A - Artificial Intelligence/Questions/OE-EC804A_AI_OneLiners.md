# OE-EC804A: Artificial Intelligence - One-Liners

---

# Chapter 1: Introduction to Artificial Intelligence

1. Artificial Intelligence definition → Branch of computer science building smart, autonomous systems.
2. Standard modern approach to AI → Acting Rationally (Rational Agent approach).
3. Two dimensions of conceptual approaches to AI → Thought processes vs. behavior; human-like vs. rational.
4. Thinking Humanly focus → Mimicking cognitive activities and mental processes of humans.
5. Thinking Rationally focus → Using formal logic and laws of thought.
6. Acting Humanly focus → Performing actions indistinguishable from a human.
7. Acting Rationally focus → Maximizing expected performance or payoff.
8. Inventor of the Turing Test → Alan Turing.
9. Year Turing Test was introduced → 1950.
10. Original name of the Turing Test → The Imitation Game.
11. Duration of interrogation in Turing Test → 5 minutes.
12. NLP purpose in Turing Test → To communicate successfully in natural language.
13. Knowledge Representation purpose in Turing Test → To store information acquired before or during conversation.
14. Automated Reasoning purpose in Turing Test → To draw conclusions from stored information.
15. Machine Learning purpose in Turing Test → To adapt to new circumstances and detect patterns.
16. Two additional requirements for Total Turing Test → Computer Vision and Robotics.
17. Cognitive Science discipline contribution to AI → Mimicking human cognitive processes.
18. Philosophy contribution to AI → Rules of logic and mind-machine concepts.
19. Mathematics contribution to AI → Logic, probability, algorithms, and tractability.
20. Economics contribution to AI → Utility theory, decision theory, and game theory.
21. Neuroscience contribution to AI → Biological models of information processing (ANNs).
22. Psychology contribution to AI → Behavioral and cognitive models of human action.
23. Control Theory contribution to AI → Feedback loops and self-regulating systems.
24. Computer Vision main function → Extracting structured information from digital images or videos.
25. Natural Language Processing main function → Processing and analyzing human languages.
26. Machine Learning main function → Improving task performance automatically from training data.
27. Expert System definition → Software emulating human expert decision-making in a narrow domain.
28. Three main components of an Expert System → Knowledge Base, Inference Engine, and User Interface.
29. Expert System Knowledge Base storage format → IF-THEN production rules.
30. Forward Chaining search bias → Data-driven reasoning from facts to conclusions.
31. Backward Chaining search bias → Goal-driven reasoning starting from hypothesis to facts.
32. Explanation Facility purpose → Showing the step-by-step reasoning path of conclusion.
33. Major disadvantage of Expert Systems → Lack of general common-sense knowledge.
34. Knowledge Acquisition Bottleneck definition → Difficulty of extracting tacit knowledge from human experts.
35. System brittleness in Expert Systems → Crashing due to gaps or contradictions in rules.
36. Year of the Dartmouth workshop (AI birth) → 1956.
37. Who coined the term "Artificial Intelligence"? → John McCarthy.

# Chapter 2: Intelligent Agents

1. AI Agent definition → Anything perceiving environment through sensors and acting via actuators.
2. Percept Sequence definition → Complete history of all percepts received to date.
3. Agent Function mathematical mapping → $f: P^* \rightarrow A$
4. Agent Program definition → Concrete implementation of agent function on physical architecture.
5. Agent formula → $\text{Agent} = \text{Architecture} + \text{Program}$
6. PEAS acronym components → Performance, Environment, Actuators, Sensors.
7. PEAS Performance Measure for Automated Taxi → Safe arrival, passenger comfort, legal driving, and profit.
8. PEAS Environment for Automated Taxi → Roads, traffic, pedestrians, weather, and customers.
9. PEAS Actuators for Automated Taxi → Steering wheel, accelerator, brakes, horn, and display.
10. PEAS Sensors for Automated Taxi → Cameras, LIDAR, sonar, GPS, and speedometer.
11. PEAS Sensors for Medical Diagnosis System → Keyboard or voice input of symptoms.
12. Autonomy in agents → Behavior guided by own experience, not built-in designer knowledge.
13. Five basic agent structures → Simple reflex, model-based, goal-based, utility-based, learning agents.
14. Simple Reflex Agent action driver → Current percept only, using condition-action rules.
15. Key limitation of Simple Reflex Agents → Requires a fully observable environment.
16. Model-Based Reflex Agent key feature → Maintains internal state to track unobserved world aspects.
17. Goal-Based Agent action selector → Chooses actions that achieve explicit goal states.
18. Utility-Based Agent action selector → Maximizes a real-valued utility function indicating state preference.
19. Four components of a Learning Agent → Learning element, performance element, critic, problem generator.
20. Learning Element function → Making improvements by learning from experience.
21. Performance Element function → Selecting external actions to execute.
22. Critic function → Evaluating behavior against external performance standards.
23. Problem Generator function → Suggesting exploratory actions to discover new knowledge.
24. Fully Observable environment → Sensors detect complete state of environment at each point.
25. Partially Observable environment → Sensors have noise or gaps leaving state details unknown.
26. Deterministic environment → Next state completely determined by current state and action.
27. Stochastic environment → Next state contains random uncertainty.
28. Strategic environment → Uncertainty arises only from actions of other agents.
29. Episodic environment → Independent, atomic episodes where past actions don't affect future.
30. Sequential environment → Current decisions affect all future states and actions.
31. Static environment → Environment does not change during agent decision-making.
32. Dynamic environment → Environment changes while agent is deciding.
33. Semidynamic environment → Environment does not change, but performance score decreases with time.
34. Discrete environment → Finite or countable states, percepts, and actions.
35. Continuous environment → Continuous real variables represent environment states.
36. Chess with clock environment properties → Fully observable, strategic, sequential, semidynamic, discrete, multi-agent.
37. Taxi driving environment properties → Partially observable, stochastic, sequential, dynamic, continuous, multi-agent.

# Chapter 3: Solving Problems by Searching (Uninformed Search)

1. Problem-Solving Agent definition → Goal-based agent finding action sequences leading to goal states.
2. Five components of problem formulation → Initial state, actions, transition model, goal test, path cost.
3. Transition Model definition → Function $Result(s, a)$ returning state reached by action.
4. Path Cost formula → $g(n) = \text{sum of step costs along path}$.
5. State Space representation → Directed graph with states as nodes and actions as edges.
6. Four search evaluation criteria → Completeness, time complexity, space complexity, optimality.
7. Branching factor ($b$) → Maximum number of successors of any node.
8. Uninformed Search definition → Search using only problem definition without heuristic guidance.
9. BFS search strategy → Explores level-by-level, expanding all shallowest nodes first.
10. BFS frontier data structure → FIFO Queue (First-In, First-Out).
11. BFS Space Complexity → $O(b^d)$ (Exponential memory).
12. BFS Optimality condition → Step costs must be uniform.
13. DFS search strategy → Explores deep into a branch before backtracking.
14. DFS frontier data structure → LIFO Stack or Recursion.
15. DFS Space Complexity → $O(bm)$ (Linear memory).
16. Reason DFS is not complete → Can get trapped in infinite paths or loops.
17. DLS definition → DFS running with a pre-specified depth limit $l$.
18. IDDFS definition → Repeated DLS with increasing limits ($l = 0, 1, 2...$).
19. IDDFS Space Complexity → $O(bd)$ (Linear space).
20. IDDFS Completeness status → Complete (if $b$ is finite).
21. UCS node expansion criteria → Node with lowest accumulated path cost $g(n)$.
22. UCS frontier data structure → Priority Queue.
23. UCS Time and Space Complexity → $O(b^{1 + \lfloor C^*/\epsilon \rfloor})$.
24. UCS completeness condition → Step costs must be positive ($\ge \epsilon > 0$).
25. 8-Puzzle Initial State → Scrambled configuration of 8 numbered tiles in $3\times3$ grid.
26. 8-Puzzle Actions → Moving blank space Left, Right, Up, or Down.
27. Missionaries and Cannibals safety constraint → Cannibals must never outnumber missionaries on either bank.
28. Missionaries and Cannibals State representation → $(M, C, B)$ for Left bank values.
29. Goal state in River Crossing problem → $(0, 0, 0)$.
30. Water Jug Problem initial state → $(0, 0)$ (both jugs empty).
31. Water Jug Problem Goal State → $(2, y)$ where 4-gallon jug has 2 gallons.
32. Water Jug rule for filling 3-Gal jug → $(x, 3)$ if $y < 3$.
33. Water Jug rule for pouring 4-Gal into 3-Gal until full → $(x - (3 - y), 3)$ if $x+y \ge 3$.
34. Water Jug rule for pouring all 3-Gal into 4-Gal → $(x+y, 0)$ if $x+y \le 4$.

# Chapter 4: Informed Search & Exploration

1. Informed Search definition → Search using problem-specific heuristic knowledge to guide pathfinding.
2. Heuristic function $h(n)$ → Estimated cost of cheapest path from $n$ to goal.
3. Greedy Best-First Search evaluation function → $f(n)=h(n)$.
4. Greedy Best-First Search expansion bias → Expands node closest to goal.
5. Greedy Best-First Search space complexity → $O(b^l)$ (Exponential space).
6. A* Search evaluation function → $f(n)=g(n)+h(n)$.
7. A* Search completeness condition → Branching factor finite; step costs $\ge\epsilon>0$.
8. Admissible heuristic definition → Heuristic never overestimating true cost to goal ($0\le h(n)\le h^*(n)$).
9. Consistent (monotone) heuristic definition → $h(n)\le c(n,a,n')+h(n')$ (triangle inequality).
10. A* tree search optimality condition → Heuristic $h(n)$ must be admissible.
11. A* graph search optimality condition → Heuristic $h(n)$ must be consistent.
12. Relation between consistency and admissibility → Every consistent heuristic is admissible.
13. Monotonicity of $f$-values in A* → If $h(n)$ is consistent, $f(n)$ is non-decreasing along paths.
14. Manhattan Distance heuristic formula for 8-Puzzle → Sum of horizontal and vertical distances from goal.
15. Misplaced Tiles heuristic definition → Count of tiles not in their goal position.
16. Simulated Annealing working principle → Local search accepting bad moves with decreasing probability over time.
17. Simulated Annealing acceptance probability formula → $P = e^{\frac{\Delta E}{T}}$.
18. Impact of slow cooling in Simulated Annealing → Guaranteed to find global optimum with probability 1.
19. Impact of fast cooling in Simulated Annealing → Traps system in a local optimum.
20. Hill-Climbing Search definition → Greedy local search moving to neighbor with highest value.
21. Three limitations of Hill-Climbing → Local Maxima, Ridges, Plateaus.
22. Flat local maximum vs. Shoulder on a Plateau → Flat maximum has no exit; shoulder allows progression.
23. Solution to Hill-Climbing limitations → Random-Restart Hill Climbing.
24. Local Beam Search working principle → Tracks $k$ states in parallel, keeping best $k$ successors.
25. AO* Search application → Finding solutions in AND-OR graphs (decomposable problems).
26. AO* evaluation function for AND branch → $f(n) = g(n) + \sum h(\text{sub-problems})$.
27. Recursive Best-First Search (RBFS) Space Complexity → $O(bd)$ (Linear space).
28. RBFS backtracking trigger → When current node $f$-value exceeds the $f$-limit.
29. RBFS back-propagation mechanism → Replaces parent's $f$-value with best child's $f$-value on backtrack.
30. RBFS time complexity limitation → Exponential time due to node regeneration.

# Chapter 5: Constraint Satisfaction Problems

1. Factored state representation in CSPs → States are represented by variables, domains, and constraints.
2. Three core components of a CSP → Variables ($V$), Domains ($D$), Constraints ($C$).
3. Australia map-coloring variables → $\{WA, NT, Q, NSW, V, SA, T\}$.
4. Australia map-coloring domain values → $\{\text{Red}, \text{Green}, \text{Blue}\}$.
5. Australia map-coloring constraint type → Adjacent regions must have different colors ($WA \ne NT$).
6. Tasmania constraint isolation in Australia map → Tasmania has no constraints with other territories.
7. Cryptarithmetic variables in SEND + MORE = MONEY → Letters $\{S,E,N,D,M,O,R,Y\}$ and carries $\{C_1,C_2,C_3,C_4\}$.
8. Domain of leading letters ($S, M$) in Cryptarithmetic → $\{1..9\}$ (cannot be zero).
9. Alldifferent Constraint definition → Requires all variables in a set to be unique.
10. Column constraint for units column in SEND+MORE → $D + E = Y + 10 \times C_1$.
11. Solved value of $M$ in SEND+MORE → $M = 1$.
12. Solved value of $S$ in SEND+MORE → $S = 9$.
13. Solved value of $O$ in SEND+MORE → $O = 0$.
14. Final Cryptarithmetic equation solution → $9568 + 1085 = 10653$.
15. Flexible CSP definition → CSP where soft constraints/preferences are relaxed to resolve overconstraints.
16. Goal of Flexible CSP solver → Maximize preference utility or minimize violation penalty costs.
17. Backtracking Search strategy → Depth-first search instantiating variables sequentially, checking constraints.
18. Backtracking search data structure basis → LIFO stack and recursion.
19. Standard logic language for Constraint Programming → Prolog.
20. Prolog library for finite domain constraint solving → CLP(FD).
21. Chronological backtracking limit → Tends to repeat same failures down search tree (thrashing).
22. Constraint propagation definition → Using constraints to reduce variable domains before or during search.
23. Node consistency definition → Every value in variable's domain satisfies unary constraints.
24. Arc consistency (AC-3) definition → For every $X$ value, some $Y$ value is allowed.

# Chapter 6: Adversarial Search

1. Minimax definition → Recursive decision algorithm for two-player, zero-sum, perfect-information games.
2. Zero-sum game definition → Opponent's gain is exactly equal to player's loss.
3. Player MAX objective in Minimax → Maximize the final utility score.
4. Player MIN objective in Minimax → Minimize the MAX utility score.
5. Value propagated from child at a MAX node → Maximum of the child values.
6. Value propagated from child at a MIN node → Minimum of the children's values.
7. Minimax Time Complexity → $O(b^d)$ (Exponential).
8. Minimax Space Complexity → $O(bd)$ (Linear space).
9. Alpha-Beta Pruning definition → Optimization skipping subtrees that won't change minimax decision.
10. Alpha ($\alpha$) in pruning → Best (highest) choice found so far for MAX.
11. Beta ($\beta$) in pruning → Best (lowest) choice found so far for MIN.
12. Initial values of Alpha and Beta → $\alpha = -\infty$ and $\beta = +\infty$.
13. Pruning cutoff condition → When $\beta \le \alpha$.
14. Alpha-cutoff location → Occurs at a MIN node when $\beta \le \alpha$.
15. Beta-cutoff location → Occurs at a MAX node when $\beta \le \alpha$.
16. Time complexity of Alpha-Beta pruning with perfect ordering → $O(b^{d/2})$ (doubles solvable depth).
17. Does pruning change the optimal minimax decision? → No, it returns the identical move.
18. Leaf node evaluation order effect on pruning → Better moves evaluated first increase pruned branches.
19. Minimax game tree level representation → Alternate plies of MAX moves and MIN moves.
20. Evaluation function in real-time games → Estimates state utility when search limit is reached.

# Chapter 7: Logical Agents

1. Propositional Logic connectives → Negation ($\neg$), conjunction ($\land$), disjunction ($\lor$), implication ($\rightarrow$), biconditional ($\leftrightarrow$).
2. Soundness of inference → Algorithm derives only sentences that logically follow (derives truth).
3. Completeness of inference → Algorithm derives all sentences that logically follow.
4. Tautology definition → Sentence that is True under all possible models.
5. Contradiction (unsatisfiable) definition → Sentence that is False under all possible models.
6. Contingency definition → Sentence True in some models, False in others.
7. Peirce's Law formula → $(((P \rightarrow Q) \rightarrow P) \rightarrow P)$ (tautology).
8. Modus Ponens syntax → $\frac{P, \quad P \rightarrow Q}{Q}$.
9. Modus Tollens syntax → $\frac{\neg Q, \quad P \rightarrow Q}{\neg P}$.
10. Resolution rule syntax → $\frac{P \lor Q, \quad \neg P \lor R}{Q \lor R}$.
11. Unit Resolution syntax → $\frac{P \lor Q, \quad \neg P}{Q}$.
12. Knowledge-Based Agent definition → Agent utilizing structured Knowledge Base (KB) for logical reasoning.
13. KB-Agent TELL function → Adds new facts or percepts to the KB.
14. KB-Agent ASK function → Queries the KB for optimal next actions.
15. PEAS Environment of Wumpus World → $4\times4$ grid cave containing Wumpus, pits, and gold.
16. Stench sensor trigger in Wumpus World → Adjacent rooms to the Wumpus.
17. Breeze sensor trigger in Wumpus World → Adjacent rooms to pits.
18. Glitter sensor trigger in Wumpus World → Room containing the gold.
19. Wumpus World performance penalty for death → $-1000$ points.
20. Semantics in propositional logic → Rules computing truth value of sentences in a model.
21. Standard proposition symbols in AI → 2 constant symbols: True ($\top$) and False ($\bot$).
22. Validity inference relation → $\text{KB}\models\alpha$ if and only if $(\text{KB}\rightarrow\alpha)$ is valid.
23. Satisfiability inference relation → $\text{KB}\models\alpha$ if and only if $(\text{KB}\land\neg\alpha)$ is unsatisfiable.
24. CNF sentence definition → Conjunctive Normal Form (conjunction of disjunctions of literals).
25. Original statement satisfiability under CNF conversion → Satisfiability is preserved (CNF unsatisfiable implies original unsatisfiable).
26. Unit Clause definition → A clause containing exactly a single literal.
27. Why Resolution is a single inference rule → It is refutation-complete for reasoning.

# Chapter 8: First-Order Logic & Knowledge Representation

1. Declarative Knowledge definition → Static facts and assertions representing concepts ("knowing what").
2. Procedural Knowledge definition → Steps, rules, and procedures to perform tasks ("knowing how").
3. Production System components → Production rules (Rule Base), Working Memory, and Inference Engine.
4. Production System rule format → IF $\langle$Condition$\rangle$ $\rightarrow$ THEN $\langle$Action$\rangle$.
5. Recognize-Act cycle steps → Match rules, resolve conflict, execute action.
6. Horn Clause definition → A clause containing at most one positive literal.
7. Definite Clause definition → Horn clause with exactly one positive literal.
8. Implication conversion to Horn Clause ($p \rightarrow q$) → $\neg p \lor q$ (definite clause).
9. Fact in Horn Clauses → Horn clause with one positive, zero negative literals.
10. Goal Clause in Horn Clauses → Horn clause with zero positive literals.
11. Skolemisation definition → Eliminating existential quantifiers ($\exists$) by substituting concrete terms.
12. Skolem Constant substitution → $\exists x P(x) \Longrightarrow P(A)$ (no universal scope).
13. Skolem Function substitution → $\forall x\exists y P(x,y)\Longrightarrow\forall x P(x,F(x))$ (universal scope).
14. Prolog programming paradigm → Declarative logic programming language based on Horn clauses.
15. Prolog base case for factorial of 0 → `factorial(0, 1).`
16. Prolog mod operator in GCD recursive rule → `R is X mod Y.`
17. FOL to CNF conversion Step 1 → Eliminate implications/biconditionals ($A \rightarrow B \Rightarrow \neg A \lor B$).
18. Move negations inward FOL rule → $\neg \forall x P(x) \Longrightarrow \exists x \neg P(x)$.
19. Standardize variables step → Renaming variables to ensure unique names per quantifier.
20. Standard CNF format → Conjunction of disjunction of literals (conjunction of clauses).
21. Resolution Refutation proof method → Negate target goal, resolve with KB clauses to derive $\Box$.
22. Resolvent of $P(x) \lor Q(x)$ and $\neg P(A)$ using $\{x/A\}$ → $Q(A)$.
23. Semantic Network representation → Concept nodes connected by directed, labeled relation edges.
24. Frame-based representation attributes and values → Slots (attributes) and fillers (values).
25. Inheritance in Frames → Subclasses inherit default slot values from superclasses.
26. Fuzzy Set membership values → Real numbers representing membership degree in $[0, 1]$.
27. Fuzzy Union operator ($\cup$) → $\mu_{A \cup B}(x) = \max(\mu_A(x), \mu_B(x))$.
28. Fuzzy Intersection operator ($\cap$) → $\mu_{A \cap B}(x) = \min(\mu_A(x), \mu_B(x))$.
29. Fuzzy Complement operator ($\bar{A}$) → $\mu_{\bar{A}}(x) = 1 - \mu_A(x)$.
30. Difference between Crisp and Fuzzy Set → Crisp has membership $\{0,1\}$; Fuzzy has degree $[0,1]$.
31. Hebb's Rule neuroscience logic → Neurons firing together wire together ($\Delta w_{ij}=\eta a_i a_j$).
32. Crossover operator in Genetic Algorithms → Swapping genetic segments between two parent chromosomes.
33. Mutation operator in Genetic Algorithms → Randomly flipping gene values to maintain diversity.
