# ARCH 241 Assignment #2

Statistical analysis of a thermal comfort chamber study.

**Author:** Urwa Irfan

**Date last updated:** 26 Sep 2026

**Rendered report:** [Link](https://github.com/urwahah/arch241-a2/blob/a6441c8c189b18ada1ee02587b54ab67b04277b5/analysis.html)

## File structure

```
.
├── analysis.qmd      # the analysis 
├── analysis.html     # the rendered report
├── data/
│   └── arch241a2.rda # the dataset, unmodified
├── output/
│   └── q1_statistical-summary.html # summary table for q1
│   └── q2_histograms.png # histogram plots for q2
│   └── ... # plots for the remaining questions
├── README.md
└── .gitignore
```

## How to reproduce this

1. Install [R](https://www.r-project.org/),
   [RStudio](https://posit.co/products/open-source/rstudio/) and
   [Quarto](https://quarto.org/docs/get-started/).
2. Install the packages used here:
   ```r
   install.packages(c("ggplot2", "tidyverse", "gt", "ggh4x", "patchwork", "ggcorrplot", "rstatix", "Metrics", "car"))
   ```
3. Open `analysis.qmd` in RStudio and click **Render** or run
   `quarto render analysis.qmd` in a terminal.

## Findings

1. There is a broad range of observations in all three thermal ratings, with thermal sensation and thermal acceptability indicating a neutral average but thermal comfort indicating a slightly uncomfortable average.
2. Thermal sensation looks normally distributed; thermal comfort is skewed to lower values.
3. Thermal sensation varies broadly by experimental condition, less so by subject, and least of all by sex.
4. Thermal sensation has a strong linear correlation with both operative temperature and PMV.
5. Statistical tests confirm that thermal sensation is normally distributed and thermal comfort is not.
6. Sex does not have a statistically significant impact on thermal sensation.
7. Thermal sensation can be predicted with moderate accuracy using a linear regression with operative temperature.
8. PMV is no better a predictor of thermal sensation than operative temperature alone.
