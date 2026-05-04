# Foundation Models

The source review argues that foundation models are becoming the main route toward reusable multi-omics intelligence, especially when pretraining can encode interactions among DNA, RNA, proteins, cells, and phenotype.

## Core idea

- Pretrain on large-scale biological sequences or cell atlases with self-supervision.
- Learn transferable sequence, gene, cell, or molecular-interaction representations before task-specific fine-tuning.
- Evaluate transfer to annotation, integration, perturbation prediction, drug response, molecular interaction prediction, and generation.

## Cross-Omics and Central-Dogma Models

| Model | Scope | Paper | Code/resource | Year | Notes |
| --- | --- | --- | --- | --- | --- |
| Evo | DNA, RNA, protein-aware genome-scale sequence modeling | [Science](https://doi.org/10.1126/science.ado9336) | [GitHub](https://github.com/evo-design/evo) | 2024 | Long-context genomic model that generalizes across molecular scales and can generate functional CRISPR/transposon systems. |
| Evo 2 | Genome modeling across all domains of life | [Nature](https://doi.org/10.1038/s41586-026-10176-5) / [bioRxiv](https://doi.org/10.1101/2025.02.18.638918) | [GitHub](https://github.com/ArcInstitute/evo2) | 2026 | Extends Evo to all domains of life with up to 1M context and OpenGenome2-scale pretraining. |
| LucaOne | Unified nucleic-acid and protein language | [Nature Machine Intelligence](https://www.nature.com/articles/s42256-025-01044-4) | [GitHub](https://github.com/LucaOne/LucaOne) | 2025 | Trains DNA/RNA/protein sequences together and directly targets central-dogma reasoning. |
| CD-GPT | DNA/RNA/protein central-dogma pretraining | [bioRxiv](https://doi.org/10.1101/2024.06.24.600337) | N/A | 2024 | Uses shared multi-molecule vocabulary and unified representation for mono- and multi-molecule tasks. |
| Life-Code | Multi-omics sequence unification | [arXiv](https://arxiv.org/abs/2502.07299) | N/A | 2025 | Reverse-transcribes RNA and reverse-translates proteins into nucleotide-style sequences with codon-aware modeling. |
| OmniBioTE | Protein-nucleic acid interaction modeling | [arXiv](https://arxiv.org/abs/2408.16245) / [PLOS ONE](https://doi.org/10.1371/journal.pone.0341501) | [GitHub](https://github.com/nyuolab/OmniBioTE), [Hugging Face](https://huggingface.co/WeiHua/OmniBioTE) | 2024/2026 | Mixed protein/nucleic-acid pretraining; strong fit for binding free-energy prediction. |
| Nucleotide Transformer | Human and multispecies DNA foundation models | [Nature Methods](https://www.nature.com/articles/s41592-024-02523-z) | [GitHub](https://github.com/instadeepai/nucleotide-transformer) | 2025 | Important DNA-only baseline for downstream genomics tasks and variant prioritization; published online in 2024 and issue-dated 2025. |
| DNABERT-2 | Efficient multispecies genome modeling | [arXiv](https://arxiv.org/abs/2306.15006) | [GitHub](https://github.com/Zhihan1996/DNABERT_2) | 2023 | Replaces fixed k-mers with BPE-style genome tokenization and provides a compact benchmark baseline. |
| HyenaDNA | Long-range genomic sequence modeling | [arXiv](https://arxiv.org/abs/2306.15794) | [GitHub](https://github.com/HazyResearch/hyena-dna) | 2023 | Efficient long-context DNA model at single-nucleotide resolution. |
| Caduceus | Reverse-complement-aware DNA modeling | [arXiv](https://arxiv.org/abs/2403.03234) | [GitHub](https://github.com/kuleshov-group/caduceus) | 2024 | Adds bidirectionality and reverse-complement equivariance for long-range genomics. |

## Single-Cell and Spatial Models

| Model | Scope | Paper | Code/resource | Year | Notes |
| --- | --- | --- | --- | --- | --- |
| Geneformer | Single-cell transcriptomes and network biology | [Nature](https://doi.org/10.1038/s41586-023-06139-9) | [Hugging Face](https://huggingface.co/ctheodoris/Geneformer) | 2023 | About 30M cells; strong reference model for network biology and perturbation-style transfer. |
| scGPT | Single-cell multi-omics foundation model | [Nature Methods](https://www.nature.com/articles/s41592-024-02201-0) | [GitHub](https://github.com/bowang-lab/scGPT) | 2024 | Over 33M cells; supports annotation, integration, perturbation prediction, and gene network inference. |
| scFoundation | Large-scale single-cell transcriptomics | [Nature Methods](https://www.nature.com/articles/s41592-024-02305-7) | [GitHub](https://github.com/biomap-research/scFoundation) | 2024 | 100M-parameter model pretrained on more than 50M human cells. |
| GeneCompass | Knowledge-informed cross-species cell model | [Cell Research](https://www.nature.com/articles/s41422-024-01034-y) | [GitHub](https://github.com/xCompass-AI/GeneCompass) | 2024 | Integrates human/mouse single-cell data with prior knowledge such as GRNs and promoter information. |
| UCE | Universal cell embeddings | [bioRxiv](https://doi.org/10.1101/2023.11.28.568918) | [GitHub](https://github.com/snap-stanford/UCE) | 2023 | Cross-species self-supervised cell embedding model. |
| CellFM | 100M-cell human transcriptomic foundation model | [Nature Communications](https://www.nature.com/articles/s41467-025-59926-5) | [GitHub](https://github.com/biomed-AI/CellFM) | 2025 | 800M parameters, trained on 100M human cells; evaluates annotation, perturbation, and gene function tasks. |
| Nicheformer | Single-cell and spatial omics | [Nature Methods](https://www.nature.com/articles/s41592-025-02814-z) | [GitHub](https://github.com/theislab/nicheformer) | 2025 | SpatialCorpus-110M; brings spatial context into foundation-scale cell representations. |
| Novae | Spatial transcriptomics | [Nature Methods](https://www.nature.com/articles/s41592-025-02899-6) | [GitHub](https://github.com/MICS-Lab/novae) | 2025 | Graph-based spatial foundation model trained on nearly 30M cells across 18 tissues. |
| EpiAgent | Single-cell epigenomics | [Nature Methods](https://www.nature.com/articles/s41592-025-02822-z) | N/A | 2025 | Extends foundation-model framing to scATAC-seq and epigenomic tasks. |
| scvi-hub | Pretrained probabilistic single-cell models | [Nature Methods](https://www.nature.com/articles/s41592-025-02799-9) | [scvi-tools](https://scvi-tools.org/) | 2025 | Infrastructure for sharing reusable single-cell models and references. |

## Recent Reviews and Evaluations

| Topic | Link | Year | Why it matters |
| --- | --- | --- | --- |
| Single-cell foundation-model guidance | [Nature Reviews Molecular Cell Biology](https://www.nature.com/articles/s41580-024-00756-6) | 2024 | Short comment on progress, limitations, and best practices. |
| Single-cell foundation-model review | [Experimental & Molecular Medicine](https://doi.org/10.1038/s12276-025-01547-5) | 2025 | Broad review of scFMs and downstream single-cell use cases. |
| Zero-shot single-cell FM evaluation | [bioRxiv](https://doi.org/10.1101/2023.09.08.555192) / [Nature Methods highlight](https://www.nature.com/articles/s41592-025-02735-x) | 2023/2025 | Important cautionary work: foundation-model embeddings do not automatically beat simpler baselines. |
| Genomic language-model guide | [Molecular Systems Biology](https://doi.org/10.1038/s44320-025-00184-4) | 2026 | Recent field guide for pretrained DNA/RNA language models. |

## Gaps Identified in the Review

- Weak biological interpretability, especially when attention or latent dimensions are overinterpreted.
- Incomplete fusion across DNA, RNA, protein, spatial, perturbation, and phenotype layers.
- Poor generalization across species, tissues, technologies, and clinical cohorts.
- High cost for long-context training and inference.
- Weak benchmark agreement for foundation-model claims.

## Suggested Model Card Fields

| Field | Example values |
| --- | --- |
| Modality | DNA, RNA, protein, scRNA-seq, scATAC-seq, spatial transcriptomics |
| Scale | Number of cells, tokens, genomes, species, parameters, context length |
| Architecture | Transformer, Hyena, Mamba, VAE, probabilistic model |
| Pretraining task | Masked modeling, autoregressive generation, contrastive alignment, translation/distillation |
| Downstream tasks | Annotation, integration, perturbation, drug response, generation, interaction prediction |
| Availability | Paper, code, checkpoints, API, dataset |
| Biological caveat | Species coverage, assay bias, modality mismatch, leakage risk, interpretability limit |

