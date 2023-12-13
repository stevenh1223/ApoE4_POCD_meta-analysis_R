# ApoE4_POCD_meta-analysis_R

### The background 
R script used for the meta-analysis conducted to investigate whether APOE4 was associated with postoperative congnitive dysfunction(POCD) or delirium(POD) occurrence in short- or medium-term among surgical patients

Performed main analyses using R (version 4.1.0) via RStudio (RStudio Team, 2021, version 1.4.1717) 

Computed odds ratio, statistical heterogeneity and subgroup analysis with forest plot carried out by function “metabin” and “forest” in package “meta” version 6.0.0

Examined small-study effect by evaluating the symmetry of the funnel plot and performing Egger’s test using function “regtest” and “funnel” in package “metafor” version 3.8.1

Reference: https://cran.r-project.org/web/packages/metafor/metafor.pdf, https://cran.r-project.org/web/packages/meta/meta.pdf

### How to use
1. Create CSV file, name POCD.csv, then enter study(column: sequential numbers), trialnam(column: name of the study), tcases(column: number of patients with APOE4 and POCD),
tnoncases(column: number of patients with APOE4 without POCD), ttotal(column: number of patients with APOE4),
ccases(column: number of patients without APOE4 with POCD), cnoncases(column: number of patients without APOE4 and POCD),
ctotal(column: number of patients without POCD), and subgroup(column: name of the subgroup, ex: type of surgery) into the first row

2. Replace `C:/Users/Steven/Desktop` in the 2th line and the 11th line with your working directory

3. Run the codes from top to bottom, then the forrest plot, subgroup analysis, contour-enhanced funnel plot, and Egger's test with regression line in the funnel plot appear
