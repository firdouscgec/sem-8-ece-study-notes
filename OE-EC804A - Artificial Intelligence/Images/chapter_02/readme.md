# Chapter 2 Diagrams

---

## 1. Environment-Agent Relationship
* **File Name:** `agent_environment.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Agent Boundary"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        Fn["Agent Function<br>f: P* ➔ A"]
    end

    Env -->|Percepts| Sensors
    Sensors -->|Percept History| Fn
    Fn -->|Selected Action| Actuators
    Actuators -->|Actions| Env

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style Fn fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
```

---

## 2. Simple Reflex Agent Structure
* **File Name:** `simple_reflex_agent.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Simple Reflex Agent"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        World["What the world is like now"]
        Rules["Condition-Action Rules"]
        Action["What action I should do"]
    end

    Env -->|Percepts| Sensors
    Sensors -->|Current Percept| World
    World --> Rules
    Rules --> Action
    Action --> Actuators
    Actuators -->|Action| Env

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style World fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Rules fill:#ffffd9,stroke:#cccc00,stroke-width:1px,color:#000
    style Action fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
```

---

## 3. Model-Based Reflex Agent Structure
* **File Name:** `model_based_agent.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Model-Based Reflex Agent"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        
        State["Internal State"]
        Evolution["How the world evolves"]
        Effects["What my actions do"]
        
        World["What the world is like now"]
        Rules["Condition-Action Rules"]
        Action["What action I should do"]
    end

    Env -->|Percepts| Sensors
    Sensors -->|Current Percept| World
    
    Evolution --> State
    Effects --> State
    State --> World
    
    World --> Rules
    Rules --> Action
    Action --> Actuators
    Actuators -->|Action| Env
    
    Action --> Effects

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style State fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style World fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Rules fill:#ffffd9,stroke:#cccc00,stroke-width:1px,color:#000
    style Action fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
    style Evolution fill:#f2f2f2,stroke:#999,stroke-width:1px,color:#000
    style Effects fill:#f2f2f2,stroke:#999,stroke-width:1px,color:#000
```

---

## 4. Goal-Based Agent Structure
* **File Name:** `goal_based_agent.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Goal-Based Agent"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        
        State["Internal State"]
        World["What the world is like now"]
        Goals["Goals"]
        Predict["What will it be like if I do action X?"]
        Action["What action I should do"]
    end

    Env -->|Percepts| Sensors
    Sensors -->|Current Percept| World
    State --> World
    World --> Predict
    Goals --> Predict
    Predict --> Action
    Action --> Actuators
    Actuators -->|Action| Env

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style State fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style World fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Goals fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
    style Predict fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Action fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
```

---

## 5. Utility-Based Agent Structure
* **File Name:** `utility_based_agent.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Utility-Based Agent"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        
        State["Internal State"]
        World["What the world is like now"]
        Utility["Utility Function"]
        Predict["How happy will I be in such a state?"]
        Action["What action I should do"]
    end

    Env -->|Percepts| Sensors
    Sensors -->|Current Percept| World
    State --> World
    World --> Predict
    Utility --> Predict
    Predict --> Action
    Action --> Actuators
    Actuators -->|Action| Env

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style State fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style World fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Utility fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
    style Predict fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style Action fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
```

---

## 6. Learning Agent Structure
* **File Name:** `learning_agent.png`

```mermaid
graph TD
    Env["Environment"]
    subgraph Agent ["Learning Agent"]
        Sensors["Sensors"]
        Actuators["Actuators"]
        
        Critic["Critic"]
        Learning["Learning Element"]
        ProblemGen["Problem Generator"]
        Performance["Performance Element"]
    end

    Env -->|Percept| Sensors
    Sensors -->|Percept| Performance
    Sensors -->|Percept| Critic
    
    Performance -->|Feedback| Critic
    Critic -->|Evaluation| Learning
    
    Learning -->|"Learning Goals"| ProblemGen
    Learning -->|"Performance Goals/Changes"| Performance
    
    ProblemGen -->|Exploratory Actions| Performance
    Performance -->|Action| Actuators
    Actuators -->|Action| Env

    style Env fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Agent fill:none,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5
    style Sensors fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Actuators fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style Critic fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000
    style Learning fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000
    style ProblemGen fill:#ffffd9,stroke:#cccc00,stroke-width:1px,color:#000
    style Performance fill:#e6ffe6,stroke:#33cc33,stroke-width:1px,color:#000
```
