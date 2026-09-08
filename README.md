# Workshop: introduction to mixOmics

### Author: Prof Kim-Anh Lê Cao

A short, hands-on introduction to multivariate analysis for omics data using the
[mixOmics](https://mixomics.org) R package. The session runs for about 1.5 hours
and is built around a single practical that participants work through on their
own machine.

| Audience | Prerequisites | Duration |
| --- | --- | --- |
| Biologists and computational biologists | [Introduction to mixOmics](https://mixomics.org/introduction-to-mixomics/) video, and a working knowledge of R | ~ 1.5 hours |

### Material

- **Practical:** https://guides.mixomics.org/mxoorg-workshop-intro-mixomics/
- **Slides:** [slides-intro-mixomics.pdf](slides-intro-mixomics.pdf)
- **R script:** [multivariate_analysis.R](multivariate_analysis.R) — the code from
  the practical on its own, for following along during the session.
- **Source:** [multivariate_analysis.Rmd](multivariate_analysis.Rmd)

### What the session covers

The practical works through three methods, each on a dataset that ships with the
package, so there is nothing to download:

1. **PCA** on the `nutrimouse` data — unsupervised exploration, and sparse PCA
   for variable selection.
2. **PLS-DA** on the `srbct` data — supervised classification of tumour
   subtypes, then sparse PLS-DA to select the genes that discriminate them.
3. **DIABLO** on the `breast.TCGA` data — integrating mRNA, miRNA and protein
   measurements while discriminating breast cancer subtypes, and predicting the
   subtypes of a held-out test set.

Exercises are set throughout, with answers hidden behind show and hide buttons
so you can attempt them first.

### Before the workshop

**1. Watch the video.** Start with the
[Introduction to mixOmics](https://mixomics.org/introduction-to-mixomics/)
recording. It covers the ideas the practical assumes, so the session itself can
be spent on the hands-on work rather than on the theory.

**2. Install the software.** Install R, then RStudio. Use recent versions of
both:

- [R](https://cran.r-project.org/) (R 4.0 or later)
- [RStudio](https://posit.co/download/rstudio-desktop/#download)

Then install mixOmics from Bioconductor, and check that it loads:

```r
if (!requireNamespace("BiocManager", quietly = TRUE)) {
  install.packages("BiocManager")
}
BiocManager::install("mixOmics")

# No error messages means you are set. Warnings are fine.
library(mixOmics)
```

**Apple mac users:** if the imported `rgl` package will not install, install
[XQuartz](https://www.xquartz.org) first, then try again.

### Provenance

This material derives from
[melbintgen/intro-to-multivariate-analysis](https://github.com/melbintgen/intro-to-multivariate-analysis),
written by Kim-Anh Lê Cao for Melbourne Integrative Genomics, with thanks to
Saritha Kodikara.

### Licence

Copyright © 2024–2026 Kim-Anh Lê Cao. Licensed under AGPL-3.0-or-later.
See [LICENSE](LICENSE) for the full text.
