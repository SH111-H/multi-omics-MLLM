# Generation

Generative models in the review are used for data integration, synthetic data generation, cross-modal mapping, privacy-preserving simulation, and cellular state modeling.

| Method | Model family | Target task | Data/source | Venue | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| scAEGAN | GAN | Single-cell multi-omics integration | SymSim, mouse hematopoietic stem cell, pancreatic islet, paired scRNA/scATAC | PLOS ONE | 2023 | Strong cross-modal integration behavior |
| Subtype-GAN | GAN | Cancer subtyping | TCGA | Bioinformatics | 2021 | Integrative clustering through generation |
| OmicsGAN | GAN | Disease phenotype prediction | TCGA | Bioinformatics | 2022 | Fuses mRNA and miRNA with interaction networks |
| MichiGAN | GAN | Cellular identity manipulation | Single-cell RNA-seq datasets | Genome Biology | 2021 | Uses disentangled latent representations |
| siVAE | VAE | Genomic representation learning | Fetal Liver Atlas | Genome Biology | 2023 | Focuses on interpretability of latent structure |
| scCross | Autoencoder | Data integration and cross-modal generation | Matched mouse multi-omics datasets | Genome Biology | 2024 | Single-cell multimodal fusion and generation |
| Precious2GPT | Diffusion | Synthetic multi-omics generation | LINCS L1000 | npj Aging | 2024 | Combines a pretrained transformer with diffusion |
| MOSD | Diffusion | Cancer subtype identification | TCGA | Journal of Translational Medicine | 2024 | Self-diffusion with weighted affinity integration |

## Notes

- The review groups GANs, VAEs, and diffusion models as the three dominant generative families.
- Single-cell settings are a major use case because generative models help with sparsity, noisy observations, and cross-modal reconstruction.
- Interpretability remains a core issue even when generation quality is strong.

