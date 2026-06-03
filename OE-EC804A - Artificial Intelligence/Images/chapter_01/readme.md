# Chapter 1 Diagrams

---

## 1. The Four Conceptual Approaches to AI Matrix
* **File Name:** `four_ai_approaches.png`

```mermaid
flowchart TD
    %% Rows represent Thinking/Acting, Columns represent Human-like/Rational
    subgraph Row1 ["THINKING PROCESSES"]
        direction LR
        A1["1. Thinking Humanly<br>(Cognitive Modeling)"]
        A2["2. Thinking Rationally<br>(Laws of Thought)"]
    end
    subgraph Row2 ["ACTING / BEHAVIOR"]
        direction LR
        B1["3. Acting Humanly<br>(Turing Test)"]
        B2["4. Acting Rationally<br>(Rational Agent)"]
    end
    
    classDef human fill:#ffe6cc,stroke:#ff9933,stroke-width:1px,color:#000;
    classDef rational fill:#e6f2ff,stroke:#3399ff,stroke-width:1px,color:#000;
    class A1,B1 human;
    class A2,B2 rational;
```

---

## 2. Turing Test Setup
* **File Name:** `turing_test_setup.png`

```mermaid
graph TD
    Interrogator["Human Interrogator"]
    Wall["Wall / Partition"]
    Human["Human Respondent"]
    AI["AI Computer"]

    Interrogator -->|Typed Text Only| Wall
    Wall --> Human
    Wall --> AI

    style Interrogator fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Human fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style AI fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
    style Wall fill:#f2f2f2,stroke:#666,stroke-width:2px,stroke-dasharray: 5 5,color:#000
```

---

## 3. Functional Sub-fields/Components of AI
* **File Name:** `ai_components.png`

```mermaid
graph TD
    AI["Autonomous AI System"]
    
    Sensing["Sensing<br>(Computer Vision, NLP, Speech)"]
    Reasoning["Reasoning & Planning<br>(Search, Logic, KR)"]
    Learning["Learning<br>(Machine Learning, Deep Learning)"]
    Acting["Acting<br>(Robotics, Control, Actuation)"]

    AI --> Sensing
    AI --> Reasoning
    AI --> Learning
    AI --> Acting

    style AI fill:#f2f2f2,stroke:#333,stroke-width:2px,color:#000
    style Sensing fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style Reasoning fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style Learning fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    style Acting fill:#ffe6e6,stroke:#ff3333,stroke-width:2px,color:#000
```

---

## 4. Expert System Architecture
* **File Name:** `expert_system_arch.png`

```mermaid
graph TD
    subgraph ES ["Expert System Boundary"]
        KB["Knowledge Base<br>(IF-THEN Rules, Facts)"]
        IE["Inference Engine<br>(Forward/Backward Chaining)"]
        UI["User Interface"]
    end
    
    User["Human User / Non-Expert"]

    KB <-->|"Rules & Facts"| IE
    IE <--> UI
    UI <-->|"Q & A / Recommendations"| User

    style ES fill:none,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5
    style KB fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style IE fill:#e6f2ff,stroke:#3399ff,stroke-width:2px,color:#000
    style UI fill:#e6ffe6,stroke:#33cc33,stroke-width:2px,color:#000
    style User fill:#f2f2f2,stroke:#666,stroke-width:2px,color:#000
```
