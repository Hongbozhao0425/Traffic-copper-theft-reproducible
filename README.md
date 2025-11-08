# Predicting Traffic Copper Cable Theft and Its Contributing Factors - A Reproducible Time-Series Modelling Approach


## Overview

This repository accompanies the research paper “Predicting Traffic Copper Cable Theft and Its Contributing Factors: A Reproducible Time-Series Modelling Approach”.

The study focuses on traffic copper cable theft incidents in New South Wales, Australia (2010–2023), developing an integrated time-series modelling framework that combines econometric models (Log–log and ARIMAX) and a machine-learning model (XGBoost).  
It systematically analyses multiple explanatory factors, including copper price fluctuations, global scrap copper demand, unemployment rate, overall theft level, legislative interventions, and seasonal (monthly) variations, and compares the predictive performance and interpretability of different models.

Results show that copper price and overall theft level are long-term, stable external drivers of traffic copper cable theft. Legislative interventions temporarily reduce theft incidents but do not provide lasting deterrence.  
Seasonal effects are generally weak, with minor peaks observed in May and September. Overall, traffic copper cable theft exhibits low inertia but high responsiveness, driven primarily by immediate market conditions and broader crime dynamics.


## Key Contributions

The main contributions of this study are as follows:

- **Research Extension:** Expands metal theft research to the underexplored area of traffic infrastructure theft, jointly examining copper prices, global scrap demand, unemployment, overall theft levels, and seasonal patterns.  
- **Methodological Innovation:** Establishes a cross-method comparative framework integrating Log–log, ARIMAX, and XGBoost models, and introduces legislative variables to distinguish short-term and cumulative effects.  
- **Reproducibility Framework:** Implements a fully automated and reproducible workflow in R and Quarto, enhancing transparency and verifiability in transport crime analysis.

This repository releases all datasets, analysis scripts, and reproducible Quarto (.qmd) documents, supporting transparent and verifiable research and policy assessment.  
This README corresponds to the reproducibility repository for the paper submitted to European Transport Research Review.


## Repository Structure

The repository follows a four-layer reproducible research framework:  

├── 01_Data/         Raw and processed datasets  
├── 02_Scripts/      R scripts for model development (Log–log, ARIMAX, XGBoost)  
├── 03_Outputs/      Figures and tables used in the manuscript  
├── 04_Manuscript/   Reproducible manuscript (.qmd)  
└── Run_all.R/        Master script to execute the workflow  

The following section describes the data sources used within this structure.

## Data

This repository includes all datasets used in the study, covering economic, legislative, and crime-related indicators for **New South Wales, Australia (2010–2023)**.

- **Traffic Copper Cable Theft:** Dataset provided and compiled by *Professor Zuduo Zheng’s research group* at *The University of Queensland*. Included in this repository with permission for research reproducibility.  
- **Overall Theft in NSW:** Monthly property crime index from the *NSW Bureau of Crime Statistics and Research (BOCSAR)*.  
- **Unemployment Rate:** Monthly unemployment rate (%) from the *Australian Bureau of Statistics (ABS)*.  
- **Global Copper Price:** Monthly median COMEX spot prices from *Macrotrends*.  
- **China’s Scrap Copper Imports:** Monthly import volumes (thousand tonnes) from *CEIC Database*.  
- **Legislative, Seasonal, and Lag Variables:** Internally generated for model analysis.

Detailed variable definitions and preprocessing notes are available in `/01_Data/01_Data_description/`.


## Reproducibility and Execution

This project requires **R (≥ 4.4.2)** and **Quarto (≥ 1.7.32)**. All required R packages are automatically installed and loaded through `/02_Scripts/01_Required_Packages_and_Setup/`.  No additional configuration is needed once the repository is cloned.

To reproduce all analyses and results:

1. **Open the project**  
   Launch the project file `Github.Rproj` in **RStudio** (or open the repository root folder as your working directory).

2. **Run the master script**  
   In the **R Console** (bottom-left panel in RStudio), enter the following command:

```r
source("Run_all.R")
```
This command will automatically execute the full reproducible workflow — including data preprocessing, model estimation (Log–log, ARIMAX, and XGBoost), and result generation — producing all outputs exactly as presented in the manuscript.
