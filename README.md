# BMI 6313: Scientific Writing in Healthcare

This repository contains details about the **bioinformatics project performed using [iDEP](http://bioinformatics.sdstate.edu/idep/)** as part of the BMI 6313: Scientific Writing in Healthcare course. The study, titled **"Long-term IQOS exposure modulates apoptosis and cytokine signaling pathways: Genomic insights from mouse lungs"**, analyzed the genomic effects of IQOS exposure on mouse lungs using public microarray dataset obtained from NCBI GEO.

---
# Long-term IQOS Exposure Modulates Apoptosis and Cytokine Signaling Pathways: Genomic Insights from Mouse Lungs

## Project Overview

### 1. Data Retrieval
The mouse microarray dataset with the the accession ID **GSE161869** was accessed through the **National Center for Biotechnology Information Gene Expression Omnibus (NCBI GEO)**. 
- Data retrieval was conducted using the **GEOquery** R package.
- **Sample groups:** Control, IQOS-exposed, and Cigarette Smoke (CS)-exposed samples (n=3 per group).
- Subsequent analyses were performed on iDEP versions [0.96](http://bioinformatics.sdstate.edu/idep96/) and [2.01](http://bioinformatics.sdstate.edu/idep/).

---

### 2. Exploratory Data Analysis (EDA)
- **Tools used:** iDEP version 0.96
- **Methods:**
  - Hierarchical clustering (heatmap) with average linkage and correlation-based distance measures.
  - Principal Component Analysis (PCA) for dimensionality reduction.
  - Quantile normalization of gene expression levels during data preprocessing.

**Figures:**
- [Heatmap](Assets/heatmap_EDA_globalgeneexpression.png) 
- [PCA Plot](Assets/PCA_EDA.png)
- [Quantile Normalization plot](Assets/transformeddata_EDA.png)

---

### 3. Differential Expression and Functional Enrichment Analysis
- **Tools used:** iDEP version 0.96, limma R package.
  1. IQOS-exposed vs. Control
  2. IQOS-exposed vs. CS-exposed
- **Criteria for Differentially Expressed Genes (DEGs):**
  - False Discovery Rate (FDR) ≤ 0.05
  - |Fold Change| > 1.5
- **Functional enrichment analyses:**
  - GO Biological Process (BP) and KEGG pathway enrichments using Gene Set Enrichment Analysis (GSEA).

**Figures:**
- [DEG Bar Plot](Assets/DEG_limma.png)
- [IQOS-exposed vs. Control Volcano Plot](Assets/volcanoplot_IQOS_control.png)
- [IQOS-exposed vs. CS-exposed Volcano Plot](Assets/volcanoplot_IQOS_CS.png)
- [DEG Venn Diagram](Assets/Venn_DEG.png)
- [Gene Ontology Biological Process Enrichment Tree plot](Assets/GOBP.png)
- [KEGG Enrichment Tables](Assets/KEGG_enrichments_tables.pdf)

  ---

### 4. Network Analysis
- **Tools used:**
  - **iDEP version 2.01** for Weighted Gene Co-Expression Network Analysis (WGCNA).
  - **StringDB version 12** for network visualization.
- **Key Parameters:**
  - Soft threshold = 5
  - Minimum module size = 20
- Functional enrichment for gene co-expression modules was conducted using GO BP and KEGG analyses.

**Figures:**
- [WGCNA Coexpressed Gene Modules and Enrichment](Assets/WGCNA_coexpressed_gene_modules_and_enrichment.png)
- [Apoptosis StringDB PPI](Assets/apoptosis_onlyterms_38_stringDB.png)
- [Cytokine Production StringDB PPI](Assets/cytokine_production_onlyterms_28_stringDB.png)

---

## Citation
If you use the tools or dataset mentioned in this repository in your research, please cite the following references:

- Barrett, T., Wilhite, S. E., Ledoux, P., Evangelista, C., Kim, I. F., Tomashevsky, M., Marshall, K. A., Phillippy, K. H., Sherman, P. M., Holko, M., Yefanov, A., Lee, H., Zhang, N., Robertson, C. L., Serova, N., Davis, S., & Soboleva, A. (2013). NCBI GEO: archive for functional genomics data sets—update. Nucleic Acids Research, 41(D1), D991–D995. https://doi.org/10.1093/NAR/GKS1193

- Ge, S. X., Son, E. W., & Yao, R. (2018). iDEP: an integrated web application for differential expression and pathway analysis of RNA-Seq data. BMC Bioinformatics 2018 19:1, 19(1), 1–24. https://doi.org/10.1186/S12859-018-2486-6

- Nitta, N. A., Sato, T., Komura, M., Yoshikawa, H., Suzuki, Y., Mitsui, A., Kuwasaki, E., Takahashi, F., Kodama, Y., Seyama, K., & Takahashi, K. (2022). Exposure to the heated tobacco product IQOS generates apoptosis-mediated pulmonary emphysema in murine lungs. American Journal of Physiology - Lung Cellular and Molecular Physiology, 322(5), L699–L711. https://doi.org/10.1152/ajplung.00215.2021

- Sean, D., & Meltzer, P. S. (2007). GEOquery: a bridge between the Gene Expression Omnibus (GEO) and BioConductor. Bioinformatics, 23(14), 1846–1847. https://doi.org/10.1093/BIOINFORMATICS/BTM254

- Szklarczyk, D., Kirsch, R., Koutrouli, M., Nastou, K., Mehryary, F., Hachilif, R., Gable, A. L., Fang, T., Doncheva, N. T., Pyysalo, S., Bork, P., Jensen, L. J., & Von Mering, C. (2023). The STRING database in 2023: protein-protein association networks and functional enrichment analyses for any sequenced genome of interest. Nucleic Acids Research, 51(D1), D638–D646. https://doi.org/10.1093/NAR/GKAC1000

---

For questions or issues, please contact the repository maintainer. Refer to the relavant [Poster](Assets/BMI6313_Final_Poster_Meena_Easwaran.pdf) along with the final class paper (via QR code) for detailed information and results.
