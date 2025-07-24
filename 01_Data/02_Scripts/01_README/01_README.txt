######################################################################
# Project Title: Predictive and Explanatory Modeling of Traffic-Related Copper Cable Theft#
######################################################################

#####################
###1. Project Overview###
#####################
This project aims to construct and compare three predictive models—log-log regression, ARIMAX, and XGBoost—to examine the explanatory power of multiple external variables on traffic-related copper cable theft in New South Wales, Australia. All data processing, modeling, and output procedures strictly adhere to reproducibility principles and are fully executable within the R environment.

##########################
###2. How to Run the Project###
##########################
Open the main project file using RStudio:Github.Rproj
Either execute each script sequentially by folder order or run the unified execution script located in the 05_Run_all_R folder for one-click reproducibility (recommended after debugging).

############################
###3. Project Directory Structure###
############################
"01_README/": Contains project documentation (i.e., this README file) and references.
"02_Required_Packages_and_Setup/": Scripts for automated installation and loading of required R packages, and path setup.
"03_Data_preprocessing/": Includes scripts for raw data cleaning, variable construction, and preprocessing. Outputs are structured for direct modeling.
"04_Granger_test/": Implements Granger causality testing to pre-select explanatory variables for modeling.
"05_Log_Log_model/": Constructs a log-log regression model to estimate elasticity between theft cases and predictors. Includes prediction plots and error metrics.
"06_ARIMAX_model/": Builds an ARIMAX time series model incorporating exogenous variables. Outputs include fitted trends and residual diagnostics.
"07_XG_Boost_model/": Implements an XGBoost machine learning model and applies SHAP values for interpretable analysis of variable importance and non-linear effects.

####################
###5. Modeling Logic###
####################
The three models are developed as parallel modeling strategies rather than sequential pipelines. Each model uses the same set of Granger-selected lagged variables and independently performs forecasting and interpretation. Key design principles include:
(1): Granger causality pre-selection is used across all models to identify statistically relevant lagged predictors.
(2): Each model operates independently and outputs its own performance metrics and plots.
(3): Final model comparison is based on predictive accuracy (e.g., RMSE, MAPE) and interpretability (e.g., coefficient analysis, SHAP values), facilitating robust model evaluation and variable selection.

############################
###6. Reproducibility Statement###
############################
This project is fully reproducible. It provides:
(1): Code-based preprocessing workflows for all data;
(2): Complete scripts for variable transformation, lagging, and modeling;
(3:) Documented modeling parameters and outputs;
(4): Reproducible visualizations and statistical summaries.
All scripts are self-contained, version-controlled, and ready for peer verification in open scientific workflows.

