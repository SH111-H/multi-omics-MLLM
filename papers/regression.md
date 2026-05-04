# Regression

Representative regression tasks in the review include gene expression prediction, drug response prediction, survival-risk modeling, and molecular interaction scoring.

| Method | Model family | Target task | Data/source | Paper | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| MOMA | RNN | Growth dynamics and molecular concentration prediction in *E. coli* | Ecomics | [Nature Communications](https://www.nature.com/articles/ncomms13090) | 2016 | Earlier sequence-model example for multi-omics state prediction. |
| MOLI | Late-integration DNN | Drug response prediction | GDSC, PDX, TCGA | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btz318) | 2019 | Learns omics-specific encoders before a shared drug-response representation. |
| DeepProg | Ensemble deep learning | Survival and cancer outcome prediction | TCGA | [Bioinformatics](https://doi.org/10.1093/bioinformatics/btz154) | 2019 | Useful for prognosis-style continuous/risk outputs. |
| Clayton et al. | ML regression/classification | Cancer drug response prediction | TCGA, GDSC | [BMC Bioinformatics](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03690-4) | 2020 | Patient-expression-to-drug-response transfer setup. |
| Wang et al. | DNN + graph embedding + attention | Anti-cancer drug response prediction | CCLE, GDSC, PPI | [BMC Bioinformatics](https://doi.org/10.1186/s12859-022-04964-9) | 2021 | Integrates expression, CNV, mutation, RPPA, metabolomics, and interactome priors. |
| NeRD | Multichannel neural network | Cellular drug response prediction | Drug informatics + multi-omics | [BMC Medicine](https://bmcmedicine.biomedcentral.com/articles/10.1186/s12916-022-02549-0) | 2022 | Multi-channel architecture for drug and omics features. |
| Seal et al. | MLP | Gene expression prediction in hepatocellular carcinoma | TCGA | [Genomics](https://doi.org/10.1016/j.ygeno.2021.12.011) | 2022 | Uses supervised regression on cancer omics. |
| Almutiri et al. | Deep Forest | Drug response prediction in cancer cell lines | CCLE | [IJACSA](https://thesai.org/Publications/ViewPaper?Volume=14&Issue=8&Code=IJACSA&SerialNo=106) | 2023 | Non-neural baseline with competitive behavior in high-dimensional data. |
| Hauptmann & Kramer | Autoencoder benchmark | Latent representation learning for drug response | Multi-omics drug response datasets | [BMC Bioinformatics](https://doi.org/10.1186/s12859-023-05166-7) | 2023 | Helpful benchmark for comparing neural latent spaces. |
| DeepAEG | Graph neural network | IC50 prediction | Genomics + drug graphs | [BMC Bioinformatics](https://doi.org/10.1186/s12859-024-05723-8) | 2024 | Adds molecular graph edge updates and data augmentation. |
| OmniBioTE | Transformer | Peptide-nucleotide binding free-energy prediction | GenBank, UniRef100 | [arXiv](https://arxiv.org/abs/2405.10979) | 2024 | Broad biological sequence regression setup with zero-shot and fine-tuning use cases. |

## Notes

- The review emphasizes interpretability, label scarcity, and computational cost as the main bottlenecks in regression.
- Drug response prediction is the densest subarea because public pharmacogenomics data make supervised evaluation easier.
- Attention, graph priors, and self-supervised pretraining are recurring ways to improve both performance and interpretability.

