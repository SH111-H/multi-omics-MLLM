# Classification

Representative classification methods highlighted in the review and a few closely related additions that help round out the category.

| Method | Model family | Target task | Data/source | Paper | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| DRPBind | SVM | DNA/RNA/protein binding site classification | Benchmark dataset from Zhang et al. | [bioRxiv](https://doi.org/10.1101/2023.03.20.533427) | 2023 | Early traditional ML baseline. |
| SPHINKS | Probabilistic classifier | Glioblastoma subtype classification | CPTAC-GBM, TCGA-GBM | [Nature Cancer](https://www.nature.com/articles/s43018-022-00510-x) | 2023 | Functional subtype classification driven by kinase-phosphosite networks. |
| ConvGNN | CNN / GNN | COPD classification | COPDGene | [PLOS ONE](https://doi.org/10.1371/journal.pone.0284563) | 2023 | Improves over traditional ML for heterogeneous omics inputs. |
| PACS / SMA | Transformer | Cancer subtype identification | TCGA | [arXiv](https://arxiv.org/abs/2308.10917) | 2023 | Attention-based multimodal fusion for subtype prediction. |
| MOGONET | GCN | Pan-cancer subtype classification | TCGA | [Nature Communications](https://www.nature.com/articles/s41467-021-23774-w) | 2021 | Strong graph baseline for supervised multi-omics classification. |
| MOGLAM | Graph attention | Cancer subtype prediction | TCGA and METABRIC | [Computers in Biology and Medicine](https://doi.org/10.1016/j.compbiomed.2023.107303) | 2023 | Graph attention fusion for subtype inference. |
| MOGAT | GAT | Cancer subtype prediction | TCGA and METABRIC | [IJMS](https://www.mdpi.com/1422-0067/25/5/2788) | 2024 | Attention weights make the fusion stage easier to inspect. |
| LASSO-MOGAT | LASSO + GAT | Pan-cancer classification | TCGA via TCGAbiolinks | [arXiv](https://arxiv.org/abs/2408.17384) | 2024 | Adds sparse feature selection before graph attention fusion. |
| HeteroGATomics | Heterogeneous GAT | Binary and multiclass cancer tasks | TCGA | [arXiv](https://arxiv.org/abs/2408.02845) | 2024 | Explicitly models heterogeneous omics entities. |
| SeNMo | Self-normalizing neural network | Primary cancer type prediction | GDC | [arXiv](https://arxiv.org/abs/2405.08226) | 2024 | Designed for very high-dimensional fusion settings. |
| GTMancer | Graph transformer / unrolling | Cancer subtype classification | Seven real-world cancer datasets | [IJCAI](https://www.ijcai.org/proceedings/2025/650) | 2025 | A newer graph-transformer direction for multi-omics subtype inference. |

## Notes

- The review frames the transition from SVM-style baselines to graph-based and attention-based models as the main evolution in classification.
- Long-range dependency modeling and multimodal fusion are the main reasons Transformer-based models become more common.
- GNN variants matter when biological relations can be encoded as graphs instead of flat concatenated vectors.

