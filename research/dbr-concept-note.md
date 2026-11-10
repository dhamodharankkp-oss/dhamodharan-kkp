# Concept Note: Reverse-Engineering, Design-Based Research (DBR), and Agentic Iteration in Functional Toy Design

> **Source Google Doc:** [View Live Concept Note in Google Docs](https://docs.google.com/document/d/1FRal6zgWQ94kOv7TnC984TP3e4rvzlZ8dmY8OLI076A/edit?tab=t.0)  
> **Document ID:** `1FRal6zgWQ94kOv7TnC984TP3e4rvzlZ8dmY8OLI076A`

---

## 1. Introduction & Background

Toy design is a sophisticated intersection of mechanical engineering, ergonomics, and developmental psychology. For a toy to successfully capture a user's attention, its structural architecture must trigger sustained **cognitive and tactile engagement**. While traditional product manufacturing relies on fragmented manual prototyping loops, this independent study introduces a rigorous **Design-Based Research (DBR)** and **Action Research** framework to systematically compress the production timeline.

By executing a structured, iterative cycle of prototyping, testing, and refining, this project seeks to dismantle successful toy mechanics, isolating the exact design tolerances, material properties, and sensory feedback loops that drive play value. To manage the massive data streams generated during product teardowns, structural testing, and user feedback logs, the project integrates [Google Antigravity](https://codelabs.developers.google.com/getting-started-google-antigravity), an agentic development and research platform. Operating within the Antigravity IDE, multi-agent computational pipelines will be deployed to process unstructured qualitative logs, automate parametric 3D modeling edits, and mathematically optimize the new toy design for peak interactive engagement.

---

## 2. Research Objectives & Questions

The primary goal of this independent study is to evaluate how an AI-assisted, closed-loop design methodology influences the iteration and optimization of consumer products.

- **RQ1:** How can Design-Based Research (DBR) be systematically applied to the reverse-engineering and evolution of functional consumer toys?
- **RQ2:** To what extent does code-based CAD editing (OpenSCAD/Python) via Antigravity's natural language interface reduce technical friction during the design modification phase?
- **RQ3:** What measurable shifts occur in user engagement and structural durability when comparing the reverse-engineered baseline toy to the newly engineered artifact?

---

## 3. Methodological Framework (The DBR Cycle)

This project utilizes a **Design-Based Research (DBR)** methodology executed across a multi-phase, recursive engineering cycle. The process follows a classic **ADDIE** (Analysis, Design, Development, Implementation, Evaluation) alignment, moving from physical deconstruction to automated digital synthesis within the Antigravity workspace:

```
                 [ PHASE 1: REVERSE-ENGINEERING ]
         Dismantling existing toys, mapping internal mechanics, 
        measuring clearances, and cataloging material properties.
                                │
                                ▼
                 [ PHASE 2: FEEDBACK COLLECTION ]
        Conducting hands-on user testing sessions and compiling 
      unstructured play logs, friction points, and behavioral data.
                                │
                                ▼
                 [ PHASE 3: AGENTIC DBR ITERATION ]
      Feeding text logs and CAD repositories into Google Antigravity.
    Multi-agent pipelines automatically modify, validate, and output 
       the refined 3D model files based on real-world test data.
```

---

## 4. Data Collection & Analytical Approach with Antigravity

To ensure experimental rigor, data will be collected, managed, and analyzed across three distinct layers of the DBR loop using the platform's multi-agent data orchestration:

- **The Mechanical & Geometric Layer (Teardown):** Physical dimensions, gear ratios, spring tensions, or snap-fit clearances from the teardown phase will be formatted into structured repositories. Antigravity will run local validation scripts to verify the mathematical feasibility of these dimensions before translating them into initial digital models.
- **The User Feedback Layer (Qualitative Synthesis):** Raw observation notes, usability forms, and user play transcripts (e.g., *"the latch is too stiff," "the spinning mechanism loses momentum"*) will be fed into Antigravity’s multi-agent pipelines. Utilizing the **Teamwork framework**, parallel sub-agents will parse this unstructured data, categorize the physical points of failure, and transform them into **validated knowledge graphs** linking user complaints directly to specific geometric parts.
- **The Artifact Evolution Layer (Autonomous Iteration):** Instead of manually rebuilding 3D models in traditional visual software, natural language prompts will drive structural changes. For instance, you will prompt the agent: *"Based on the user play logs showing structural weakness in the hinge, modify the OpenSCAD code to increase the wall thickness by 1.5mm and add a reinforcing fillet."* Antigravity will coordinate a **two-agent verification loop**: *Agent A (The CAD Modifier)* writes the script adjustments, while *Agent B (The Engineering Critic)* reviews the proposed changes to ensure they comply with physical manufacturing constraints (e.g., checking for unprintable overhangs or excess support material) before exporting the final **Artifact**.

---

## 5. Significance of the Research

This study provides a definitive blueprint for how independent product developers can execute rigorous, data-driven design cycles without the backing of a large corporate R&D department. By offloading complex data aggregation, parallel qualitative analysis, and repetitive CAD coding adjustments to **Google Antigravity**, a solo researcher can systematically reverse-engineer, analyze, and build highly engaging physical products with corporate-level precision.
