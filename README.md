README for Multi-Variable Mixed Effects Model Analysis

&#x20;

Project Description

This repository contains R code for analyzing the effects of head-down bed rest (HDBR) on lower extremity muscle composition using MRI data and blood biomarkers. The analysis employs linear mixed-effects models (LMM) with unstructured (UN) covariance structure to account for repeated measurements. If UN is unable to construct a model then consider CAR1. Key Features

* Multi-variable mixed effects modeling with UN covariance structure

* Comprehensive model diagnostics including VIF and correlation analysis

* Automated model comparison using AICc criteria

* Publication-ready result tables and visualizations

Repository Structure

project/

├── data/                   # Contains raw and processed data files

│   └── xueye2_xiaotui.xlsx  # Original Excel data file

├── scripts/                 # R analysis scripts

│   └── mixed_effects_analysis.R  # Main analysis script

├── output/                  # Generated results

│   ├── vif_diagnosis.png    # Variance inflation factor plot

│   ├── corrplot.png         # Correlation matrix plot

│   └── best_model_results_CBMATLFF_xueye2.docx  # Model results table

└── README.md                # This file

Requirements

To run this analysis, you will need:

* R (version >= 4.2.0)

* The following R packages:

* install.packages(c("nlme", "tidyverse", "car", "corrplot", "gtsummary",

                 "emmeans", "broom.mixed", "readxl", "flextable"))

Usage Instructions

1. Set your working directory to the project folder:

setwd("path/to/project")

2. Run the main analysis script:

source("scripts/mixed_effects_analysis.R")

3. The script will automatically:

   * Load and preprocess the data

   * Perform multicollinearity diagnostics

   * Build and compare mixed effects models

   * Generate diagnostic plots and result tables

   * Save outputs to the output/folder

Data Description

The analysis uses two sets of variables:

1. ​​Blood biomarkers​​:

l  Ca, P, DR, ACTH, IPTH, CT, OC, OHD

l  UCORT, CORT, RBC, WBC, Hb

2. ​​MRI parameters​​:

l  Muscle cross-sectional area (MHMCSAR, GHMCSAR, etc.)

l  Muscle fat fraction (MHIMATRFF, GHIMATRFF, etc.)

Key Outputs

1. ​​Model comparison table​​: Compares different covariance structures using AICc

2. ​​Best model results​​: Detailed fixed effects estimates with significance levels

3. ​​Diagnostic plots​​:

   * VIF analysis for multicollinearity

   * Correlation matrix of blood biomarkers

   * Model residual diagnostics

License

This project is licensed under the MIT License - see the LICENSEfile for details.

Contact

For questions about this analysis, please contact [Weili Yu] at [yuweili123456@outlook.com]
