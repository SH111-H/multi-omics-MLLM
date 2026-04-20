# Regression

Representative regression tasks in the review include gene expression prediction, drug response prediction, and molecular state modeling.

| Method | Model family | Target task | Data/source | Venue | Year | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Seal et al. | MLP | Gene expression prediction in hepatocellular carcinoma | TCGA | Genomics | 2022 | Uses supervised regression on cancer omics |
| Almutiri et al. | Deep Forest | Drug response prediction in cancer cell lines | CCLE | IJACSA | 2023 | Non-neural baseline with competitive performance |
| MOMA | RNN | Growth dynamics and molecular concentration prediction in *E. coli* | Ecomics | Nature Communications | 2016 | Earlier multi-omics regression architecture |
| Wang et al. | DNN | Anti-cancer drug response prediction | CCLE | BMC Bioinformatics | 2021 | Uses attention to improve interpretability |
| OmniBioTE | Transformer | Peptide-nucleotide binding free-energy prediction | GenBank, UniRef100 | arXiv | 2024 | Broad biological sequence regression setup |

## Notes

- The review emphasizes interpretability, label scarcity, and computational cost as the main bottlenecks in regression.
- Attention mechanisms and semi-supervised learning are presented as practical ways to reduce those limitations.

