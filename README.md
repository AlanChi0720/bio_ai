# 🧬 bio_ai — Bioinformatics & Bio-AI Self-Study

A structured self-learning curriculum exploring AI applications in biology, progressing from classical ML on gene expression data to deep learning in genomics, structural biology, cheminformatics, and single-cell transcriptomics.

**Background:** Life sciences + Python/pandas. New to ML and bio-AI.  
**Environment:** Google Colab

---

## 📍 Roadmap

| Phase | Focus | Status |
|-------|-------|--------|
| **Phase 1** | Visualization + ML fundamentals on real gene expression data | ✅ Complete |
| **Phase 2** | 4 mini-projects across different bio-AI domains | 🔄 In progress |
| **Phase 3** | Deep dive into one Phase 2 domain | 🔜 Planned |
| **Phase 4** | Concrete project in the chosen domain | 🔜 Planned |

---

## Phase 1 — Gene Expression ML

**Dataset:** GSE2034 Breast Cancer (GEO) — ~286 samples, ~22,000 genes  
**Goal:** Predict bone relapse from gene expression profiles

**Key tools:** `GEOparse` · `seaborn` · `scikit-learn`

**Topics covered:**
- Loading and parsing GEO Series Matrix files
- Extracting sample metadata from `characteristics_ch1` fields
- Dimensionality reduction (PCA)
- Classification (e.g., predicting relapse: 1=yes, 0=no)
- Visualization of high-dimensional gene expression data

---

## Phase 2 — Bio-AI Mini Projects

### A · DNA k-mer Classification
**Dataset:** UCI E. coli promoter dataset  
**Goal:** Classify DNA sequences as promoter or non-promoter using k-mer frequency features

**Topics:** k-mer encoding, sequence featurization, classification

---

### B · Protein Embedding + PCA
**Model:** ESM-2 (Meta's protein language model)  
**Goal:** Embed kinase vs. opsin protein sequences and visualize clustering in embedding space

**Topics:** Protein language models, sequence embeddings, PCA visualization, representation learning

---

### C · Molecular Solubility Prediction
**Dataset:** Delaney ESOL dataset  
**Goal:** Predict aqueous solubility (logS) from molecular SMILES strings

**Key tools:** `RDKit` · `scikit-learn` (Random Forest)

**Topics:** SMILES encoding, Morgan fingerprints (ECFP), molecular descriptors, Lipinski's Rule of Five, regression (RMSE, R²)

> ⚠️ **Note:** Use `rdkit` (not the deprecated `rdkit-pypi`) when installing in Colab.

---

### D · Single-Cell RNA-seq Clustering
**Dataset:** PBMC3k (10x Genomics)  
**Goal:** Cluster peripheral blood mononuclear cells and annotate cell types

**Key tools:** `scanpy` · Leiden algorithm · UMAP

**Topics:** scRNA-seq preprocessing, normalization, highly variable genes, PCA, neighbor graph construction, UMAP, Leiden clustering, marker gene annotation

> ⚠️ **Note:** May encounter pandas version conflicts in Colab — see notebook for fix.

---

## 🛠 Environment Setup

All notebooks run on **Google Colab**. Key dependencies by project:

```
# Phase 1
geoparse seaborn scikit-learn

# Phase 2A
scikit-learn

# Phase 2B
fair-esm torch

# Phase 2C
rdkit scikit-learn

# Phase 2D
scanpy leidenalg
```

---

## 📂 Repo Structure

```
bio_ai/
├── phase1_gene_expression/
│   └── GSE2034_breast_cancer.ipynb
├── phase2_mini_projects/
│   ├── 2A_dna_kmer_classification.ipynb
│   ├── 2B_protein_embedding_pca.ipynb
│   ├── 2C_molecular_solubility.ipynb
│   └── 2D_scrna_pbmc_clustering.ipynb
└── README.md
```

---

## 📚 Key References

- Luecken & Theis (2020) — *Current best practices in single-cell RNA-seq analysis*
- Delaney (2004) — ESOL solubility dataset
- Lin et al. (2023) — ESM-2 protein language model
- 10x Genomics PBMC3k dataset

---

*This is an active learning repo — structure and content will evolve as the curriculum progresses into Phase 3 and 4.*
