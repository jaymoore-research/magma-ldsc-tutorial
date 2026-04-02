# MAGMA & LDSC Cell-Typing Tutorial

A self-contained tutorial demonstrating how to test which cell types drive genetic risk for schizophrenia using two complementary methods:

- **MAGMA cell-typing**: competitive gene-set analysis using gene-property models
- **LDSC-SEG**: partitioned heritability via LD score regression with cell-type-specific annotations

Uses schizophrenia GWAS summary statistics (Trubetskoy et al. 2022, PGC3) and the Allen Institute for Brain Science (AIBS) human cortex cell-type reference.

## Quick Start

```r
# Install dependencies
if (!require("renv")) install.packages("renv")
renv::restore()

# Open and knit the tutorial
# In RStudio: Open tutorial.Rmd -> Knit
# Or from R console:
rmarkdown::render("tutorial.Rmd")
```

## Requirements

- R >= 4.2
- MAGMA binary (auto-installed by MAGMA.Celltyping on first run)
- Internet connection for first run (downloads ~50 MB of reference data, cached thereafter)
- Optional: Python 3 + LDSC for the LDSC-SEG section (pre-computed results included as fallback)

## Data Sources

| Data | Source | Size |
|------|--------|------|
| SCZ3 GWAS gene-level results | Pre-computed via [MAGMA_Files_Public](https://github.com/neurogenomics/MAGMA_Files_Public) | ~2 MB |
| Allen Brain Atlas CTD | [MAGMA.Celltyping releases](https://github.com/neurogenomics/MAGMA_Celltyping) | ~15 MB |
| LDSC-SEG results | Pre-computed, shipped in `data/` | <1 MB |

## Tutorial Sections

1. **Introduction** — what MAGMA and LDSC-SEG do and why
2. **Setup & Data** — load packages, download data, inspect structures
3. **MAGMA Gene-Level Analysis** — explore pre-computed gene-level results
4. **MAGMA Cell-Type Association** — run enrichment, visualise results
5. **LDSC-SEG Cell-Type Enrichment** — partitioned heritability approach
6. **Comparison** — side-by-side MAGMA vs LDSC results
7. **Outputs & Next Steps** — what to do with a full dataset

## References

- Trubetskoy et al. (2022). Mapping genomic loci implicates genes and synaptic biology in schizophrenia. *Nature*, 604, 502-508.
- Skene et al. (2018). Genetic identification of brain cell types underlying schizophrenia. *Nature Genetics*, 50, 825-833.
- de Leeuw et al. (2015). MAGMA: Generalized Gene-Set Analysis of GWAS Data. *PLOS Computational Biology*, 11(4), e1004219.
- Finucane et al. (2018). Heritability enrichment of specifically expressed genes identifies disease-relevant tissues and cell types. *Nature Genetics*, 50, 621-629.

## Licence

MIT
