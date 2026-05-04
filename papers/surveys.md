# Surveys and Field Maps

Use this page when you need fast AI/MLLM orientation before diving into individual methods. The first entry is the source paper for this repository.

| Topic | Paper | Venue/source | Year | Why it matters |
| --- | --- | --- | --- | --- |
| Central dogma-centric multi-omics AI | [Artificial Intelligence for Central Dogma-Centric Multi-Omics: Challenges and Breakthroughs](https://arxiv.org/abs/2412.12668) | arXiv | 2024 | Source taxonomy for this repository: challenges, tasks, fusion strategies, and foundation models. |
| Multi-omics deep learning roadmap | [A roadmap for multi-omics data integration using deep learning](https://doi.org/10.1093/bib/bbab454) | Briefings in Bioinformatics | 2021 | Broad review of integration tasks, architectures, and biomedical applications. |
| Technical integration review | [A technical review of multi-omics data integration methods: from classical statistical to deep generative approaches](https://doi.org/10.1093/bib/bbaf355) | Briefings in Bioinformatics | 2025 | Recent systematic review connecting classical statistics, VAEs, and foundation models. |
| Single-cell foundation models | [Single-cell foundation models: bringing artificial intelligence into cell biology](https://www.nature.com/articles/s12276-025-01547-5) | Experimental & Molecular Medicine | 2025 | Recent review of AI/MLLM-style single-cell foundation models. |
| scFM benchmark | [Biology-driven insights into the power of single-cell foundation models](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-025-03781-6) | Genome Biology | 2025 | Benchmarks six scFMs across gene-level and cell-level tasks. |
| Multimodal integration benchmark | [Multitask benchmarking of single-cell multimodal omics integration methods](https://www.nature.com/articles/s41592-025-02856-3) | Nature Methods | 2025 | Evaluates 40 integration methods across 64 real and 22 simulated datasets. |
| Single-cell epigenomic foundation model | [Deciphering single-cell epigenomic language with a foundation model](https://www.nature.com/articles/s41592-025-02851-8) | Nature Methods | 2025 | Places EpiAgent in the epigenomic foundation-model line. |
| scFM utility evaluation | [Evaluating the Utilities of Foundation Models in Single-cell Data Analysis](https://doi.org/10.1002/advs.202514490) | Advanced Science | 2026 | Recent benchmark-oriented evaluation of foundation models for single-cell analysis. |
| Multi-omics integration methods | [Methods and applications for single-cell and spatial multi-omics](https://doi.org/10.1038/s41576-023-00580-2) | Nature Reviews Genetics | 2023 | Strong orientation for single-cell/spatial experimental designs and computational goals. |
| Deep learning for multi-omics | [Deep learning in multi-omics data analysis and precision medicine](https://doi.org/10.3389/fgene.2021.691574) | Frontiers in Genetics | 2021 | Useful entry point for classical deep learning architectures and biomedical use cases. |
| Single-cell multimodal integration | [Single-cell multimodal omics: the power of many](https://doi.org/10.1038/s41592-019-0691-5) | Nature Methods | 2020 | Explains why paired and mosaic single-cell modalities require different integration strategies. |
| Multi-omics cancer subtype discovery | [A review of integrative clustering methods for multi-omics data](https://doi.org/10.1093/bib/bbz015) | Briefings in Bioinformatics | 2019 | Helpful background for clustering and subtype discovery pages. |
| Graph learning for omics | [Graph neural networks in bioinformatics](https://doi.org/10.1093/bib/bbaa170) | Briefings in Bioinformatics | 2021 | Context for graph priors, sample graphs, pathway graphs, and GNN-based fusion. |
| Biological foundation models | [Foundation models for generalist medical artificial intelligence](https://www.nature.com/articles/s41586-023-05881-4) | Nature | 2023 | Not omics-specific, but useful for understanding foundation-model framing and evaluation. |
| Single-cell foundation models | [Harnessing the deep learning power of foundation models in single-cell omics](https://www.nature.com/articles/s41580-024-00756-6) | Nature Reviews Molecular Cell Biology | 2024 | Helps place scGPT, Geneformer, scFoundation, and newer cell models in a common lens. |

## How to classify a new paper

| Question | Put it under |
| --- | --- |
| Does it predict a class label such as cancer subtype, cell type, or disease status? | [Classification](classification.md) |
| Does it predict a continuous value such as IC50, expression level, survival risk, or binding energy? | [Regression](regression.md) |
| Does it synthesize samples, impute missing modalities, translate across modalities, or simulate perturbation? | [Generation](generation.md) |
| Does it discover groups without labels or learn low-dimensional representations for grouping? | [Clustering](clustering.md) |
| Is its central contribution the way modalities are aligned or fused? | [Fusion and integration](fusion-and-integration.md) |
| Is it primarily pretrained and reused across multiple biological tasks? | [Foundation models](../models/foundation-models.md) |
