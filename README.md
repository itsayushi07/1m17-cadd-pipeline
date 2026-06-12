<div align="center">

# 🧬 1M17 • AI-Assisted Drug Discovery Pipeline

### Structure-Based Computational Analysis of the EGFR Kinase Domain

<img src="./figures/week1/full_protein.png" width="100%">

<br>

![Computational Biology](https://img.shields.io/badge/Computational_Biology-Research-blueviolet?style=for-the-badge)
![Structural Bioinformatics](https://img.shields.io/badge/Structural_Bioinformatics-EGFR-success?style=for-the-badge)
![Drug Discovery](https://img.shields.io/badge/Drug_Discovery-CADD-orange?style=for-the-badge)
![AlphaFold3](https://img.shields.io/badge/AlphaFold3-AI_Modeling-purple?style=for-the-badge)
![PyRx](https://img.shields.io/badge/PyRx-Molecular_Docking-red?style=for-the-badge)

<br>

### Computational Biology × Structural Bioinformatics × Artificial Intelligence

### 🎯 Target: EGFR Kinase Domain

### 📍 PDB ID: 1M17

</div>

---

# 🌟 Project Snapshot

<div align="center">

| 🧬 Target | ⚡ Best Binder | 📊 RMSD | 🤖 Validation |
|-----------|-----------|-----------|-----------|
| EGFR Kinase Domain | Lapatinib | 0.484 Å | AlphaFold3 |

</div>

---

# 🌍 Overview

This repository presents a complete **Computer-Aided Drug Design (CADD)** workflow targeting the **Epidermal Growth Factor Receptor (EGFR) Kinase Domain** using the experimentally resolved protein structure **1M17**.

The project integrates:

- 🎯 Binding Site Prediction
- 🧬 Protein Preparation
- 💊 Drug-Likeness Screening
- ⚡ Molecular Docking
- 🔗 Protein–Ligand Interaction Analysis
- 📊 ADMET Profiling
- 🤖 AI-Based Structure Validation

to evaluate clinically relevant EGFR inhibitors through a modern structure-based drug discovery workflow.

---

# 🦠 Protein Target

<div align="center">

<img src="./figures/week1/full_protein.png" width="900">

### Experimental Structure of EGFR Kinase Domain (PDB: 1M17)

</div>

| Property | Value |
|-----------|-----------|
| Protein | Epidermal Growth Factor Receptor (EGFR) |
| PDB ID | 1M17 |
| Resolution | 2.60 Å |
| Method | X-Ray Crystallography |
| Co-Crystallized Ligand | Erlotinib |
| Disease Relevance | Cancer Progression |
| Target Class | Receptor Tyrosine Kinase |

---

# 🎯 Binding Pocket Analysis

<div align="center">

<img src="./figures/week1/binding_pocket.png" width="900">

</div>

<br>

<div align="center">

<img src="./figures/week1/binding_residues.png" width="900">

</div>

### Key Active Site Residues

```text
LEU694
VAL702
ALA719
ILE720
LYS721
GLU738
MET742
CYS751
LEU764
THR766
GLN767
LEU768
MET769
GLY772
LEU820
THR830
ASP831
```

> The predicted pocket overlapped directly with the co-crystallized Erlotinib binding site, confirming biological relevance.

---

# 🧬 Protein Preparation

<div align="center">

<table>
<tr>

<td align="center">

<img src="./figures/week1/before_preparation.png" width="450">

### Before Preparation

</td>

<td align="center">

<img src="./figures/week1/after_preparation.png" width="450">

### After Preparation

</td>

</tr>
</table>

</div>

### Preparation Workflow

```diff
+ Chain A Selection
+ Water Removal
+ Heteroatom Removal
+ Hydrogen Addition
+ Dock Prep Optimization
```

Output:

```text
1M17_prepared.pdb
```

---

# 💊 Drug-Likeness Screening

<div align="center">

<img src="./figures/week2/swissadme.png" width="950">

</div>

### Evaluated Compounds

| Compound | Drug-Likeness |
|-----------|-----------|
| Erlotinib | ✅ Pass |
| Gefitinib | ✅ Pass |
| Lapatinib | ⚠ High Molecular Weight |

### Key Observation

Erlotinib and Gefitinib demonstrated favorable oral drug-like characteristics, while Lapatinib exceeded the recommended molecular weight threshold.

---

# ⚡ Molecular Docking

### AutoDock Vina via PyRx

| Rank | Compound | Binding Affinity (kcal/mol) |
|--------|--------|--------|
| 🥇 | Lapatinib | **-11.6** |
| 🥈 | Gefitinib | -8.6 |
| 🥉 | Erlotinib | -8.3 |

<div align="center">

## 🏆 Best Docking Candidate

# Lapatinib

**Binding Affinity: −11.6 kcal/mol**

</div>

---

# 🔗 Protein–Ligand Interaction Analysis

## Erlotinib

<div align="center">

<img src="./figures/week2/erlotinib_2d_interaction..jpg" width="850">

</div>

---

## Gefitinib

<div align="center">

<img src="./figures/week2/gefitinib_2d_interaction.jpg" width="850">

</div>

---

## Lapatinib

<div align="center">

<img src="./figures/week2/lapatinib_2d_interaction.jpg" width="850">

</div>

### Interaction Highlights

```diff
+ Hydrogen Bond Formation
+ Hydrophobic Contacts
+ Active Site Stabilization
+ Strong Molecular Complementarity
+ Favorable Binding Orientation
```

---

# 📊 ADMET Profiling

<div align="center">

<img src="./figures/week2/admet_result.png" width="950">

</div>

### Comparative Assessment

| Compound | Assessment |
|-----------|-----------|
| Erlotinib | ⭐ Most Balanced Profile |
| Gefitinib | ⚠ Elevated hERG Risk |
| Lapatinib | ⚠ Increased PPB & Metabolic Risk |

### Evaluated Categories

```text
Absorption
Distribution
Metabolism
Excretion
Toxicity
```

---

# 🤖 AlphaFold3 Validation

## Predicted Structure

<div align="center">

<img src="./figures/week3/alphafold_predicted.png" width="900">

</div>

---

## Experimental vs Predicted Structural Alignment

<div align="center">

<img src="./figures/week3/aligned_overlay.png" width="950">

</div>

---

### Structural Metrics

| Metric | Result |
|-----------|-----------|
| RMSD | 0.484 Å |
| Atoms Aligned | 1831 |
| Structural Agreement | Excellent |
| Confidence | High |

### Interpretation

The AlphaFold3-predicted model demonstrated excellent agreement with the experimentally resolved EGFR structure, supporting the reliability of AI-assisted protein modelling.

---

# 🏆 Major Findings

```diff
+ EGFR selected as a clinically relevant oncology target
+ Binding site prediction matched experimental active site
+ Lapatinib achieved strongest docking affinity
+ Erlotinib demonstrated optimal ADMET balance
+ AlphaFold3 reproduced experimental architecture
+ RMSD = 0.484 Å
+ Strong support for AI-assisted drug discovery workflows
```

---

# 📂 Repository Structure

```text
1m17-cadd-pipeline/

├── README.md
├── LICENSE
├── .gitignore
│
├── data/
├── docking/
├── structures/
│
├── figures/
│   ├── week1/
│   ├── week2/
│   └── week3/
│
├── results/
└── docs/
```

---

# 🛠 Technology Stack

| Category | Tool |
|-----------|-----------|
| Protein Visualization | PyMOL |
| Protein Preparation | UCSF Chimera |
| Binding Site Prediction | DoGSiteScorer |
| Drug-Likeness Screening | SwissADME |
| Molecular Docking | PyRx (AutoDock Vina) |
| Interaction Analysis | BIOVIA Discovery Studio |
| ADMET Prediction | ADMETlab 3.0 |
| AI Structure Prediction | AlphaFold3 |

---

# 🌟 Scientific Significance

EGFR is one of the most clinically important receptor tyrosine kinases involved in cancer progression and targeted therapy development.

This project demonstrates the integration of:

- Computational Biology
- Structural Bioinformatics
- Molecular Docking
- Pharmacokinetic Profiling
- Artificial Intelligence

within a unified structure-based drug discovery workflow.

---

# 👩‍🔬 Author

## Ayushi

**Final Year B.Sc. Chemistry**

Computational Biology • Bioinformatics • Structural Bioinformatics • CADD

### Research Interests

🧬 Computational Biology

💊 Drug Discovery

🤖 AI in Life Sciences

🔬 Structural Bioinformatics

---

<div align="center">

# ⭐ Star this repository if you found it useful

### Computational Biology × Structural Bioinformatics × Drug Discovery × AI

</div>
