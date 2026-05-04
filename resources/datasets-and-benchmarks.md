# Datasets and Benchmarks

This page collects the benchmark directions emphasized in the source review and expands them into reusable data-entry points.

## Dataset Index

| Area | Dataset/resource | Modalities | Best-fit tasks | Access | Notes |
| --- | --- | --- | --- | --- | --- |
| Cancer multi-omics | [TCGA via GDC Data Portal](https://portal.gdc.cancer.gov/) | Genomics, transcriptomics, methylation, miRNA, clinical, pathology images | Classification, clustering, survival/risk regression, generation | Open + controlled tiers | Default cancer multi-omics benchmark; use [TCGAbiolinks](https://bioconductor.org/packages/release/bioc/html/TCGAbiolinks.html) for reproducible R workflows. |
| Cancer proteogenomics | [CPTAC / Proteomic Data Commons](https://pdc.cancer.gov/pdc/) | Proteomics, phosphoproteomics, genomics, transcriptomics, clinical | Classification, clustering, pathway interpretation | Open + controlled tiers | Key resource for central-dogma studies because protein-level data are available with genome and transcriptome context. |
| Cancer cell lines | [CCLE / DepMap](https://depmap.org/portal/ccle/) | Expression, mutation, CNV, methylation, dependency, drug sensitivity | Drug response regression, biomarker discovery | Open portal | Common source for drug-response modeling and cell-line representation learning. |
| Pharmacogenomics | [GDSC](https://www.cancerrxgene.org/) | Drug response, mutation, CNV, expression, tissue annotation | IC50/AUC regression, drug sensitivity classification | Open with usage terms | Often paired with CCLE for external validation. |
| Perturbational transcriptomics | [LINCS L1000 / CMap](https://clue.io/) | Landmark gene expression under chemical/genetic perturbation | Generation, perturbation prediction, retrieval | Registration may be required | Useful for synthetic expression and drug perturbation tasks. |
| Tissue expression | [GTEx Portal](https://gtexportal.org/home/) | Genotype, tissue RNA-seq, QTLs, histology | Tissue-aware regression, expression modeling, pretraining | Open + controlled tiers | Useful for normal-tissue background and tissue specificity. |
| Single-cell atlas | [Human Cell Atlas Data Portal](https://data.humancellatlas.org/) | Single-cell transcriptomics and growing multi-omic atlas data | Annotation, integration, pretraining | Open portal | Multi-organ reference data; good for generalization tests. |
| Single-cell atlas | [CZ CELLxGENE Census](https://chanzuckerberg.github.io/cellxgene-census/) | Standardized scRNA-seq, emerging spatial support | Pretraining, annotation, retrieval, benchmarking | Open API | Versioned, queryable, and convenient for large-scale model training. |
| Single-cell multiome | [10x Genomics Multiome PBMC 10k](https://www.10xgenomics.com/datasets/10-k-human-pbm-cs-multiome-v-1-0-chromium-x-1-standard-2-0-0) | Paired scRNA-seq + scATAC-seq | Integration, cross-modal generation, clustering | Open | Practical paired benchmark with direct raw and processed files. |
| Single-cell multimodal | [10x PBMC 5' Feature Barcode + V(D)J](https://www.10xgenomics.com/datasets/human-pbmc-from-a-healthy-donor-10-k-cells-multi-v-2-2-standard-5-0-0) | RNA, surface protein, immune receptor | Cell annotation, multimodal fusion | Open | Useful for CITE-seq-like RNA/protein workflows. |
| Spatial and multi-modal atlas | [HuBMAP Data Portal](https://portal.hubmapconsortium.org/) | Spatial omics, single-cell, proteomics, imaging | Spatial integration, foundation-model evaluation | Open + controlled tiers | Good candidate for spatial central-dogma expansion. |
| Sequence corpus | [GenBank / NCBI Nucleotide](https://www.ncbi.nlm.nih.gov/genbank/) | DNA/RNA nucleotide sequences | Sequence pretraining, retrieval, annotation | Open | Core sequence resource for DNA/RNA language models. |
| Protein sequence corpus | [UniRef100](https://www.uniprot.org/help/uniref) | Protein sequences | Protein-language pretraining, peptide/protein interaction prediction | Open | Common foundation-model source for protein-aware central-dogma work. |
| Expression compendium | [ARCHS4](https://maayanlab.cloud/archs4/) | Human/mouse RNA-seq expression from GEO/SRA | Pretraining, expression imputation, retrieval | Open | Large processed expression compendium for model pretraining. |
| Simulation | [SymSim](https://github.com/YosefLab/SymSim) | Synthetic single-cell expression | Controlled stress tests, sparsity/noise experiments | Open source | Helpful when evaluating robustness and missingness handling. |

## Benchmark Axes

| Axis | What to report | Why it matters |
| --- | --- | --- |
| Modality coverage | DNA, RNA, protein, methylation, ATAC, spatial, image, phenotype | Prevents overclaiming "multi-omics" when only two layers are used. |
| Pairing pattern | Fully paired, partially paired, mosaic, or unpaired | Determines whether cross-modal generation and alignment claims are valid. |
| Cohort split | Random, tissue-held-out, species-held-out, institution-held-out, patient-held-out | Tests whether the model generalizes or memorizes dataset structure. |
| Batch structure | Platform, lab, institution, sequencing chemistry, tissue source | Batch leakage is a common hidden failure mode. |
| Downstream endpoint | Class label, continuous value, synthetic sample, cluster, embedding, retrieval | Keeps comparisons task-specific and fair. |
| Biological validation | Pathway enrichment, known biomarkers, perturbation consistency, survival association | A model should be biologically plausible, not just numerically strong. |
| Access tier | Open, registered, controlled, commercial terms | Reproducibility depends on whether other groups can actually obtain the data. |

## Benchmark Needs Called Out by the Review

- Cross-species evaluation systems.
- Privacy-aware evaluation for multi-omics data use.
- Better downstream task suites for foundation models.
- More public multi-organ and multimodal datasets.
- Evaluation that distinguishes biological signal from batch, tissue, and platform shortcuts.

## Representative Benchmark-Oriented Tools

| Tool | Link | Use |
| --- | --- | --- |
| Seurat | [Website](https://satijalab.org/seurat/) | Single-cell and multimodal integration, WNN baselines. |
| scvi-tools | [Website](https://scvi-tools.org/) | Probabilistic single-cell modeling, totalVI, MultiVI, model sharing. |
| MOFA+ | [Website](https://biofam.github.io/MOFA2/) | Latent factor baseline for multi-omics integration. |
| GLUE | [GitHub](https://github.com/gao-lab/GLUE) | Graph-linked single-cell multi-omics integration. |
| TCGAbiolinks | [Bioconductor](https://bioconductor.org/packages/release/bioc/html/TCGAbiolinks.html) | Reproducible TCGA/GDC data retrieval and analysis. |
| cptac Python package | [GitHub](https://github.com/PayneLab/cptac) | Programmatic access to CPTAC processed proteogenomics data. |
| cellxgene-census | [Docs](https://chanzuckerberg.github.io/cellxgene-census/) | Versioned single-cell atlas access from Python and R. |

## Minimal Reproducibility Checklist

- Dataset version or access date.
- Exact cohort/cancer type/tissue/cell filters.
- Modality list and preprocessing steps.
- Train/validation/test split with patient/sample identifiers protected from leakage.
- External validation cohort if available.
- Code, random seeds, and environment.
- Metric suite appropriate to the task.

