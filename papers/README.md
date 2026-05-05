# Papers

This folder is the living AI/MLLM bibliography for the repository. It starts from the source review and then expands outward to adjacent, newer, and methodologically important papers.

## Index

| Page | What it covers |
| --- | --- |
| [By year](by-year.md) | Chronological paper index for survey-style reading |
| [Classification](classification.md) | Cancer subtype, disease state, and phenotype classification |
| [Regression](regression.md) | Drug response, expression prediction, and continuous phenotype modeling |
| [Generation](generation.md) | Synthetic omics generation, cross-modal translation, and simulation |
| [Clustering](clustering.md) | Subtype discovery, cell grouping, and unsupervised representation learning |
| [Fusion and integration](fusion-and-integration.md) | Alignment, shared latent spaces, graph fusion, and cross-modal embedding |
| [Surveys](surveys.md) | Review papers and field maps for faster orientation |

## How To Use This Folder

1. Start with [Surveys](surveys.md) if you need field context.
2. Use [By year](by-year.md) when you want a timeline across method families.
3. Use the task pages when you already know the prediction or analysis objective.
4. Jump to [../models/foundation-models.md](../models/foundation-models.md) when the main contribution is pretraining and reuse.

## Curation Rules

- Put the paper title or method name on a link.
- Prefer primary sources first, then official preprints, then publisher pages.
- Add dataset, venue, year, and notes whenever they improve searchability.
- Cross-list methods that naturally belong to more than one bucket instead of forcing a single label.
- Keep adding newer AI/MLLM papers as the field moves.

## Scope Boundaries

Use these rough rules when deciding where to place a new paper:

- `classification.md`: label prediction such as subtype, diagnosis, or cell type.
- `regression.md`: continuous prediction such as IC50, expression, survival risk, or affinity.
- `generation.md`: imputation, translation, simulation, perturbation, or synthetic sample generation.
- `clustering.md`: unsupervised grouping, subtype discovery, or representation learning for grouping.
- `fusion-and-integration.md`: the core novelty is modality alignment or fusion.
- `surveys.md`: reviews, benchmarks, and field overviews.

## Maintenance Notes

- Keep duplicate entries intentional and lightweight.
- Prefer one-line notes that explain why a paper is worth tracking.
- Mark missing code links as `N/A` rather than leaving the field ambiguous.
