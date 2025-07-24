######################################
###README for folder: 03_Raw_original_data###
######################################
This folder contains all raw datasets used in the study, each stored in its original format prior to any transformation. These files serve as the foundation for all model inputs. Following a series of preprocessing steps—such as filtering, reshaping, interpolation, and temporal alignment—all variables were cleaned and standardized before being merged into a single consolidated dataset. This integrated dataset is saved in "02_Processed_data.xlsx" under the directory "02_Scripts/02_Processed_data/", and serves as the final input for subsequent modeling and analysis. A summary of each raw file and its corresponding derived variables is provided below.

##################
###02_6202004.xlsx###  
##################
- Variable: Unwork_NSW (Unemployment rate in New South Wales)  
- Source: Australian Bureau of Statistics (ABS)  
- Frequency: Monthly  
- Time range: Feb 1978 – Jan 2025  
- Access: Public  
- Notes: Processed using columns from the “Data1” sheet, specifically column "AW"; dates parsed from Excel numeric format. See related script in `02_Scripts`.

##############################
###03_chart_20250721T044019.csv  ###
##############################
- Variable: Copper_price (Monthly median COMEX copper spot price)  
- Source: Macrotrends  
- Frequency: Daily → aggregated to monthly  
- Time range used: Jan 2010 – Jun 2023  
- Access: Public  
- Notes: Parsed from raw daily data, grouped and summarized by monthly median. See `02_Scripts`.


###########################
###04_copper_theft_NSW.xlsx ###
########################### 
- Variables:
  - cases (Copper_Theft_Traffic_NSW)
  - intervention (legislation dummy)
  - t_since (months since intervention)
  - total_t (global time index)  
- Source: Internal project dataset (non-public)  
- Frequency: Monthly  
- Time range: Jan 2010 – Jun 2023  
- Access: Restricted  
- Notes: Not publicly available.


#########################
###05_Incident_by_NSW.xlsx###
#########################  
- Variable: Total_theft (Total recorded theft incidents in NSW)  
- Source: Bureau of Crime Statistics and Research (BOCSAR)  
- Frequency: Monthly  
- Time range: Jan 1995 – Mar 2025  
- Access: Public  
- Notes: Filtered by selected subcategories, pivoted into long format and aggregated monthly.


############################################
###06_Non_Ferrous_Metal_Import_Copper_Waste.xlsx### 
############################################
- Variable: Scrap_Imports_CN (China’s imported copper scrap volume)  
- Source: CEIC (via General Administration of Customs of China)  
- Frequency: Monthly  
- Time range used: Jan 2010 – Jun 2023  
- Access: Subscription required  
- Notes: Parsed from numeric Excel format, filtered and cleaned. 


Script Reference:
All preprocessing and transformation workflows are implemented in the `02_Scripts` directory, following the reproducibility standard. Merged output is saved in `02_Processed_data.xlsx`.


Last updated: 23 July 2025
Maintainer: [Hongbo Zhao / Contact: hongbo.zhao@uqconnect.edu.au]
