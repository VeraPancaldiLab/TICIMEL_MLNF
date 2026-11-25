# TNF blockade with certolizumab improves the efficacy of anti-PD-1 and anti-CTLA-4 combination therapy for melanoma


This repository contains the analysis code for the study:

> Margarido Pereira T., Virazels M., Jung B., et al., Montfort A., Ségui B.
> **TNF blockade with certolizumab improves the efficacy of anti-PD-1 and anti-CTLA-4 combination therapy for melanoma.**
> *medRxiv* (2026). https://doi.org/10.64898/2026.02.11.26346073

---

## Descriptions

This repository contains the code for the following analyses of the paper:

1. **CITE-Seq of patient PBMC.** PBMC collected at baseline (W0; `S1` in the code) and week 6 (W6; `S6` in the code) were profiled from 8 patients in each TICIMEL cohort (certolizumab and infliximab) and from 8 patients of the MELANFα trial treated with nivolumab + ipilimumab alone (24 patients in total). CD8⁺ T cells, CD4⁺ T cells and Tregs were then selected from the integrated data and analyzed separately.
   - Pre-processing, QC, CCA integration and clustering (Seurat v5)
   - Selection of T cell subsets with signature scores (Single Cell Signature Explorer)
   - Trajectory analysis (slingshot via SCP)
   - Differential expression and over-representation analysis (Seurat, fgsea / MSigDB)
   - Transcription factor activity inference on pseudo-bulk profiles (decoupleR)
2. **Bulk RNA-Seq of mouse B16-OVA tumors.** 
   - Differential expression (DESeq2)
   - GO Biological Process GSEA (clusterProfiler)
   - Enrichment network analysis (aPEAR) 
