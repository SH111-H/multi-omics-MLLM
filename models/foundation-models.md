# Foundation Models

The review argues that foundation models are becoming the main route toward reusable multi-omics intelligence, especially when pretraining can encode interactions among DNA, RNA, and proteins.

## Core idea

- Pretrain on large-scale biological sequences with self-supervision
- Learn sequence semantics before task-specific fine-tuning
- Evaluate transfer to downstream omics tasks such as annotation, integration, perturbation prediction, and molecular interaction prediction

## Representative models

| Model | Focus | Notes |
| --- | --- | --- |
| Evo | Long-sequence biological modeling | Highlighted as an early foundation-model attempt for multi-omics tasks |
| scGPT | Single-cell foundation model | Trained on more than 33 million single-cell samples; supports annotation, integration, perturbation response prediction, and network inference |
| LucaOne | DNA-protein classification | Used to probe whether a model can directly reason across biological macromolecule interactions |
| CD-GPT | Central dogma-aware multi-omics large model | Uses a two-stage pretraining setup: single-molecule pretraining, then multi-molecule pretraining |
| scFoundation | Multi-organ pretraining | Emphasizes scale and organ diversity in pretraining data |

## Gaps identified in the review

- Weak biological interpretability
- Incomplete fusion across modalities
- Poor generalization across species, tissues, and tasks
- High cost for long-context training and inference

## Immediate expansion targets

1. Add model cards with architecture, data, tasks, and code links
2. Separate sequence foundation models from single-cell foundation models
3. Add benchmark mapping for each model

