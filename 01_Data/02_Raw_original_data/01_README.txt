######################################
###README for folder: 03_Raw_original_data###
######################################

This folder contains all raw datasets used in the current study, stored in their original form prior to any transformation or preprocessing. Each file is mapped to the variable(s) described in the 'data_description.qmd' file.

File List:

1. 02_6202004.xlsx  
   - Content: Monthly unemployment rate in New South Wales (Unwork_NSW)  
   - Source: Australian Bureau of Statistics  
   - Public access: Yes

2. 03_chart_20250721T044019.csv  
   - Content: Daily COMEX copper spot prices (Copper_Price)  
   - Source: Macrotrends  
   - Public access: Yes

3. 04_copper_theft_NSW.xlsx  
   - Content: Monthly traffic copper cable theft data (Cases)  
   - Source: Internal project data (non-public)  
   - Public access: No

4. 05_Incident_by_NSW.xlsx  
   - Content: Monthly total theft incidents in New South Wales (Total_Theft)  
   - Source: BOCSAR  
   - Public access: Yes

5. 06_Non_Ferrous_Metal_Import_Copper_Waste.xlsx  
   - Content: Monthly scrap copper imports to China (Scrap_Imports_CN)  
   - Source: CEIC Data Platform (GACC)  
   - Public access: Subscription required

Script Reference:
All data preprocessing and variable transformations are documented in the "02_Scripts/" directory.

Note:
Non-public datasets cannot be redistributed. However, all transformation steps are transparently recorded in script files to ensure full reproducibility.

Last updated: 23 July 2025
Maintainer: [Hongbo Zhao / Contact: hongbo.zhao@uqconnect.edu.au]
