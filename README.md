# tcga-brca-classification
## TCGA-BRCA Tumor vs Normal Classification
RNA-seq classification project using breast cancer data from TCGA. The goal was to build and compare two classifiers for distinguishing tumor from normal tissue samples.
## What I did
Pulled 113 primary tumor and 113 normal tissue samples using TCGAbiolinks, normalized with TMM and logCPM transformation, and ran PCA to check for separation before modeling. Used limma/voom to rank genes by association with tissue type and pulled the top features for classification. Compared Firth logistic regression and naive Bayes across 100 repeated 80/20 train/test splits to get stable performance estimates.
## Results
Both models performed well. ROC AUC came out around 0.999 across repeated splits. Two-gene models showed small but consistent improvement over single-gene models.
## Tools and packages
R, TCGAbiolinks, edgeR, limma, logistf, e1071, rsample, yardstick, ggplot2
## Course
Mathematical Modeling, Brandeis University, MS Bioinformatics, 2026
