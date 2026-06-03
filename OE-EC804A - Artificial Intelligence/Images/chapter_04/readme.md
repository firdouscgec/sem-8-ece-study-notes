# Chapter 4 Diagrams

---

## 1. Heuristic Consistency Inequality Triangle
* **File Name:** `consistency_triangle.png`

```mermaid
graph TD
    n["Node n"]
    np["Successor Node n'"]
    Goal["Goal Node"]

    n -->|"c(n, a, n')"| np
    n -.->|"h(n)"| Goal
    np -.->|"h(n')"| Goal

    style n fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style np fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style Goal fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
```

---

## 2. A* Optimality Contradiction Tree
* **File Name:** `astar_optimality.png`

```mermaid
graph TD
    Start["Start Node"]
    n["Node n (on optimal path)"]
    G["Optimal Goal G <br> f(G) = C*"]
    G2["Suboptimal Goal G2 <br> f(G2) = g(G2) > C*"]

    Start --> n
    n --> G
    Start --> G2

    style Start fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style n fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style G fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    style G2 fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
```

---

## 3. 8-Puzzle State Transition Trace
* **File Name:** `puzzle_search_tree.png`

```mermaid
graph TD
    S["Root S <br> f = 5"]
    C["Node C <br> f = 5 (Blank Up)"]
    C1["Node C1 <br> f = 5 (Blank Left)"]
    C1_1["Node C1_1 <br> f = 5 (Blank Up)"]
    C1_1_2["Node C1_1_2 <br> f = 5 (Blank Down)"]
    G["Goal State <br> f = 5 (Blank Right)"]

    S --> C --> C1 --> C1_1 --> C1_1_2 --> G

    style S fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style G fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    classDef step fill:#fff,stroke:#333,stroke-width:1px,color:#000;
    class C,C1,C1_1,C1_1_2 step;
```

---

## 4. AND-OR Graph Decompositions
* **File Name:** `and_or_graph.png`

```mermaid
graph TD
    AI["Solve AI Course (OR Node)"]
    SelfStudy["Self Study"]
    Lectures["Attend Lectures (AND Node)"]
    Class["Attend Class"]
    HW["Do Homework"]

    AI --> SelfStudy
    AI --> Lectures
    
    Lectures --> Class
    Lectures --> HW
    
    Class -.->|AND| HW

    style AI fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Lectures fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style SelfStudy fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Class fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
    style HW fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
```
