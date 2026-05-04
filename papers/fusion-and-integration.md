# Fusion and Integration

This page tracks methods whose main contribution is cross-omics alignment, fusion, or shared representation learning. Some methods are also listed under downstream tasks when they are commonly evaluated for subtype prediction, clustering, or cross-modal generation.

## Representative Methods

| Method | Main idea | Omics setting | Paper | Code/resource | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| MOFA | Multi-omics factor analysis | Bulk and single-cell multi-view data | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1438-3) | [MOFA2](https://biofam.github.io/MOFA2/) | 2018 | Strong statistical baseline for latent factor discovery and interpretation. |
| MOFA+ | Scalable Bayesian factor analysis | Large multi-omics cohorts | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02015-1) | [MOFA2](https://biofam.github.io/MOFA2/) | 2020 | Useful anchor method before deep generative fusion models. |
| Seurat WNN | Weighted nearest-neighbor fusion | Single-cell multimodal data | [Cell](https://doi.org/10.1016/j.cell.2021.04.048) | [Seurat](https://satijalab.org/seurat/) | 2021 | Widely used practical baseline for multimodal single-cell analysis. |
| totalVI | Deep generative RNA-protein model | CITE-seq RNA + protein | [Nature Methods](https://www.nature.com/articles/s41592-020-01050-x) | [scvi-tools](https://docs.scvi-tools.org/en/stable/user_guide/models/totalvi.html) | 2021 | Models technical noise while learning a joint latent space. |
| Cobolt | Joint probabilistic embedding | Single-cell multi-omics | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-021-02556-z) | [GitHub](https://github.com/epurdom/cobolt) | 2021 | Handles heterogeneous single-cell modalities in a shared representation. |
| scJoint | Transfer learning across modalities | scRNA-seq + scATAC-seq | [Nature Biotechnology](https://www.nature.com/articles/s41587-021-01161-6) | [GitHub](https://github.com/SydneyBioX/scJoint) | 2022 | Aligns unpaired single-cell measurements for label transfer. |
| GLUE | Graph-linked unified embedding | scRNA-seq, scATAC-seq, regulatory graph | [Nature Biotechnology](https://www.nature.com/articles/s41587-022-01284-4) | [GitHub](https://github.com/gao-lab/GLUE) | 2022 | Adds prior biological graph structure to the integration problem. |
| scMDC | Multimodal deep clustering | CITE-seq and SMAGE-seq | [Nature Communications](https://www.nature.com/articles/s41467-022-35031-9) | [GitHub](https://github.com/xianglin226/scMDC) | 2022 | Jointly optimizes feature learning, clustering, and batch correction. |
| MultiVI | Joint model for paired and unpaired data | scRNA-seq + scATAC-seq | [Nature Methods](https://www.nature.com/articles/s41592-023-01909-9) | [scvi-tools](https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html) | 2023 | Especially useful for mosaic datasets with incomplete modality coverage. |
| MOGLAM | Multi-omics graph learning with attention | Cancer subtype classification | [Computers in Biology and Medicine](https://doi.org/10.1016/j.compbiomed.2023.107303) | N/A | 2023 | Attention-based graph fusion for patient classification. |
| MOGONET | Multi-omics graph convolutional network | Cancer subtype classification | [Nature Communications](https://www.nature.com/articles/s41467-021-23774-w) | [GitHub](https://github.com/txWang/MOGONET) | 2021 | Common reference point for graph-based patient-level multi-omics fusion. |
| MOGAT | Graph attention network fusion | Multi-omics disease prediction | [IJMS](https://www.mdpi.com/1422-0067/25/5/2788) | [GitHub](https://github.com/MezbahJUCSE39/MOGAT) | 2024 | Uses graph attention to model sample and feature interactions. |
| LASSO-MOGAT | Feature selection + graph attention | mRNA + miRNA + DNA methylation | [arXiv](https://arxiv.org/abs/2408.17384) | N/A | 2024 | Combines sparse feature selection with graph attention. |
| HeteroGATomics | Heterogeneous graph attention | Cancer binary and multiclass tasks | [arXiv](https://arxiv.org/abs/2408.02845) | N/A | 2024 | Explicitly represents heterogeneous omics entities before downstream prediction. |
| scCross | VAE/GAN/MNN cross-modal model | Single-cell multi-omics | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-024-03338-z) | N/A | 2024 | Integrates, generates, simulates, and perturbs across modalities. |
| SIMO | Spatial multi-omics integration | Spatial multi-omics single-cell data | [Nature Communications](https://www.nature.com/articles/s41467-025-56523-4) | N/A | 2025 | Spatial alignment of multi-omics single-cell data. |
| HALO | Hierarchical causal modeling | Coupled and decoupled single-cell multi-omics | [Nature Communications](https://www.nature.com/articles/s41467-025-63921-1) | N/A | 2025 | Models causal dependence across modalities and cell states. |
| scTFBridge | Gene regulation inference | Single-cell multi-omics gene regulation | [Nature Communications](https://www.nature.com/articles/s41467-025-64227-y) | N/A | 2025 | Bridges TF motifs and downstream regulatory effects. |
| MultiVeloVAE | Latent dynamic modeling | Multi-omic velocity / RNA-accessibility coupling | [Nature Communications](https://www.nature.com/articles/s41467-025-66287-6) | N/A | 2025 | Extends velocity-style modeling into joint multi-omic dynamics. |

## Alignment Patterns

| Pattern | Typical use | Representative links |
| --- | --- | --- |
| Linear projection | Quick baseline when modalities have comparable sample-level alignment | [MOFA+](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02015-1) |
| Deep latent bottleneck | Denoising, missing modality reconstruction, and batch robustness | [totalVI](https://www.nature.com/articles/s41592-020-01050-x), [MultiVI](https://www.nature.com/articles/s41592-023-01909-9) |
| Biological graph prior | Gene regulatory, pathway, or sample similarity graphs | [GLUE](https://www.nature.com/articles/s41587-022-01284-4), [MOGONET](https://www.nature.com/articles/s41467-021-23774-w) |
| Attention fusion | Learned modality weighting and heterogeneous feature interaction | [MOGAT](https://www.mdpi.com/1422-0067/25/5/2788), [HeteroGATomics](https://arxiv.org/abs/2408.02845) |
| Cross-modal generation | Predict missing modalities or simulate cell states | [scCross](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-024-03338-z) |
| Spatial and causal alignment | Preserve tissue structure and modality-dependent causality | [SIMO](https://www.nature.com/articles/s41467-025-56523-4), [HALO](https://www.nature.com/articles/s41467-025-63921-1), [scTFBridge](https://www.nature.com/articles/s41467-025-64227-y), [MultiVeloVAE](https://www.nature.com/articles/s41467-025-66287-6) |
