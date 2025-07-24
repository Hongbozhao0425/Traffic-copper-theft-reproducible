####################################################
###Supplementary Outputs for Traffic Copper Cable Theft Analysis###
####################################################
This folder contains all supplementary figures and tables used in the paper. Each item is numbered and briefly described below to enhance transparency and reproducibility.

###########################
###1. Variable Selection Output###
###########################
Figure 01 – Granger_Heatmap_600dpi.tiff: 
Heatmap illustrating the results of pairwise Granger causality tests across all candidate predictors. This output was used to identify significant lagged variables for further modeling.

##########################
###2. Model Prediction Results###
##########################
(1): Figure 02 – Log_Log_Predicted_vs_Actual_Cases.tiff
(2): Figure 03 – ARIMAX_Predicted_vs_Actual_Cases.tiff
(3): Figure 04 – XGBoost_Predicted_vs_Actual_Cases.png
Comparisons of model-predicted values versus actual copper cable theft cases across quarters. All predictions were generated on the test set (2021 Q1 to 2023 Q2).

##################################
###3. Residual Diagnostics (ACF and PACF)###
##################################
(1): Figures 05–06 – ACF and PACF of Log-Log Model Residuals
(2): Figures 07–08 – ACF and PACF of ARIMAX Model Residuals
(3): Figures 09–10 – ACF and PACF of XGBoost Model Residuals
These plots assess whether residuals exhibit temporal autocorrelation. The Log-Log model shows statistically significant autocorrelation at multiple lags, indicating potential model misspecification. In contrast, the ARIMAX and XGBoost models exhibit no significant autocorrelation at the 5% level, supporting the assumption of residual independence.

#######################################
###4. Feature Importance and Model Explanation###
#######################################
(1): Figure 11 – XGBoost_SHAP_Feature_Importance_Percentage.png:
SHAP summary plot illustrating the relative contribution of each feature to the XGBoost model output. 
(2: )Figure 12 – XGBoost_Variable_Impact_Table.png
Table summarizing the changes in model accuracy metrics (MAPE, RMSE, R²) when each key variable is removed. This supports variable importance analysis through performance degradation.

##########################
###5. Model Coefficient Tables###
##########################
(1): Figure 13 – Log_Log_Coefficient_Table.png
(2): Figure 14 – ARIMAX_Coefficient_Table.png
Estimated coefficients, standard errors, and statistical significance levels for the two primary models. The intervention dummy, copper price (lag 1), and total theft rate (lag 1) were consistently significant in both models, confirming their robust associations with traffic copper cable theft.