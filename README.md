# APOE4 and Postoperative Cognitive Dysfunction (POCD) – Meta-Analysis

This repository contains R code and data for a meta-analysis assessing the association between the APOE4 gene and short- and medium-term postoperative cognitive dysfunction (POCD).

## Publication

- **Title:** Apolipoprotein E4 allele is genetically associated with risk of the short- and medium-term postoperative cognitive dysfunction: A meta-analysis and trial sequential analysis
- **Journal:** PLOS ONE
- **Authors:** Wei-Jen Hsiao (First Author), et al.
- **Link:** [PLOS ONE Publication](https://doi.org/10.1371/journal.pone.0282214)

## Project Structure

```
.
├── ApoE4.R                 # Main analysis script
├── pocd_1week.csv          # Data for 1-week POCD meta-analysis
├── pocd_1-3months.csv      # Data for 1-3 months POCD meta-analysis
├── pocd_1year.csv          # Data for 1-year POCD meta-analysis
├── delirium.csv            # Data for post-op delirium meta-analysis
└── README.md               # Project description
```

## Statistical Methods Used

- **Random-effects meta-analysis** using `meta` and `metafor` packages
- **Subgroup analysis** by type of surgery
- **Funnel plot** with contour enhancement to assess publication bias
- **Egger’s regression test** to statistically test for publication bias

## Key Skills Demonstrated

- Effect size estimation and heterogeneity quantification
- Visualization: forest plots, funnel plots
- Hypothesis testing and publication bias analysis
- R programming: `meta`, `metafor` packages

## How to Run

1. Open `ApoE4.R` in **RStudio**
2. Make sure the required packages are installed:
   ```r
   install.packages("meta")
   install.packages("metafor")
   ```
3. Run the script to perform meta-analysis and visualize results.

## Funnel Plot Example

To generate:
```r
funnel(res, yaxis = "seinv", level = c(90, 95, 99), shade = c("white", "gray55", "gray75"))
```

To save:
```r
png("funnel_plot.png", width = 800, height = 600)
funnel(res, yaxis = "seinv", level = c(90, 95, 99), shade = c("white", "gray55", "gray75"))
dev.off()
```

---

This project showcases clinical data analysis and publication-quality research using R, applicable to data-driven roles in quantitative finance and beyond.
