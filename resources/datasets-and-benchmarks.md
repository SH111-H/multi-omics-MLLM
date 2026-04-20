# Datasets and Benchmarks

This page collects the benchmark directions emphasized in the source review.

## Benchmarks mentioned or implied

| Area | Examples from the review | Why it matters |
| --- | --- | --- |
| Cancer multi-omics | TCGA, CPTAC-GBM, GDC | Disease subtype discovery, phenotype prediction, survival analysis |
| Drug response | CCLE | Regression and response modeling |
| Single-cell multi-omics | CITE-seq, SMAGE-seq, large pretraining corpora | Cell annotation, integration, perturbation, cross-modal prediction |
| Large biological sequence corpora | GenBank, UniRef100 | Sequence pretraining and transfer |
| Multi-organ single-cell data | scFoundation pretraining corpus | Better generalization across tissues and organs |

## Benchmark needs called out by the review

- Cross-species evaluation systems
- Privacy-aware evaluation for multi-omics data use
- Better downstream task suites for foundation models
- More public multi-organ and multi-modal datasets

## Representative benchmark-oriented tools discussed

- Seurat
- MOJITOO
- scAI
- Subtype-Former
- CBOW

## Next curation pass

1. Add dataset links and access conditions
2. Distinguish bulk, single-cell, and spatial multi-omics
3. Track whether a dataset supports classification, regression, generation, or clustering

