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



## Data

This repository includes all datasets used in the study, covering economic, legislative, and crime-related indicators for **New South Wales, Australia (2010–2023)**.

- **Traffic Copper Cable Theft:** Dataset provided and compiled by *Professor Zuduo Zheng’s research group* at *The University of Queensland*. Included in this repository with permission for research reproducibility.  
- **Overall Theft in NSW:** Monthly property crime index from the *NSW Bureau of Crime Statistics and Research (BOCSAR)*.  
- **Unemployment Rate:** Monthly unemployment rate (%) from the *Australian Bureau of Statistics (ABS)*.  
- **Global Copper Price:** Monthly median COMEX spot prices from *Macrotrends*.  
- **China’s Scrap Copper Imports:** Monthly import volumes (thousand tonnes) from *CEIC Database*.  
- **Legislative, Seasonal, and Lag Variables:** Internally generated for model analysis.

Detailed variable definitions and preprocessing notes are available in `/01_Data/01_Data_description/`.



## Analysis and Results

This section presents the main results obtained from the R-based analyses described in the manuscript. All **figures** were generated directly from the analytical outputs of the R scripts,  while the **data tables** were programmatically derived and manually formatted for clarity. To ensure transparency and traceability of all numerical values, each data table in the final **Reproducible Manuscript** includes the corresponding R code embedded right below the table.  By running these embedded code blocks, readers can directly reproduce the values shown in each table.

The results below are provided to illustrate the outputs produced by the reproducible scripts，detailed interpretation and discussion can be found in the main manuscript.  


### 1. Model Assumption Tests

All three models (**Log–log**, **ARIMAX(1,0,1)**, and **XGBoost**) satisfy the key assumptions of residual normality, homoscedasticity, and stationarity. The Log–log model shows slight autocorrelation (Box–Ljung *p* = 6.65×10⁻¹³), which was corrected using Newey–West robust standard errors.
<img width="865" height="396" alt="image" src="https://github.com/user-attachments/assets/de455398-f941-417f-a0e3-0013643209ce" />


### 2. Predictive Performance

All models perform significantly better than the naïve lag baseline (MASE < 1). The **Log–log model** achieves the best overall error control, the **ARIMAX** model captures short-term fluctuations more effectively, and **XGBoost** provides better interpretability through feature importance measures.
<img width="865" height="266" alt="image" src="https://github.com/user-attachments/assets/16d94597-f537-49b2-9091-2715cabfa827" />

<img width="859" height="527" alt="image" src="https://github.com/user-attachments/assets/06814f7f-0104-4e49-9af6-ed17f2e5c77b" />


### 3. Key Factor Analysis

Cross-model comparisons indicate that:
- **Copper price** and **overall theft level** are persistent long-term positive drivers;
- **Legislative interventions** temporarily suppress theft incidents but show no cumulative deterrent effect;
- **Unemployment rate** and **China’s scrap copper imports** show limited statistical significance;
- **Seasonal effects** are minor, with small peaks observed in **May** and **September**.
<img width="864" height="298" alt="image" src="https://github.com/user-attachments/assets/3d0236cc-c1ca-4ffe-b3eb-4037345f0175" />


### 4. Summary

Overall, traffic copper cable theft in New South Wales exhibits **low inertia but high responsiveness**, primarily driven by short-term market dynamics and broader crime trends. These outputs provide a baseline reference for reproducibility validation and serve as benchmarks for future model extensions or comparative studies.



## Repository Structure

The repository follows a four-layer reproducible research framework:  

├── 01_Data/         Raw and processed datasets  
├── 02_Scripts/      R scripts for model development (Log–log, ARIMAX, XGBoost)  
├── 03_Outputs/      Figures and tables used in the manuscript  
├── 04_Manuscript/   Reproducible manuscript (.qmd)  
└── Run_all.R/        Master script to execute the workflow  

This repository releases all datasets, analysis scripts, and reproducible Quarto (.qmd) documents, supporting transparent and verifiable research and policy assessment.  


## Reproducibility and Execution (还需要补全一个R studio的版本)

（待定）


## 8. Citation

If you wish to cite this repository, please use the following **temporary citation format** (to be updated upon journal publication):

> Anonymous. (2025). Predicting Traffic Copper Cable Theft and Its Contributing Factors: A Reproducible Time-Series Modelling Approach. 
> Manuscript submitted for publication.  
> Available at: [GitHub Repository]([https://github.com/Hongbozhao0425/Traffic-copper-theft-reproducible]

## 9. License

This project is distributed under the **MIT License**, allowing free use, modification, and redistribution for academic and educational purposes. Users must retain the original author attribution and license statement in any derivative works. For full license details, please see the [`LICENSE`](./LICENSE) file.


## 10. Contact

For questions regarding the dataset, code, or reproducibility, please contact:

**Hongbo Zhao**  
*The University of Queensland*  
📧 [hongbo.zhao@uqconnect.edu.au](mailto:hongbo.zhao@uqconnect.edu.au)  
