# Classification

Representative classification methods highlighted in the review.

| Method | Model family | Target task | Data/source | Venue | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| DRPBind | SVM | DNA/RNA/protein binding site classification | Benchmark dataset from Zhang et al. | bioRxiv | 2023 | Early traditional ML baseline |
| SPHINKS | SVM | Glioblastoma subtype classification | CPTAC-GBM, TCGA-GBM | Nature Cancer | 2023 | Functional subtype classification from multi-omics data |
| ConvGNN | CNN/GNN | COPD classification | COPDGene | PLOS ONE | 2023 | Improves over traditional ML for heterogeneous omics inputs |
| LASSO-MOGAT | GAT/GNN | Pan-cancer classification | TCGA via TCGAbiolinks | Academia Biology | 2024 | Integrates mRNA, miRNA, and DNA methylation |
| HeteroGATomics | GNN | Binary and multiclass cancer tasks | TCGA | arXiv | 2024 | Heterogeneous graph attention for omics integration |
| SMA | Transformer | Cancer subtype identification | TCGA | IEEE | 2023 | Strong multimodal fusion performance on multiple cancers |
| SeNMo | Self-normalizing neural network | Primary cancer type prediction | GDC | arXiv | 2024 | Designed for very high-dimensional fusion settings |

## Notes

- The review frames the transition from SVM-style baselines to GNNs and Transformers as the main evolution in classification.
- Long-range dependency modeling and multimodal fusion are the main reasons Transformer-based models become dominant.
- GNN variants matter when biological relations can be encoded as graphs instead of flat concatenated vectors.

