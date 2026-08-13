
# Therapeutically targetable pathways underlying the paracrine-mediated co-option of a weakly metastatic clone in an *in vitro* breast cancer model of inter-clonal cooperation

This repository contains the R code used for the transcriptomic analyses in the study above. Using an *in vitro* breast cancer model system, we characterized the signalling pathways activated in a weakly metastatic clone (MCF7) in response to the conditioned medium of a highly metastatic clone (MDA-MB-231), with the goal of identifying components that can be targeted with available drugs.

The code covers:

1. Global expression profiling (Venn diagrams, PCA, volcano plots) of DESeq2 output
2. Ligand–receptor (L–R) interaction analysis of TALKIEN output
3. Over-representation analysis (ORA) with g:Profiler, including hierarchical annotation and representative-term selection for GO, KEGG and Reactome
4. Gene Set Enrichment Analysis (GSEA) — ranked-list generation and result visualization
5. Gene Set Variation Analysis (GSVA) and EMT scoring


**Raw RNA-seq data:** NCBI BioProject **PRJNA1473975**

## Analysis Workflow

```text
RNA-seq data
    ↓
   PCA
    ↓
Gene expression & DEG analysis
    ↓
Venn / Volcano plots
    ↓
Ligand–receptor analysis
    ↓
dbEMT & PANTHER
    ↓
g:Profiler ORA
    ↓
GSVA – Hallmark EMT
    ↓
Biological interpretation
```

## Repository Structure

| Folder                                         | Analysis                                    |
| ---------------------------------------------- | ------------------------------------------- |
| `00_PCA`                                       | Principal component analysis                |
| `1.1_Venn expressed genes`                     | Expressed gene overlap                      |
| `1.2_Venn co-expressed genes`                  | Co-expressed gene overlap                   |
| `1.3_Venn co-expressed DEGs`                   | Co-expressed DEG overlap                    |
| `1.4_Volcano plot`                             | Differential expression visualization       |
| `2_Ligand-receptor...`                         | Ligand–receptor, dbEMT and PANTHER analyses |
| `3.1_ORA gProfiler`                            | Functional enrichment analysis              |
| `3.2_ORA gProfiler Post Processing and Graphs` | Enrichment processing and visualization     |
| `4_GSVA EMT hallmark plot and heatmap`         | GSVA and EMT visualization                  |

## Main Analyses

### PCA and Differential Expression

PCA was used to evaluate sample clustering and transcriptomic variation. Differential expression analyses were visualized using volcano plots, while Venn analyses were used to identify shared and condition-specific genes.

### Ligand–Receptor Analysis

Ligand–receptor interactions were investigated to identify potential mechanisms of **inter-clonal communication**. Candidate genes were further evaluated using **dbEMT** and **PANTHER**.

### Functional Enrichment

**g:Profiler ORA** was used to identify enriched biological processes and pathways associated with selected gene sets.

### GSVA and EMT

**GSVA** was used to estimate Hallmark EMT activity across samples, providing a pathway-level assessment complementary to individual-gene differential expression.

## Software

Main R packages and resources include:

* R
* ggplot2
* dplyr
* GSVA
* biomaRt
* msigdbr
* gprofiler2
* dbEMT
* PANTHER

## Reproducibility

Clone the repository:

```bash
git clone https://github.com/carol-carneiro/Transcriptomic-Analysis-of-Inter-Clonal-Cooperation-in-Breast-Cancer.git
```

Run the analyses following the folder order described above. Input-file paths and required packages are specified within the individual scripts.

## Data Availability

Raw sequencing data are available through **NCBI BioProject PRJNA1473975**.

## Author

**Caroline Carneiro**

[GitHub: @carol-carneiro](https://github.com/carol-carneiro)
