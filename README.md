# -Netflix-Case-Study-Agent-Based-Simulation-Causal-Inference


This project was created as a response to the Netflix Data Scientist (L4/5) – Product role. It combines **agent-based user modeling** and **causal graph inference** to explore how Live or Live-like content should be positioned to maximize engagement and retention.

---

## Problem Statement

How might different user personas interact with Live content if we promoted it more prominently on the homepage? Can we simulate this behavior without access to real user data?

---

##  Methodology

### 1. **Synthetic User Simulation**
- Constructed feature vectors for Netflix content using public metadata (genre, duration, rating).
- Defined agent profiles: `Binger`, `Event Seeker`, `Critic`, `Kids Friendly`.
- Simulated selections via ε-greedy choice strategies.

### 2. **Causal Graph Modeling (Do-Calculus)**
- Developed a DAG to model `Content → Selection → Retention` with confounding by `UserType`.
- Simulated causal inference using a synthetic dataset to demonstrate the **importance of backdoor adjustment**.
- Visualized the contrast between observational and adjusted inferences.

---

## Outputs

- Matplotlib bar plots showing top content selected by each synthetic agent.
- Causal DAG (drawn using `networkx`) representing confounding structure.
- Simulation comparing:
  - `P(Retention | ContentFeature)` vs.
  - `P(Retention | ContentFeature, UserType)` (backdoor-adjusted)

---

## Key Insights

- Live-like content (Reality TV, Docuseries, Stand-Up) is highly favored by "event-driven" users.
- Causal models reveal how user segmentation affects engagement — even without experiment logs.
- Agent-based simulations are a powerful prototyping tool before experimentation infrastructure exists.

---

## Project Goals

✅ Demonstrate product intuition under data constraints  
✅ Apply experimental design and causal reasoning  
✅ Show analytical creativity — physics meets product strategy


