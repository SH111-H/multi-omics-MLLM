# Generation

Generative models in the review are used for data integration, synthetic data generation, cross-modal mapping, privacy-preserving simulation, histopathology translation, and cellular state modeling.

| Method | Model family | Target task | Data/source | Paper | Code/resource | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Subtype-GAN | GAN | Cancer subtyping | TCGA | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btab109) | N/A | 2021 | Integrative cancer subtyping through adversarial generation. |
| MichiGAN | VAE + GAN | Cellular identity manipulation | Single-cell RNA-seq datasets | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-021-02373-4) | [GitHub](https://github.com/welch-lab/MichiGAN) | 2021 | Samples from disentangled single-cell representations. |
| OmicsGAN | GAN | Disease phenotype prediction and survival prediction | TCGA BRCA, LUAD, OV | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btab608) | [GitHub](https://github.com/CompbioLabUCF/omicsGAN) | 2022 | Fuses mRNA/miRNA and biological interaction networks into synthetic features. |
| scAEGAN | GAN | Single-cell multi-omics integration | SymSim, hematopoietic stem cell, pancreatic islet, paired scRNA/scATAC | [PLOS ONE](https://doi.org/10.1371/journal.pone.0281315) | [GitHub](https://github.com/sumeer1/scAEGAN) | 2023 | Adversarial latent-space correspondence for paired and unpaired data. |
| siVAE | VAE | Interpretable genomic representation learning | Fetal Liver Atlas and other single-cell datasets | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-02850-y) | [GitHub](https://github.com/quon-titative-biology/siVAE) | 2023 | Designed for interpretable latent dimensions and gene-module discovery. |
| MultiVI | VAE | Missing modality generation and joint embedding | Paired and unpaired scRNA/scATAC | [Nature Methods](https://www.nature.com/articles/s41592-023-01909-9) | [scvi-tools](https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html) | 2023 | Important baseline for mosaic single-cell multi-omics datasets. |
| scCross | VAE / GAN / MNN | Data integration and cross-modal generation | Matched mouse single-cell multi-omics | [Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-024-03338-z) | N/A | 2024 | Supports integration, cross-modal generation, simulation, and perturbation. |
| MOSD | Self-diffusion on affinity networks | Cancer subtype identification | TCGA gene expression, methylation, miRNA | [Journal of Translational Medicine](https://doi.org/10.1186/s12967-024-04864-x) | [GitHub](https://github.com/DXCODEE/MOSD) | 2024 | Diffusion-style graph refinement for subtype discovery rather than sample synthesis. |
| Precious2GPT | Transformer + conditional diffusion | Synthetic multi-omics sample generation | GTEx, ARCHS4, methylation datasets, LINCS landmarks | [npj Aging](https://www.nature.com/articles/s41514-024-00163-3) | N/A | 2024 | Generates multi-species and multi-tissue expression/methylation profiles. |
| His-MMDM | Diffusion | Multi-domain and multi-omics histopathology translation | TCGA images with genomic/transcriptomic profiles | [medRxiv](https://doi.org/10.1101/2024.07.11.24310294) | [GitHub](https://github.com/lzx325/His-MMDM) | 2024 | Extends generation toward genomics- and transcriptomics-guided image editing. |

## Notes

- The review groups GANs, VAEs, and diffusion models as the three dominant generative families.
- Single-cell settings are a major use case because generative models help with sparsity, noisy observations, missing modalities, and cross-modal reconstruction.
- Newer work is moving beyond tabular omics into omics-conditioned histopathology and synthetic cohorts.
- Interpretability remains a core issue even when generation quality is strong.

