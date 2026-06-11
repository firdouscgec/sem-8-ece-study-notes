---
description: Comprehensive overview of the Semester VIII repository layout, subjects, and study indexes.
---

# Semester VIII Directory & Resource Index

Welcome to the central resource guide for Semester VIII B.Tech ECE preparation (MAKAUT, West Bengal). This workspace acts as a modular preparation notebook mapped to your 4 selected subjects.

---

## 📚 Subject Directories

Select a subject below to view its detailed syllabus, progress trackers, notes, and study questions:

1. ### [PE-EC801B: Fiber Optic Communication](./PE-EC801B%20-%20Fiber%20Optic%20Communication/syllabus.md)
    * **L-T-P:** 3L:0T:0P | **Credits:** 3
    * *Covers: Vector nature of light, step index fibers, optical sources (LEDs/Lasers), detectors, WDM/DWDM systems, and non-linear effects.*
    * **Resources:** [Previous Year Questions](./PE-EC801B%20-%20Fiber%20Optic%20Communication/Questions/previous_year_questions.md) | [CA4 Questions](./PE-EC801B%20-%20Fiber%20Optic%20Communication/Questions/FOC_CA4_08-06-2026.md) | [Study Guide PDF](./PE-EC801B%20-%20Fiber%20Optic%20Communication/Exports/PE-EC801B_FOC_Study_Guide.pdf) | [Flashcards PDF](./PE-EC801B%20-%20Fiber%20Optic%20Communication/Exports/PE-EC801B_FOC_Flashcards.pdf) | [Quick Recall PDF](./PE-EC801B%20-%20Fiber%20Optic%20Communication/Exports/PE-EC801B_FOC_QuickRecall.pdf)

2. ### [PE-EC802B: Industrial Automation and Control](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/syllabus.md)
    * **L-T-P:** 3L:0T:0P | **Credits:** 3
    * *Covers: Sensors, Actuators, Signal Conditioning, PID Controller Tuning, PLC, DCS, SCADA, and Advanced Control Techniques.*
    * **Resources:** [Previous Year Questions](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/Questions/previous_year_questions.md) | [CA4 Questions](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/Questions/IA_CA4_09_06_2026.md) | [Study Guide PDF](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/Exports/PE-EC802B_Automation_Study_Guide.pdf) | [Flashcards PDF](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/Exports/PE-EC802B_Automation_Flashcards.pdf) | [Quick Recall PDF](./PE-EC802B%20-%20Industrial%20Automation%20and%20Control/Exports/PE-EC802B_Automation_QuickRecall.pdf)

3. ### [OE-EC803A: Internet of Things (IoT)](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/syllabus.md)
    * **L-T-P:** 3L:0T:0P | **Credits:** 3
    * *Covers: IoT Overview, Design Principles, Internet Protocols, Prototyping Embedded Devices, Manufacturing, and IoT Ethics.*
    * **Resources:** [Previous Year Questions](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/Questions/previous_year_questions.md) | [CA4 Questions](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/Questions/IoT_CA4_11_06_2026.md) | [Study Guide PDF](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/Exports/OE-EC803A_IoT_Study_Guide.pdf) | [Flashcards PDF](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/Exports/OE-EC803A_IoT_Flashcards.pdf) | [Quick Recall PDF](./OE-EC803A%20-%20Internet%20of%20Things(IoT)/Exports/OE-EC803A_IoT_QuickRecall.pdf)

4. ### [OE-EC804A: Artificial Intelligence](./OE-EC804A%20-%20Artificial%20Intelligence/syllabus.md)
    * **L-T-P:** 3L:0T:0P | **Credits:** 3
    * *Covers: Intelligent Agents, Search Strategies, Constraint Satisfaction, Adversarial Search (Games), and Logical/First-Order Agents.*
    * **Resources:** [Previous Year Questions](./OE-EC804A%20-%20Artificial%20Intelligence/Questions/previous_year_questions.md) | [CA4 Questions](./OE-EC804A%20-%20Artificial%20Intelligence/Questions/AI_CA4_12_06_2026.md) | [Study Guide PDF](./OE-EC804A%20-%20Artificial%20Intelligence/Exports/OE-EC804A_AI_Study_Guide.pdf) | [Flashcards PDF](./OE-EC804A%20-%20Artificial%20Intelligence/Exports/OE-EC804A_AI_Flashcards.pdf) | [Quick Recall PDF](./OE-EC804A%20-%20Artificial%20Intelligence/Exports/OE-EC804A_AI_QuickRecall.pdf)

---

## 📂 Repository Structure

Each subject directory uses an optimized structure designed for active recall, preparation status tracking, and LaTeX publication:

```text
.agents/
├── scripts/
│   ├── generate_flashcards_iot.py
│   ├── generate_flashcards_ai.py
│   ├── generate_flashcards_ia.py
│   ├── generate_flashcards_fiber.py
│   └── md_to_tex.py
├── skills/
│   ├── latex_skill.md
│   └── md_editing_skill.md
└── workflows/
    ├── instruction.md
    ├── readme.md
    └── workflow.md
[Subject Directory]/
├── syllabus.md
├── progress.md
├── quick_revision.md
├── Notes/
│   ├── chapter_01.md
│   └── chapter_02.md
├── Questions/
│   ├── previous_year_questions.md
│   ├── chapterwise_questions.md
│   └── final_questions.md
├── Flashcards/
│   └── chapter_01_qa.md
├── Images/
├── Latex/
│   ├── Main.tex
│   └── chapter_01.tex
└── Exports/
    └── notes.pdf
```

### 🔍 Directory & File Breakdown

#### **.agents/**
*   **`.agents/`**: Contains helper configurations, orchestration skills, automation scripts, and workflow guidelines.
    *   **`scripts/`**: Python automation scripts for resource generation.
        *   **`generate_flashcards_iot.py`**: Reads unit-wise active recall Q&A markdown files for IoT and compiles them into a beautiful, styled LaTeX two-column flashcard sheet.
        *   **`generate_flashcards_ai.py`**: Reads unit-wise active recall Q&A markdown files for AI and compiles them into a beautiful, styled LaTeX two-column flashcard sheet.
        *   **`generate_flashcards_ia.py`**: Reads unit-wise active recall Q&A markdown files for Industrial Automation and compiles them into a beautiful, styled LaTeX two-column flashcard sheet.
        *   **`generate_flashcards_fiber.py`**: Reads unit-wise active recall Q&A markdown files for Fiber Optic Communication and compiles them into a beautiful, styled LaTeX two-column flashcard sheet.
        *   **`generate_oneliners.py`**: Converts chapter-wise One-Liners markdown files into premium Quick Recall PDF guides using pdflatex.
        *   **`md_to_tex.py`**: Converts markdown chapter notes, tables, figures, equations, and quick revision guides into pdflatex-compatible tex files.
    *   **`skills/`**: Custom guidance and instruction files for markdown editing (`md_editing_skill.md`) and LaTeX management (`latex_skill.md`).
    *   **`workflows/`**: Preparation checklists and standards:
        *   **`readme.md`**: Master repository index (this file).
        *   **`workflow.md`**: Standard B.Tech ECE preparation workflow.
        *   **`instruction.md`**: Rules and instructions for drafting top-grade exam answers.


#### 1. Root Subject Files
*   **`syllabus.md`**: Official MAKAUT syllabus units and textbook catalogs.
*   **`progress.md`**: Checklist tracker showing status of notes, questions, flashcards, and revision.
*   **`quick_revision.md`**: High-priority revision index containing formulas, definitions, and visual diagrams.

#### 2. `Notes/`
*   Chapter-wise detailed study content and answers drafted in Markdown.

#### 3. `Questions/`
*   **`previous_year_questions.md`**: Master collection of past papers in Markdown.
*   **`chapterwise_questions.md`**: past questions sorted by syllabus chapter with frequency trends marked.
*   **`final_questions.md`**: Mapped master question catalog graded by priority rating and mark scale.

#### 4. `Flashcards/`
*   Q&A active recall flashcards (`chapter_01_qa.md`, etc.).

#### 5. `Images/`
*   Folder holding schematics and figures linked within study notes.

#### 6. `Latex/` & `Exports/`
*   **`Latex/`**: LaTeX configuration templates for compiling draft sheets into high-quality PDFs.
*   **`Exports/`**: Holds compiled final PDF documents.
