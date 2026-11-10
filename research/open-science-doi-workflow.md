# Open Science, GitBook & DOI Archival Workflow for 3D-Printed Toy Design (DBR)

This document establishes the end-to-end scholarly dissemination, version-control, and archival pipeline for the research project: **"Reverse-Engineering, Design-Based Research (DBR), and Agentic Iteration in Functional Toy Design"**. 

It transitions the project from an internal engineering repository into a **citable, peer-recognized, and reproducible Open Science contribution**.

---

## 1. Executive Architecture & Systems Flow

The publication workflow integrates five decoupled layers to ensure living flexibility during design cycles alongside permanent, immutable academic record-keeping:

```
[1. Primary Engineering & Experimental Assets]
  ├── Parametric CAD Scripts (.scad)
  ├── Production Mesh Binaries (.stl) & Slicer Profiles (.3mf / .gcode)
  ├── Classroom Ergonomic & Usability Play Logs
  └── Workshop Environmental Telemetry (UFP / VOC Sensors)
                           │
                           ▼
[2. GitHub Version-Controlled Repository] 
  ├── Git branch workflows & pull requests
  ├── Automated GitHub Releases (Semantic Versioning: v1.0.0)
  └── CITATION.cff metadata manifest
         │                                    │
         ▼ (Live Two-Way Sync)                ▼ (Automated Webhook)
[3. GitBook Living Monograph]          [4. Zenodo Archival Repository]
  ├── Interactive CAD/Model Viewer       ├── Immutable Snapshot Retention
  ├── Living DBR Case Studies            ├── DataCite DOI Minting
  └── Educator & Maker Interface         └── Version vs Concept DOI Tracking
                                                      │
                                                      ▼
                                       [5. ORCID Researcher Registry]
                                         ├── Persistent Author Attribution
                                         └── Works Indexing (Open Hardware / Monograph)
```

---

## 2. Layer 1: Primary Research Inputs & Hardware Artifacts

Unlike observational citizen science, Design-Based Research in additive manufacturing is grounded in **computational, physical, and human-interaction datasets**. All research inputs must be structured with explicit licensing, version tags, and provenance:

### 2.1 Computational & Geometric Data
* **Parametric Code:** Explicit mathematical source files (`cad/numicon_base.scad`) governed by dimensional variables (`pitch = 25.0 mm`, `hole_clearance = 0.25 mm`, `corner_radius = 2.5 mm`).
* **Binary Meshes:** Production-ready STLs (`cad/numicon_1.stl` through `cad/numicon_10.stl`) pre-tested for non-manifold boundaries and manifold zero-error geometry.
* **Manufacturing Toolchains:** Standardized slicing profiles (e.g., 0.24 mm layer height, 4 perimeter walls / 1.6 mm shell, 8%–10% gyroid infill, 8.0 mm Z-height).
* **Licensing:** Standardized under **CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S)** or **CC-BY-SA 4.0**, guaranteeing derivative open-source access.

### 2.2 Empirical Play & Usability Logs (Phase 2 DBR)
* **Qualitative Field Data:** Structured rubrics capturing tactile grip friction, peg insertion resistance, drop-test fracture logs, and classroom engagement observations across diverse learner cohorts.
* **Ethics & Consent:** Full de-identification of student participants in compliance with institutional review board (IRB) and human subject protection standards.

### 2.3 Environmental & Safety Telemetry
* Real-time air quality logs measuring Ultrafine Particles (UFP count < 20,000 particles/cm³) and Volatile Organic Compounds (VOCs) during multi-printer FDM fabrication runs, validating toxicological safety protocols.

---

## 3. Layer 2: GitBook as the Living Research Monograph

GitBook serves as the public-facing, interactive **Living Research Interface**. It allows educators, researchers, and makers to explore the evolution of the toys without wading through raw repository commits.

### 3.1 Monograph Structure (`SUMMARY.md`)
```markdown
# Summary

* [Front Matter & Executive Overview](README.md)
* [Methodological Framework](methodology.md)
  * [Design-Based Research (DBR) Cycles](dbr_cycles.md)
  * [Pedagogical Foundations (CDIO & EiE)](pedagogy.md)
* [Hardware Engineering & Manufacturing](hardware.md)
  * [Parametric OpenSCAD Architecture](openscad_architecture.md)
  * [High-Efficiency Shell Slicing Profiles](slicing_profiles.md)
  * [Workshop Safety & Emission Compliance](emission_control.md)
* [Empirical Case Studies](case_studies.md)
  * [Numicon Math Toy Redesign (Shapes 1–10)](numicon_case_study.md)
  * [Classroom Usability & Iteration Logs](classroom_logs.md)
* [Agentic CAD & Prompt Engineering](agentic_cad.md)
  * [Prompt Matrices & Multi-Agent Loops](prompt_matrices.md)
  * [AI & Algorithmic Transparency Statement](ai_disclosure.md)
* [Citations & Archival Releases](citations.md)
```

### 3.2 Dynamic Embeds
* Embed interactive 3D WebGL STL previews directly within documentation pages for real-time model inspection in browser.
* Embed parametric parameter calculators for custom classroom peg clearances.

---

## 4. Layer 3: Version Control & Milestone Freezing via GitHub

Academic citation demands **fixed, unalterable milestones**. While GitBook evolves continuously, research claims must reference a static, frozen state of the code and findings.

### 4.1 Branching & Semantic Release Strategy
* Main development occurs on feature branches (`feature/odd-shape-geometry`, `feature/anti-slip-pockets`).
* Formal DBR cycles trigger semantic version releases:
  * `v1.0.0-dbr1` : Initial baseline reverse-engineered set (Numicon 1–10) with initial classroom field testing.
  * `v1.1.0-dbr2` : Agentic optimization iteration (chamfered lead-ins, 0.25 mm dynamic clearance, Braille counting rings).
  * `v2.0.0-final`: Multi-school validated production set with toxicological compliance verification.

### 4.2 Citation Metadata Manifest (`CITATION.cff`)
Place a `CITATION.cff` file in the root of the repository:
```yaml
cff-version: 1.2.0
message: "If you use this research, software, or 3D models, please cite it as below."
authors:
  - family-names: "Dhamodharan"
    given-names: "H."
    orcid: "https://orcid.org/0000-0000-0000-0000" # Replace with valid ORCID
    affiliation: "Payir Trust"
title: "Reverse-Engineering, Design-Based Research (DBR), and Agentic Iteration in Functional Toy Design: Open-Source Numicon Case Study"
version: 1.0.0
doi: 10.5281/zenodo.xxxxxx # Updated upon first release
date-released: 2026-10-22
url: "https://github.com/your-org/numicon-dbr-research"
keywords:
  - "3D Printing"
  - "OpenSCAD"
  - "Design-Based Research"
  - "Educational Technology"
  - "Mathematical Manipulatives"
  - "Open Hardware"
license: "CERN-OHL-S-2.0"
```

---

## 5. Layer 4: Zenodo Archival & DataCite DOI Minting

Zenodo (operated by CERN) serves as the persistent archival core, guaranteeing minimum 20-year data availability and indexing in global scientific catalogs.

### 5.1 Automated Webhook Configuration
1. Log in to [zenodo.org](https://zenodo.org/) using your ORCID or GitHub account.
2. Under **Account → GitHub**, enable the toggle switch for the research repository.
3. Once enabled, publishing a **GitHub Release** automatically triggers Zenodo to:
   * Archive a `.zip` snapshot of all code, STLs, slicer configurations, and markdown logs.
   * Generate a persistent **DataCite DOI**.

### 5.2 Concept DOI vs. Version DOI
* **Concept DOI (e.g., `10.5281/zenodo.1234560`):** An umbrella identifier representing the entire living project across all iterations. Resolves to the latest release. Recommended for inclusion on the GitBook landing page.
* **Version DOI (e.g., `10.5281/zenodo.1234561`):** A granular identifier permanently bound to the exact code and paper state of a single DBR release (e.g., `v1.0.0`). Mandatory for formal journal and conference citations.

### 5.3 Zenodo Deposit Metadata Template
* **Upload Type:** `Publication` → `Report` or `Software` (or `Open Hardware`).
* **Title:** Reverse-Engineering, Design-Based Research, and Agentic Iteration in Functional Toy Design (Release vX.X).
* **Communities:** Add to open communities such as *Open Educational Resources*, *Open Hardware*, and *Additive Manufacturing*.
* **Related Identifiers:**
  * `IsDocumentedBy` → GitBook Live URL.
  * `IsSupplementTo` → Target journal preprint or Google Docs Master Document.

---

## 6. Layer 5: Author Attribution & ORCID Integration

ORCID provides persistent, non-proprietary author identity, preventing citation ambiguity and ensuring non-traditional outputs receive equal tenure/grant credit:

1. **Zenodo → ORCID Auto-Sync:**
   * Within Zenodo account settings, authorize DataCite to export minted works automatically to your ORCID profile.
   * Every tagged DBR release appears automatically under your **ORCID Works** section with full DataCite metadata.
2. **ORCID Profile Categorization:**
   * **Works Section:** Lists Zenodo DOIs categorized as *Software* (OpenSCAD codebase) and *Report* (living monograph snapshots).
   * **Websites & Social Links:** Add the live GitBook URL under the description: *"Living Research Monograph: AI-Assisted Functional Toy Design"*.
   * **Other IDs:** Link GitHub developer profile.

---

## 7. Methodological AI & Agentic Transparency Protocol

In accordance with **COPE (Committee on Publication Ethics)** and major scientific publisher guidelines (*Nature*, *Elsevier*), artificial intelligence and autonomous agents cannot hold authorship. However, their agentic integration in this project represents a core methodological contribution.

### 7.1 Formal AI Disclosure Statement
Incorporate the following standardized disclosure into the monograph front matter and academic submissions:

> ### **Methodological Transparency & AI Tool Disclosure**
> 
> *"This research incorporates generative AI models and autonomous agentic workflows (specifically Google Antigravity and Large Language Models) as computational research and engineering tools. 
> 
> * **Computational CAD Generation:** AI agents were utilized to assist in authoring, debugging, and refactoring parametric OpenSCAD scripts (`cad/numicon_base.scad`), including resolving 2D boolean polygon clipper bottlenecks and CGAL execution halts.
> * **Literature & Framework Synthesis:** Generative RAG tools were employed to accelerate multi-source literature cross-referencing across 33 papers in spatial cognition, additive manufacturing emissions, and engineering design pedagogy.
> * **Human Agency & Accountability:** The author(s) designed all overarching experimental protocols, established all mathematical clearance thresholds (e.g., 0.25 mm peg tolerance, 8 mm shell slicing), directly supervised physical fabrication and FDM testing, and conducted all classroom qualitative analyses. The human author(s) assume complete responsibility and accountability for the accuracy, geometric integrity, safety standards, and pedagogical validity of all published outputs."*

### 7.2 Reproducibility Prompt Matrix
To ensure scientific reproducibility, all prompts used to drive the multi-agent CAD loops are indexed in the repository under [numicon_case_study.md](numicon_case_study.md), including system roles, geometric constraints, and evaluation critics.

---

## 8. Academic Citation Standards & Formatting

Once the pipeline is active, external scholars and educators can cite your work across diverse formats:

### 8.1 APA 7th Edition
> Dhamodharan, H. (2026). *Reverse-Engineering, Design-Based Research (DBR), and Agentic Iteration in Functional Toy Design: Numicon Parametric Architecture* (Version 1.0.0) [Computer software and design monograph]. Zenodo. https://doi.org/10.5281/zenodo.xxxxxx

### 8.2 BibTeX (for LaTeX & Academic Papers)
```bibtex
@software{dhamodharan_toy_dbr_2026,
  author       = {Dhamodharan, H.},
  title        = {{Reverse-Engineering, Design-Based Research (DBR), 
                   and Agentic Iteration in Functional Toy Design}},
  month        = oct,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.xxxxxx},
  url          = {https://doi.org/10.5281/zenodo.xxxxxx}
}
```

---

## 9. Implementation Checklist & Next Milestones

| Step | Action Item | Tool / Platform | Target Deliverable |
| :--- | :--- | :--- | :--- |
| **1** | Establish public/open repository for `d:\DD Research` assets | GitHub | `numicon-dbr-research` repo with `cad/` and `.md` docs |
| **2** | Add `CITATION.cff` and `LICENSE` (CERN-OHL-S / CC-BY-SA) | Git / Local Editor | Root citation metadata manifest |
| **3** | Initialize GitBook workspace connected to GitHub repository | GitBook | Live, responsive documentation site |
| **4** | Activate Zenodo GitHub webhook | Zenodo → Settings | Automated DOI pipeline on release tags |
| **5** | Draft initial tagged release (`v1.0.0-dbr1`) | GitHub Releases | Minted DataCite DOI for baseline Numicon set |
| **6** | Connect Zenodo to ORCID account | ORCID → DataCite | Automated entry in scholarly Works record |
| **7** | Integrate Concept DOI badge into GitBook and README | Markdown / SVG | Live clickable academic attribution badge |
