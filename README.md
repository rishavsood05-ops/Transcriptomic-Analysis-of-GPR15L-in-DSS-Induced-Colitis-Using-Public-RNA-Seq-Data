# Transcriptomic Analysis of GPR15L in DSS-Induced Colitis

## Overview

This project analyzes publicly available RNA-seq data from the NCBI Gene Expression Omnibus (GEO) to investigate the role of GPR15L in DSS-induced colitis, a mouse model of inflammatory bowel disease.

Differential gene expression analysis was performed using DESeq2 in R. Volcano plots, heatmaps, and pathway enrichment analyses were used to identify transcriptional and biological pathway changes associated with GPR15L deletion.

## Research Question

How does deletion of GPR15L alter gene expression and immune-related biological pathways during DSS-induced colitis?

## Dataset

- Organism: Mus musculus
- Experiment type: RNA-seq expression profiling
- Source: NCBI Gene Expression Omnibus
- Conditions analyzed:
  - Colon WT DSS
  - Colon GPR15L-KO DSS
  - LPMCs WT DSS
  - LPMCs GPR15L-KO DSS

## Analysis Pipeline

1. Downloaded processed RNA-seq count data from GEO
2. Imported raw count matrix into R
3. Created sample metadata table
4. Performed differential expression analysis using DESeq2
5. Generated volcano plots and heatmaps
6. Annotated Ensembl gene IDs using org.Mm.eg.db
7. Performed GO and KEGG pathway enrichment analysis using clusterProfiler
8. Interpreted biological pathways affected by GPR15L deletion

## Key Results

- Identified 148 significantly differentially expressed genes in colon tissue using padj < 0.05 and |log2FC| > 1.
- Identified 10 significantly differentially expressed genes in LPMCs.
- Colon tissue showed stronger transcriptional remodeling than LPMCs.
- GO enrichment analysis identified pathways related to B-cell activation and B-cell receptor signaling.
- KEGG enrichment analysis identified immune-related pathways including inflammatory bowel disease, intestinal immune network for IgA production, NF-kappa B signaling, and TGF-beta signaling.

- ## Tools and Packages

- R
- DESeq2
- ggplot2
- pheatmap
- dplyr
- tibble
- clusterProfiler
- org.Mm.eg.db
- AnnotationDbi

## Figures

Figures generated in this project include:

- Colon volcano plot
- LPMC volcano plot
- Colon heatmap
- LPMC heatmap
- GO enrichment plot
- KEGG enrichment plot

- ## Biological Interpretation

GPR15L deletion caused stronger gene expression changes in colon tissue than in LPMCs. Enrichment of B-cell activation, IgA production, NF-kappa B signaling, and IBD-associated pathways suggests that GPR15L may contribute to intestinal immune regulation, host-microbiota interactions, and inflammatory signaling during DSS-induced colitis.

## Future Work

Future analyses could include Gene Set Enrichment Analysis, comparison with additional GEO datasets, integration with microbiome data, and validation of candidate genes using qPCR or protein-expression data.

