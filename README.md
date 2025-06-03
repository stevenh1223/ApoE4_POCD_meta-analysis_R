# APOE4 and Postoperative Cognitive Dysfunction (POCD) – Meta-Analysis

This repository contains R code and data for a meta-analysis assessing the association between the APOE4 gene and short- and medium-term postoperative cognitive dysfunction (POCD).

## Publication

- **Title:** Apolipoprotein E4 allele is genetically associated with risk of the short- and medium-term postoperative cognitive dysfunction: A meta-analysis and trial sequential analysis
- **Journal:** PLOS ONE
- **First-author contribution:** Data curation, Investigation, Methodology, Software, Writing – original draft
- **Link:** [PLOS ONE Publication](https://doi.org/10.1371/journal.pone.0282214)

## Project Structure

This repository includes the R code and cleaned datasets used to analyze the association between APOE4 and postoperative cognitive dysfunction (POCD).

```
.
├── README.md # Project documentation
├── .gitignore # Ignore system and temp files
├── code/
│ └── ApoE4.R # Main R script for meta-analysis
├── data/
│ ├── pocd_1week.csv # POCD outcomes within 1 week
│ ├── pocd_1year.csv # POCD outcomes at 1 year
│ ├── pocd_1-3months.csv # POCD outcomes between 1–3 months
│ └── delirium.csv # Delirium outcome dataset
```

You can run the analysis using `ApoE4.R` after adjusting the file paths to your local environment.

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

## License

```
Copyright © 2025 Steven Hsiao

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

## Relevance to Quantitative Finance

This project demonstrated:

- Expertise in hypothesis testing and statistical inference  
- Risk quantification under heterogeneous and sparse data conditions  
- Data-driven decision-making under uncertainty  

These analytical skills are directly applicable to:

- Quantitative finance  
- Systematic risk management  
- High-stakes decision frameworks in volatile environments
