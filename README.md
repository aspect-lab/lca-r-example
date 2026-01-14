# Latent Class Analysis in R: A Step-by-Step Guide

This repository contains a comprehensive tutorial for conducting Latent Class Analysis (LCA) in R using the `poLCA` package.

## Overview

The tutorial covers:

- Setting up and running LCA models
- Creating synthetic demographic data with realistic school-clustered distributions
- Calculating and comparing fit statistics:
  - AIC/BIC
  - Entropy
  - Average Posterior Probability (AvePP)
  - Odds of Correct Classification (OCC)
  - Bootstrap Likelihood Ratio Test (BLRT)
- Model selection strategies
- Interpreting and visualizing results
- Adding covariates (AGE, SCHOOL, GPA) to predict class membership
- Using SHAP values for predictor importance (optional advanced section)

## Dataset

The tutorial uses the indicator variables from the `cheating` dataset built into the `poLCA` package, combined with **synthetic demographic data** to simulate K-12 student research.

### Indicator Variables (from cheating dataset)

| Variable | Description |
|----------|-------------|
| LIEEXAM | Lied to avoid taking an exam |
| LIEPAPER | Lied to avoid handing a paper in on time |
| FRAUD | Purchased a term paper to hand in as own work |
| COPYEXAM | Copied answers during an exam from someone nearby |

### Synthetic Demographic Variables

| Variable | Description |
|----------|-------------|
| AGE | Student age (10-18 years) |
| SCHOOL | School level (Elementary, Middle School, High School) |
| GPA | Grade point average (1.0-4.0 scale) |
| GPA_ZSCORE | Z-scored GPA within school level |

The GPA distributions are school-clustered with different means and variances by school level, reflecting realistic patterns where elementary students have tighter GPA distributions and high school students show more variation.

## Requirements

```r
install.packages(c("poLCA", "tidyverse", "knitr", "kableExtra", "patchwork",
                   "randomForest", "fastshap"))
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
- Lundberg, S. M., & Lee, S. I. (2017). A unified approach to interpreting model predictions. *Advances in Neural Information Processing Systems*, 30.
