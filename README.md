
<!-- README.md is generated from README.Rmd. Please edit that file -->

# DEP2

<!-- badges: start -->
<!-- badges: end -->
<!-- <img src="logo.png" alt="logo" width="300"/> -->
<!-- ![logo](./logo.png) -->

DEP2 provides an comprehensive analysis workflow for mass spectrometry
based proteomics data, developed from the previous package DEP. This
package provided differential expression/enrichment analysis pipelines
for various data including protein-level quantity(e.g. proteingroup),
peptide-level quantity data and modification-specific proteomics
(quantities of modified peptides). Inherited from DEP, DEP2 provides
functions for data processing, hypothesis testing (via limma) and
visualization. The peptide to protein aggregation strategy is integrated
into workflows. To reduced the barrier in omics analysis, downstream
functional exploration are packaged as suites including functional
enrichment, timecourse cluster and protein-protein interaction network.
DEP2 also contains an easy-used shiny application designed under
modularization.

## Installation

You can install DEP2 from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("mildpiggy/DEP2")
```

DEP2 required an R version higher than 4.1.0. We recommended to install
in the latest R version from scratch to avoid compatibility problem
about dependent packages. For Apple Mac,
[Fortran](https://mac.r-project.org/tools/) compiler is necessary for
some dependencies.

## Check the suggested packages required in analysis

DEP2 install with with basal dependent package in default. Some suggest
packages are required in more analysis modules. Users can run following
commands to complete DEP2 functionality.

``` r
library(DEP2)

# required packages for enrichment analysis
DEP2::check_enrichment_depends(install = TRUE)

# Anotation OrgDb for human
DEP2::check_organismDB_depends(organism = "Human",install = TRUE)

# required packages for PPI analysis
DEP2::check_PPI_depends(install = TRUE)

# required packages for RNA-seq analysis
DEP2::check_RNAseq_depends(install = TRUE)
```

Or, it is available to install DEP2 with all suggest packages.

``` r
devtools::install_github("mildpiggy/DEP2", dependencies = TRUE)
```

## Run shiny application

Run the build-in shiny application though `run_app` function.

``` r
library(DEP2)
DEP2::run_app()
```

## Vignette

View the Vignette for more information

``` r
vignette("DEP2_analysis")
```
