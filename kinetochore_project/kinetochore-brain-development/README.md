# Kinetochore Gene Expression Across Human Brain Development

**Author:** Sai Sasi Sekhar Kongala  
**MSc Brain Sciences, University of Glasgow (2024–2025)**  
**Project Type:** Independent Computational Research Project  

---

## Project Question

Do kinetochore proteins remain expressed in the post-mitotic 
human brain, suggesting cell-division-independent neuronal functions?

---

## Background

Kinetochore proteins are classically studied for their role in 
chromosome segregation during cell division. However, Cheerambathur 
et al. (2019) demonstrated that components of the NDC80 complex 
persist in post-mitotic neurons and regulate dendrite morphogenesis 
independently of cell division.

This project investigates whether human kinetochore genes show 
persistent expression across the human brain lifespan using publicly 
available developmental transcriptomics data.

---

## Data Source

**BrainSpan Atlas of the Developing Human Brain**  
Downloaded from: http://www.brainspan.org/static/download.html  
Dataset: RNA-Seq Gencode v10 summarized to genes
524 brain tissue samples
31 developmental stages (8 pcw → 40 years)
52,376 genes in the full dataset
5 major brain regions

> **Note:** Raw data files are not uploaded to this repository  
> due to file size. Please download directly from BrainSpan using  
> the link above. Three files are needed:  
> - expression_matrix.csv  
> - rows_metadata.csv  
> - columns_metadata.csv  

---

## Genes Analysed

11 kinetochore genes across 4 functional complexes:

| Complex | Genes |
|---|---|
| NDC80 Complex | NDC80, NUF2, SPC24, SPC25 |
| KNL1 Network | CASC5, BUB1, BUB1B, BUB3 |
| Spindle Assembly Checkpoint | MAD2L1 |
| Outer Kinetochore | CENPE, CENPF |

---

## Key Findings

All 11 genes showed significantly higher prenatal expression  
(p < 0.05, Mann-Whitney U test, all results p = 0.0).

Most striking result — fold change comparison:

| Gene | Fold Change | Interpretation |
|---|---|---|
| NDC80 | 45.49x | Strongly mitosis-dependent |
| CASC5 | 38.36x | Strongly mitosis-dependent |
| BUB1  | 31.22x | Strongly mitosis-dependent |
| MAD2L1 | 3.25x | Persists post-mitotically |
| BUB3  | 1.94x | Strongly persists post-mitotically |

**BUB3 and MAD2L1 showed the smallest fold changes, remaining  
substantially expressed in adult post-mitotic neurons — suggesting  
cell-division-independent functions directly relevant to the  
Cheerambathur lab's research programme.**

---

## Repository Structure
kinetochore-brain-development/
├── README.md
├── kinetochore_project.ipynb        ← full analysis notebook
├── figures/
│   ├── NDC80_trajectory.png
│   ├── all_genes.png
│   └── fold_change.png
└── results/
└── statistical_results.csv

---

## How to Reproduce

1. Download BrainSpan data from link above
2. Place all 3 CSV files in a folder called data/
3. Open analysis.ipynb in Jupyter Notebook
4. Update the file path in Cell 3 to match your folder
5. Run all cells in order

---

## Tools and Libraries
Python 3
Pandas      — data loading and manipulation
Matplotlib  — visualisation
Seaborn     — statistical plots
Scipy       — Mann-Whitney U statistical testing
Numpy       — numerical operations

---

## References

1. Cheerambathur et al. (2019). Kinetochore-associated proteins 
   promote dendrite morphogenesis. Current Biology, 29(21).

2. Miller et al. (2014). Transcriptional landscape of the prenatal 
   human brain. Nature, 508, 199–206.

3. Kang et al. (2011). Spatio-temporal transcriptome of the human 
   brain. Nature, 478, 483–489.

---

## Note on Reproducibility

All code is fully documented in kinetochore_project.ipynb with markdown  
explanations between each step. Every figure can be reproduced  
by following the steps above with the raw BrainSpan data.

