# Chapter 3 Diagrams

---

## 1. 8-Puzzle Start and Goal States
* **File Name:** `eight_puzzle_states.png`

```mermaid
flowchart LR
    Start["<b>Start State</b><br>┌───┬───┬───┐<br>│ 2 │ 8 │ 3 │<br>├───┼───┼───┤<br>│ 1 │ 6 │ 4 │<br>├───┼───┼───┤<br>│ 7 │   │ 5 │<br>└───┴───┴───┘"]
    Goal["<b>Goal State</b><br>┌───┬───┬───┐<br>│ 1 │ 2 │ 3 │<br>├───┼───┼───┤<br>│ 8 │   │ 4 │<br>├───┼───┼───┤<br>│ 7 │ 6 │ 5 │<br>└───┴───┴───┘"]
    
    Start -->|Solve| Goal
    
    style Start fill:#fff,stroke:#ff9933,stroke-width:2px,color:#000
    style Goal fill:#fff,stroke:#33cc33,stroke-width:2px,color:#000
```

---

## 2. Water Jug Traced Solution Path
* **File Name:** `water_jug_trace.png`

```mermaid
graph TD
    S0["(0, 0) <br> Start"]
    S1["(0, 3)"]
    S2["(3, 0)"]
    S3["(3, 3)"]
    S4["(4, 2)"]
    S5["(0, 2)"]
    S6["(2, 0) <br> Goal Reached"]

    S0 -->|"Fill 3-Gal (Rule 2)"| S1
    S1 -->|"Pour 3-Gal -> 4-Gal (Rule 7)"| S2
    S2 -->|"Fill 3-Gal (Rule 2)"| S3
    S3 -->|"Pour 3-Gal -> 4-Gal until full (Rule 5)"| S4
    S4 -->|"Empty 4-Gal (Rule 3)"| S5
    S5 -->|"Pour 3-Gal -> 4-Gal (Rule 7)"| S6

    style S0 fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style S6 fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    classDef step fill:#fff,stroke:#333,stroke-width:1px,color:#000;
    class S1,S2,S3,S4,S5 step;
```

---

## 3. 8-Puzzle States with Heuristics and Path Cost
* **File Name:** `eight_puzzle_heuristics.png`

```mermaid
graph LR
    Start["<b>Start State</b><br>┌───┬───┬───┐<br>│ 2 │ 8 │ 3 │<br>├───┼───┼───┤<br>│ 1 │ 6 │ 4 │<br>├───┼───┼───┤<br>│ 7 │   │ 5 │<br>└───┴───┴───┘<br><br><b>g(n)=0</b><br><b>h(n)=5</b><br><b>f(n)=5</b>"] -->|"Move 4"| A["<b>State A</b><br>┌───┬───┬───┐<br>│ 2 │ 8 │ 3 │<br>├───┼───┼───┤<br>│ 1 │   │ 6 │<br>├───┼───┼───┤<br>│ 7 │ 4 │ 5 │<br>└───┴───┴───┘<br><br><b>g(n)=1</b><br><b>h(n)=4</b><br><b>f(n)=5</b>"]
    
    Start -->|"Move 8"| B["<b>State B</b><br>┌───┬───┬───┐<br>│ 2 │   │ 3 │<br>├───┼───┼───┤<br>│ 1 │ 8 │ 4 │<br>├───┼───┼───┤<br>│ 7 │ 6 │ 5 │<br>└───┴───┴───┘<br><br><b>g(n)=1</b><br><b>h(n)=5</b><br><b>f(n)=6</b>"]
    
    A -->|"Move 6"| C["<b>State C</b><br>┌───┬───┬───┐<br>│ 2 │ 8 │ 3 │<br>├───┼───┼───┤<br>│ 1 │ 6 │   │<br>├───┼───┼───┤<br>│ 7 │ 4 │ 5 │<br>└───┴───┴───┘<br><br><b>g(n)=2</b><br><b>h(n)=4</b><br><b>f(n)=6</b>"]
    
    B -->|"Move 6"| D["<b>State D</b><br>┌───┬───┬───┐<br>│ 2 │ 8 │ 3 │<br>├───┼───┼───┤<br>│ 1 │   │ 4 │<br>├───┼───┼───┤<br>│ 7 │ 6 │ 5 │<br>└───┴───┴───┘<br><br><b>g(n)=2</b><br><b>h(n)=5</b><br><b>f(n)=7</b>"]

    style Start fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style A fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style B fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style C fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    style D fill:#fff,stroke:#333,stroke-width:1px,color:#000
```
