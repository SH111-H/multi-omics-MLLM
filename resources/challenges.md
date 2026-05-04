# Challenges

The source review repeatedly returns to a stable set of bottlenecks in central dogma-centric multi-omics. This page turns them into a checklist for evaluating papers and deciding what the repository still needs.

## Data Challenges

| Challenge | What to look for | Useful mitigation |
| --- | --- | --- |
| High dimensionality with weak sample size | Many features, few patients, large variance across cohorts | Sparse feature selection, dimensionality reduction, regularization, external validation |
| Noise and sparsity | Dropout in single-cell data, missing proteins, weak ATAC coverage | Denoising models, modality-specific likelihoods, uncertainty reporting |
| Missing modalities | Mosaic datasets where not every sample has every omics layer | MultiVI-style partial observation models, imputation baselines, missingness-aware splits |
| Batch and platform effects | Cohorts separable by lab, chemistry, platform, or acquisition year | Batch-aware splits, domain adaptation, held-out institution/tissue tests |
| Weak alignment | DNA/RNA/protein/spatial/image measurements collected from different samples or time points | Careful pairing metadata, graph priors, biological pathway constraints |
| Privacy and access | Controlled clinical tiers and non-shareable patient-level data | Federated evaluation, synthetic data, secure enclaves, transparent access notes |

## Modeling Challenges

| Challenge | Why it matters | Evaluation signal |
| --- | --- | --- |
| Nonlinear cross-modal interaction | Central-dogma relations are causal, dynamic, and condition-dependent | Ablations by modality and pathway-level validation |
| Long biological sequence modeling | Genomic context can exceed standard Transformer limits | Context length, variant effects, long-range regulatory tasks |
| Interpretability | Clinical and biological users need mechanism, not only prediction | Gene/pathway stability, perturbation consistency, calibrated explanations |
| Leakage | Patient, tissue, or batch identifiers can masquerade as biology | Patient-level splits, tissue-held-out splits, negative controls |
| Foundation-model hype | Larger pretraining does not guarantee better downstream biology | Compare against strong linear, MOFA+, Seurat, scVI, and task-specific baselines |
| Compute cost | Long-context and large-cell models can be expensive to reproduce | Parameter count, GPU hours, inference latency, checkpoint availability |

## Infrastructure Challenges

- Public multi-organ and multi-omics datasets remain limited.
- Cross-species evaluation is still immature.
- Clinical deployment is blocked by privacy, robustness, reproducibility, and regulatory evidence.
- Benchmarks are fragmented across bulk omics, single-cell omics, spatial omics, and biological sequence modeling.
- Many papers report performance without enough preprocessing and split details to reproduce the result.

## Why the Central Dogma Framing Matters

The source paper organizes the field around interactions among DNA, RNA, and proteins instead of treating each omics modality as an isolated input table. That framing is useful because it pushes model design toward biological consistency rather than purely statistical fusion.

## Open Problems Worth Tracking

| Problem | Why it is promising |
| --- | --- |
| DNA-to-RNA-to-protein causal benchmarking | Directly tests whether a model has learned central-dogma structure. |
| Protein-aware cancer subtype modeling | Adds functional readout beyond transcript abundance. |
| Spatial multi-omics foundation models | Connects molecular layers to tissue architecture. |
| Perturbation-aware multi-omics generation | Moves from observational prediction to intervention modeling. |
| Multi-species transfer | Tests whether learned representations generalize beyond human cohort shortcuts. |
| Model calibration for clinical use | Required before risk prediction and treatment-response tools become credible. |

