# Clustering

This category covers dimensionality reduction, subtype discovery, patient grouping, and cell heterogeneity analysis.

| Method | Model family | Target task | Data/source | Venue | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| PCD2Vec | PCA | Host classification of COVID-19 spike proteins | COVID-19 spike protein sequences | IJCNN | 2023 | Statistical dimensionality reduction baseline |
| PCA-Plus | PCA | Batch-effect-aware dimensionality reduction | TCGA | bioRxiv | 2024 | Enhanced PCA adapted for multi-omics |
| Deep Learning Autoencoder | Autoencoder | Multi-omics compression to bottleneck features | TCGA | Clinical Cancer Research | 2018 | Early deep representation learning approach |
| CLCluster | Autoencoder / contrastive learning | Cancer subtype identification and splicing analysis | TCGA | bioRxiv | 2024 | Uses contrastive learning with clustering |
| scMDC | Autoencoder + K-means | Multi-modal single-cell clustering | CITE-seq, SMAGE-seq | Nature Communications | 2022 | Improves cell type identification and batch robustness |
| SpaHDmap | NMF / GNN | Spatial transcriptomics feature embedding | Mouse brain, PDOX, colorectal cancer datasets | bioRxiv | 2024 | Integrates spatial transcriptomics with histology |
| GRMEC-SC | NMF / multi-view ensemble | Single-cell clustering and heterogeneity analysis | Single-cell multi-omics datasets | Bioinformatics | 2024 | Strong on heterogeneity discovery |
| TCGN | CNN / Transformer / GNN | Gene expression prediction via dimensionality reduction | HER2-positive spatial transcriptomics | Medical Image Analysis | 2024 | Combines local and global features |

## Notes

- The review positions clustering as the bridge from classical dimensionality reduction to modern representation learning.
- Autoencoders and contrastive learning are especially important when labels are limited or unavailable.

