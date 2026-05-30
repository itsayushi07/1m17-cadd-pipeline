# 1m17-cadd-pipeline

<div align="center">

# 1M17 CADD Pipeline

### AI-Assisted Structure-Based Drug Discovery of EGFR Kinase Domain (1M17)

Structure-based computational drug discovery workflow integrating **PyMOL**, **UCSF Chimera**, **DoGSiteScorer**, **SwissADME**, **PyRx**, **Discovery Studio**, **ADMETlab 3.0**, and **AlphaFold3**.

![Field](https://img.shields.io/badge/Field-Computational%20Biology-black)
![Workflow](https://img.shields.io/badge/Workflow-CADD-black)
![Protein](https://img.shields.io/badge/Protein-1M17-black)
![Status](https://img.shields.io/badge/Status-Completed-success)

</div>

---

## Overview

This repository presents a **structure-based Computer-Aided Drug Design (CADD) workflow** performed on the **Epidermal Growth Factor Receptor (EGFR) kinase domain** using the experimentally validated protein structure **1M17**.

The project integrates **protein target evaluation**, **binding site analysis**, **protein preparation**, **drug-likeness screening**, **molecular docking**, **ADMET profiling**, and **AI-based structure validation** using **AlphaFold3**.

The objective was to evaluate clinically relevant **EGFR inhibitors** computationally while exploring protein–ligand interactions, pharmacological properties, and structural reliability through modern computational biology workflows.

---

# Protein Information

| Parameter                  | Value                                                 |
| -------------------------- | ----------------------------------------------------- |
| **Protein Name**           | Epidermal Growth Factor Receptor (EGFR) kinase domain |
| **PDB ID**                 | `1M17`                                                |
| **Experimental Method**    | X-Ray Crystallography                                 |
| **Resolution**             | `2.60 Å`                                              |
| **Co-crystallized Ligand** | Erlotinib                                             |
| **Target Relevance**       | Cancer-associated receptor tyrosine kinase            |

---

## Research Objective

To computationally evaluate **EGFR inhibitors** against the **EGFR kinase domain (1M17)** through a complete **structure-based drug discovery workflow**, integrating:

* Protein target selection
* Binding site identification
* Protein preparation
* Drug-likeness screening
* Molecular docking
* ADMET profiling
* AI-based structural validation

---

# Workflow

## 1. Protein Target Selection & Structure Evaluation

The **EGFR kinase domain (1M17)** was selected due to its biological importance in **cell growth regulation and cancer progression**.

The structure was experimentally resolved through **X-ray crystallography** at a resolution of **2.60 Å**, providing reliable structural quality for computational analysis.

The presence of the co-crystallized inhibitor **Erlotinib** enabled accurate identification and validation of the active binding pocket.

<p align="center">
  <img src="figures/week1/full_protein.png" width="700">
</p>

---

## 2. Binding Site Identification

Binding pocket prediction was performed using **DoGSiteScorer**, identifying **Pocket P_1** as the highest-ranked biologically relevant binding region.

### Key Binding Residues

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

The predicted pocket overlapped directly with the location of **Erlotinib** in the crystal structure, confirming biological relevance and active-site accuracy.

<p align="center">
  <img src="figures/week1/binding_pocket.png" width="700">
</p>

---

## 3. Protein Preparation

Protein preparation was carried out in **UCSF Chimera** to generate a docking-ready protein structure.

### Preparation Workflow

* Selection of **Chain A**
* Removal of water molecules (**HOH**)
* Removal of unnecessary ligands and heteroatoms
* Hydrogen addition
* Charge assignment through **Dock Prep**

### Output File

```text
1M17_prepared.pdb
```

The cleaned structure improved structural consistency and docking reliability.

<p align="center">
  <img src="figures/week1/before_preparation.png" width="48%">
  <img src="figures/week1/after_preparation.png" width="48%">
</p>

---

## 4. Drug-Likeness Screening

Drug-likeness analysis was performed using **SwissADME** based on **Lipinski’s Rule of Five**.

### Evaluated Compounds

| Compound  | Drug-Like             |
| --------- | --------------------- |
| Erlotinib | Yes                   |
| Gefitinib | Yes                   |
| Lapatinib | Partial (MW > 500 Da) |

### Key Observation

Erlotinib and Gefitinib demonstrated favorable oral drug-like characteristics, while Lapatinib exceeded the recommended molecular weight threshold.

<p align="center">
  <img src="figures/week2/swissadme.png" width="700">
</p>

---

## 5. Molecular Docking

Molecular docking was performed using **PyRx (AutoDock Vina)** to evaluate predicted ligand-binding affinity toward the EGFR active site.

### Docking Scores

| Compound      | Binding Affinity (kcal/mol) |
| ------------- | --------------------------- |
| **Lapatinib** | **-11.6**                   |
| Gefitinib     | -8.6                        |
| Erlotinib     | -8.3                        |

### Key Finding

**Lapatinib** demonstrated the strongest predicted interaction with the EGFR kinase domain based on docking score and molecular interaction stability.

<p align="center">
  <img src="figures/week2/pyrx_docking.png" width="700">
</p>

---

## 6. Protein–Ligand Interaction Analysis

Interaction analysis was performed in **BIOVIA Discovery Studio** to evaluate hydrogen bonding and hydrophobic interactions within the active site.

Comparative interaction mapping suggested stronger intermolecular stabilization for **Lapatinib**, supporting its superior docking performance.

<p align="center">
  <img src="figures/week2/lapatinib_interaction.png" width="700">
</p>

---

## 7. ADMET Profiling

ADMET prediction was conducted using **ADMETlab 3.0** to assess pharmacokinetic and toxicity-related properties.

### Major Findings

* **Erlotinib** showed the most balanced overall ADMET profile.
* **Gefitinib** demonstrated elevated hERG inhibition risk.
* **Lapatinib** displayed strong plasma protein binding and increased metabolic interaction risk.

### Evaluated Properties

```text
Absorption
Distribution
Metabolism
Excretion
Toxicity
```

<p align="center">
  <img src="figures/week2/admet_results.png" width="700">
</p>

---

## 8. AlphaFold3 Structure Validation

AI-based structure prediction was performed using **AlphaFold3**, followed by structural alignment against the experimentally prepared protein structure in **PyMOL**.

### Structural Alignment Metrics

| Metric               | Result    |
| -------------------- | --------- |
| RMSD                 | `0.484 Å` |
| Atoms Aligned        | `1831`    |
| Structural Agreement | Excellent |

The AlphaFold3-predicted structure showed strong structural agreement with the experimentally resolved model, with only minor deviations observed in flexible regions.

<p align="center">
  <img src="figures/week3/aligned_overlay.png" width="700">
</p>

---

# Key Findings

* **1M17** was selected as a biologically relevant cancer-associated therapeutic target.
* Binding site prediction successfully matched the experimentally validated active site.
* **Lapatinib** showed the strongest docking affinity (**−11.6 kcal/mol**).
* **Erlotinib** demonstrated the most balanced ADMET profile.
* AlphaFold3 achieved **excellent structural agreement** with experimental data (**RMSD = 0.484 Å**).

---

# Repository Structure

```bash
1m17-cadd-pipeline/
│── README.md
│── LICENSE
│── .gitignore
│
├── data/
├── docking/
├── structures/
├── figures/
├── results/
└── docs/
```

---

# Tools & Technologies

| Category                | Tool                    |
| ----------------------- | ----------------------- |
| Protein Visualization   | PyMOL                   |
| Protein Preparation     | UCSF Chimera            |
| Binding Site Prediction | DoGSiteScorer           |
| Drug-Likeness Screening | SwissADME               |
| Molecular Docking       | PyRx (AutoDock Vina)    |
| Interaction Analysis    | BIOVIA Discovery Studio |
| ADMET Prediction        | ADMETlab 3.0            |
| AI Structure Prediction | AlphaFold3              |

---

## Scientific Relevance

**EGFR (Epidermal Growth Factor Receptor)** is a clinically important receptor tyrosine kinase implicated in cancer progression and targeted therapy development.

This project demonstrates the integration of **structural bioinformatics, molecular docking, pharmacokinetic profiling, and AI-assisted protein modelling** within a unified computational drug discovery pipeline.

---

## Author

**Ayushi**
Computational Biology • Bioinformatics • CADD

<div align="center">

### Computational Biology × Structural Bioinformatics × AI

</div>
