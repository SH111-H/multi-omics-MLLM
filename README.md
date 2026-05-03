# Artificial Intelligence for Central Dogma-Centric Multi-Omics

A review-style GitHub scaffold built from the paper *Artificial Intelligence for Central Dogma-Centric Multi-Omics: Challenges and Breakthroughs* (arXiv:2412.12668, Dec 17, 2024).

This repository is a first-pass prototype. The current content is organized from the source paper only, without a full external literature expansion yet.

## Scope

This repo tracks AI methods for central dogma-centric multi-omics with five main threads:

1. Core problems in multi-omics data analysis
2. Cross-modal alignment and fusion strategies
3. Task-oriented method landscape
4. Foundation models for multi-omics
5. Open challenges, benchmarks, and outlook

## Taxonomy

### 1. Core issues in multi-omics

- High dimensionality and strong noise
- Cross-platform heterogeneity and batch effects
- Sparse observations and missingness
- Weak alignment across DNA, RNA, protein, and phenotype layers
- Limited interpretability in downstream disease models

More notes: [resources/challenges.md](resources/challenges.md)

### 2. Alignment strategies

- Linear projector
- Multi-layer perceptron
- Cross-attention
- Q-Former style query compression

More notes: [docs/repo-roadmap.md](docs/repo-roadmap.md)

### 3. Task landscape

| Task family | Representative methods | Entry |
| --- | --- | --- |
| Classification | DRPBind, ConvGNN, LASSO-MOGAT, SMA, SeNMo | [papers/classification.md](papers/classification.md) |
| Regression | MOMA, Wang et al. DNN, OmniBioTE | [papers/regression.md](papers/regression.md) |
| Generation | scAEGAN, OmicsGAN, MichiGAN, siVAE, Precious2GPT | [papers/generation.md](papers/generation.md) |
| Clustering | PCA-Plus, CLCluster, scMDC, GRMEC-SC | [papers/clustering.md](papers/clustering.md) |

### 4. Foundation models

Representative models highlighted in the source review:

- Evo
- scGPT
- LucaOne
- CD-GPT
- scFoundation

More notes: [models/foundation-models.md](models/foundation-models.md)

### 5. Outlook

- Cross-species evaluation systems
- Interpretable fusion guided by biological rules
- Long-sequence modeling
- Multi-organ datasets
- Biological migration and immune applications

More notes: [resources/datasets-and-benchmarks.md](resources/datasets-and-benchmarks.md)

## Repository Map

```text
central-dogma-multiomics-ai-survey/
+-- README.md
+-- papers/
|   +-- README.md
|   +-- classification.md
|   +-- regression.md
|   +-- generation.md
|   `-- clustering.md
+-- models/
|   `-- foundation-models.md
+-- resources/
|   +-- challenges.md
|   `-- datasets-and-benchmarks.md
`-- docs/
    `-- repo-roadmap.md
```

## Source Paper

```bibtex
@article{xin2024ai,
  title   = {Artificial Intelligence for Central Dogma-Centric Multi-Omics: Challenges and Breakthroughs},
  author  = {Lei Xin and Caiyun Huang and Hao Li and Shihong Huang and others},
  journal = {arXiv preprint arXiv:2412.12668},
  year    = {2024}
}
```

## Current Status

- Built from the provided PDF only
- Includes a first-pass taxonomy and representative method list
- Suitable as a repository skeleton before full literature expansion

## Next Build Steps

1. Expand each category into a complete paper table with links, code, and datasets
2. Add a timeline figure and comparison tables
3. Add post-2024 updates beyond the source review
4. Normalize naming, venues, and benchmark metadata

## Contributor
Lei Xin（Wuhan University，2835838600@qq.com）
Zhenglun Kong（Havard University）
Caiyun Huang（Hunan University）
Sihong Huang（Nanjing Agricutural University）
Hao Tang（Peking University）
