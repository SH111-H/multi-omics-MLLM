# Challenges

The source review repeatedly returns to a stable set of bottlenecks in central dogma-centric multi-omics.

## Data challenges

- High dimensionality with weak sample size
- Noise, sparsity, and missing observations
- Heterogeneous data structures across omics layers
- Batch effects and institution-level domain shifts
- Weak spatial and temporal alignment across modalities

## Modeling challenges

- Nonlinear cross-modal interactions are hard to capture
- Long biological sequences are expensive to model
- Interpretability is often weaker than predictive performance
- Most models still depend on task-specific engineering

## Infrastructure challenges

- Public multi-organ and multi-omics datasets remain limited
- Cross-species evaluation is still immature
- Clinical deployment is blocked by privacy, robustness, and reproducibility concerns

## Why the central dogma framing matters

The source paper organizes the field around interactions among DNA, RNA, and proteins instead of treating each omics modality as an isolated input table. That framing is useful because it pushes model design toward biological consistency rather than purely statistical fusion.

