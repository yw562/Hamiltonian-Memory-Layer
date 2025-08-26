# Roadmap: 10-Week Action Plan for Hamiltonian Memory Layer (HML)

This roadmap outlines the **minimum viable path** to produce a working prototype, experimental results, and a workshop-ready paper.  
Each week has a clear **goal** and **deliverable**.

---

## 📅 Week 1–2: Baseline Setup
- **Goal**: Build training/evaluation pipeline for long-context baselines (Mamba, Hyena, RetNet).  
- **Tasks**:
  - Reproduce one baseline (e.g., Mamba) on a small Long Range Arena (LRA) task.  
  - Set up experiment scripts (`experiments/run_lra.sh`).  
  - Verify GPU runtime + logging.  
- **Deliverables**:
  - Working baseline code in `src/`.  
  - First plots in `results/` (baseline accuracy vs. sequence length).  

---

## 📅 Week 3–4: HML Prototype
- **Goal**: Implement first version of Hamiltonian Memory Layer.  
- **Tasks**:
  - Define HML state representation \((q, p)\).  
  - Implement symplectic update (Leapfrog integrator).  
  - Add simple read/write mechanism.  
  - Integrate into baseline pipeline.  
- **Deliverables**:
  - `src/hml_layer.py` (prototype).  
  - Toy experiment: copy task / synthetic sequence.  
  - Plot: HML vs. baseline on toy data.  

---

## 📅 Week 5–6: Synthetic Experiments
- **Goal**: Test HML on controlled long-range tasks.  
- **Tasks**:
  - Run Needle-in-a-Haystack retrieval.  
  - Run arithmetic/sequence prediction.  
  - Compare gradient stability (norm vs. length).  
- **Deliverables**:
  - Plots: retrieval accuracy vs. context length.  
  - Plots: gradient norm stability.  
  - `results/synthetic/` folder with logs & figures.  

---

## 📅 Week 7: Benchmark Evaluation (LRA)
- **Goal**: Evaluate HML on Long Range Arena.  
- **Tasks**:
  - Train on 1–2 LRA tasks (ListOps, Text).  
  - Compare against baselines under same parameter budget.  
- **Deliverables**:
  - Accuracy/F1 tables.  
  - Plot: performance vs. sequence length.  

---

## 📅 Week 8: Language Modeling (PG-19 subset)
- **Goal**: Demonstrate HML on a real long-text dataset.  
- **Tasks**:
  - Train HML + baseline on PG-19 small split.  
  - Measure perplexity vs. context length.  
- **Deliverables**:
  - `results/pg19/` with perplexity curves.  
  - Early draft figure for paper.  

---

## 📅 Week 9: Write-Up
- **Goal**: Draft workshop-style paper (4–6 pages).  
- **Tasks**:
  - Write intro + method + results.  
  - Generate clean figures.  
  - Add arXiv-ready LaTeX template.  
- **Deliverables**:
  - `paper/` directory with draft.  
  - Updated `proposal.md` with results summary.  

---

## 📅 Week 10: Polish & Release
- **Goal**: Finalize repo for public release.  
- **Tasks**:
  - Clean code, add comments.  
  - Update README with results.  
  - Upload preprint to arXiv.  
  - Submit to NeurIPS/ICLR Workshop.  
- **Deliverables**:
  - Public GitHub repo (with results & paper draft).  
  - ArXiv preprint link.  
  - Workshop submission confirmation.  

---

# ✅ Success Criteria
- At least one **plot** showing HML has comparable or better performance vs. baselines on long-context tasks.  
- A complete **paper draft** (arXiv/workshop).  
- An **open-source repo** with proposal, roadmap, code, and results.  
