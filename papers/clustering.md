# Clustering

This category covers dimensionality reduction, subtype discovery, patient grouping, spatial feature embedding, and cell heterogeneity analysis.

| Method | Model family | Target task | Data/source | Paper | Code/resource | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| SNF | Similarity network fusion | Patient subtype discovery | Multi-omics cancer cohorts | [Nature Methods](https://www.nature.com/articles/nmeth.2810) | [SNFtool](https://cran.r-project.org/web/packages/SNFtool/index.html) | 2014 | Classical benchmark for patient-level multi-omics clustering. |
| Deep Learning Autoencoder | Autoencoder | Survival subtype discovery | TCGA liver cancer | [Clinical Cancer Research](https://doi.org/10.1158/1078-0432.CCR-17-0853) | N/A | 2018 | Early deep representation learning approach for cancer multi-omics. |
| iClusterPlus | Joint latent variable model | Cancer subtype discovery | TCGA and other genomic cohorts | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btu862) | [Bioconductor](https://bioconductor.org/packages/release/bioc/html/iClusterPlus.html) | 2015 | Still useful as a statistical reference baseline. |
| PCD2Vec | PCA | Host classification of COVID-19 spike proteins | COVID-19 spike protein sequences | [IJCNN](https://doi.org/10.1109/IJCNN54540.2023.10191255) | N/A | 2023 | Statistical dimensionality-reduction baseline from the review. |
| scMDC | Autoencoder + K-means | Multimodal single-cell clustering | CITE-seq, SMAGE-seq | [Nature Communications](https://www.nature.com/articles/s41467-022-35031-9) | [GitHub](https://github.com/xianglin226/scMDC) | 2022 | Improves cell type identification and batch robustness. |
| DeepAutoGlioma | Autoencoder | Glioma subtype discovery/classification | TCGA transcriptome and methylome | [BioData Mining](https://biodatamining.biomedcentral.com/articles/10.1186/s13040-023-00349-7) | N/A | 2023 | Example of disease-specific autoencoder integration. |
| CLCluster | Contrastive autoencoder | Cancer subtype identification and splicing analysis | TCGA | [bioRxiv](https://doi.org/10.1101/2024.01.19.576272) | [GitHub](https://github.com/jiangyanucas/CLCluster) | 2024 | Uses contrastive learning with clustering. |
| PCA-Plus | PCA | Batch-effect-aware dimensionality reduction | TCGA | [bioRxiv](https://doi.org/10.1101/2024.01.02.573793) | N/A | 2024 | Enhanced PCA adapted for multi-omics. |
| SpaHDmap | NMF / GNN | Spatial transcriptomics feature embedding | Mouse brain, PDOX, colorectal cancer datasets | [bioRxiv](https://doi.org/10.1101/2024.02.12.580044) | [GitHub](https://github.com/QuKunLab/SpaHDmap) | 2024 | Integrates spatial transcriptomics with histology. |
| GRMEC-SC | NMF / multi-view ensemble | Single-cell clustering and heterogeneity analysis | Single-cell multi-omics datasets | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btae169) | [GitHub](https://github.com/polarisChen/GRMEC-SC) | 2024 | Graph-regularized multi-view ensemble clustering. |
| TCGN | CNN / Transformer / GNN | Gene expression prediction and spatial representation | HER2-positive spatial transcriptomics | [Medical Image Analysis](https://doi.org/10.1016/j.media.2023.103040) | N/A | 2024 | Combines local image cues, global context, and graph structure. |

## Notes

- The review positions clustering as the bridge from classical dimensionality reduction to modern representation learning.
- Autoencoders and contrastive learning are especially important when labels are limited or unavailable.
- Patient-level clustering and cell-level clustering should be evaluated separately because the data geometry and failure modes are different.

