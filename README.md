# Predicting Traffic Copper Cable Theft and Its Contributing Factors - A Reproducible Time-Series Modelling Approach


## Overview

This repository accompanies the research paper “Predicting Traffic Copper Cable Theft and Its Contributing Factors: A Reproducible Time-Series Modelling Approach”， which provides a fully reproducible analytical framework and all associated datasets and scripts.

The study focuses on traffic copper cable theft incidents in New South Wales, Australia (2010–2023), developing an integrated time-series modelling framework that combines econometric models (Log–log and ARIMAX) and a machine-learning model (XGBoost).  
It systematically analyses multiple explanatory factors, including copper price fluctuations, global scrap copper demand, unemployment rate, overall theft level, legislative interventions, and seasonal (monthly) variations, and compares the predictive performance and interpretability of different models.

Results show that copper price and overall theft level are long-term, stable external drivers of traffic copper cable theft. Legislative interventions temporarily reduce theft incidents but do not provide lasting deterrence.  
Seasonal effects are generally weak, with minor peaks observed in May and September. Overall, traffic copper cable theft exhibits low inertia but high responsiveness, driven primarily by immediate market conditions and broader crime dynamics.


## Key Contributions

The main contributions of this study are as follows:

- Research Extension: Expands metal theft research to the underexplored area of traffic infrastructure theft, jointly examining copper prices, global scrap demand, unemployment, overall theft levels, and seasonal patterns.  
- Methodological Innovation: Establishes a cross-method comparative framework integrating Log–log, ARIMAX, and XGBoost models, and introduces legislative variables to distinguish short-term and cumulative effects.  
- Reproducibility Framework: Implements a fully automated and reproducible workflow in R and Quarto, enhancing transparency and verifiability in transport crime analysis.


This repository releases all datasets, analysis scripts, and reproducible Quarto (.qmd) documents, supporting transparent and verifiable research and policy assessment.  
This README corresponds to the reproducibility repository for the paper submitted to European Transport Research Review.


## Repository Structure

The repository follows a four-layer reproducible research framework:  

├── 01_Data/        # Raw and processed datasets  
├── 02_Scripts/     # R scripts for model development (Log–log, ARIMAX, XGBoost)  
├── 03_Outputs/     # Figures and tables used in the manuscript  
├── 04_Manuscript/  # Reproducible manuscript (.qmd)  
└── Run_all.R       # Master script to execute the workflow  

This structure ensures transparency, traceability, and full reproducibility.


## Data Availability

All original datasets were obtained from the Bureau of Crime Statistics and Research (BOCSAR),  
New South Wales, Australia. Processed and anonymized datasets used in this study  
are provided within the repository under the `/01_Data/04_Processed_data/` directory.
