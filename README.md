# Latent Class Analysis in R: A Step-by-Step Guide

This repository contains a comprehensive tutorial for conducting Latent Class Analysis (LCA) in R using the `poLCA` package.

## Overview

The tutorial covers:

- Setting up and running LCA models
- Calculating and comparing fit statistics:
  - AIC/BIC
  - Entropy
  - Average Posterior Probability (AvePP)
  - Odds of Correct Classification (OCC)
  - Bootstrap Likelihood Ratio Test (BLRT)
- Model selection strategies
- Interpreting and visualizing results

## Dataset

The tutorial uses the `cheating` dataset built into the `poLCA` package. This dataset contains self-reported cheating behaviors from 319 undergraduate students with four binary indicators:

| Variable | Description |
|----------|-------------|
| LIEEXAM | Lied to avoid taking an exam |
| LIEPAPER | Lied to avoid handing a paper in on time |
| FRAUD | Purchased a term paper to hand in as own work |
| COPYEXAM | Copied answers during an exam from someone nearby |

This dataset produces fit statistics in typical ranges, making it ideal for teaching purposes.

## Requirements

```r
install.packages(c("poLCA", "tidyverse", "knitr", "kableExtra"))
```

## Files

- `lca-walkthrough.qmd` - Main Quarto document with the full tutorial

## Usage

Open `lca-walkthrough.qmd` in RStudio and render to HTML, or use:

```r
quarto::quarto_render("lca-walkthrough.qmd")
```

## License

This tutorial is provided for educational purposes.

## References

- Linzer, D. A., & Lewis, J. B. (2011). poLCA: An R package for polytomous variable latent class analysis. *Journal of Statistical Software, 42*(10), 1-29.
- Nylund, K. L., Asparouhov, T., & Muthen, B. O. (2007). Deciding on the number of classes in latent class analysis and growth mixture modeling. *Structural Equation Modeling, 14*(4), 535-569.
- Collins, L. M., & Lanza, S. T. (2010). *Latent class and latent transition analysis: With applications in the social, behavioral, and health sciences*. John Wiley & Sons.
