Title： Traffic Copper Theft – Reproducible Analysis

This repository provides a fully reproducible research framework for analyzing traffic copper cable theft in New South Wales (NSW), Australia. The study focuses on the influence of copper prices, scrap metal imports, unemployment, and legislation on theft incidents. The analysis includes ARIMAX, log-log regression, and XGBoost models.

Repository Structure
01_Data/: Raw and processed data files
02_Scripts/: Scripts for data processing and modeling. All scripts must be executed sequentially in the numbered order. Skipping any script may result in execution errors or missing dependencies.
03_Outputs/: Model outputs including plots and summary tables
04_Manuscript/: Final manuscript source files (Quarto format)

Quick Execution: Run_all.R
To streamline the analysis process, this repository includes a Run_all.R file, which automatically sources all key scripts in sequence—from data preprocessing to model fitting. It is recommended to open the Github.Rproj project file in RStudio and execute Run_all.R for a complete, end-to-end reproducible workflow. Please, make sure all required packages are installed and that Quarto is properly configured to render .qmd files.

Software Requirements
R version: 4.x or later
Quarto version: 1.4 or later

Required R packages are listed in:
02_Scripts/02_Required_Packages_and_Setup/02_Required_packages_and_setup.qmd
