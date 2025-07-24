#########################################
###Data Structure and Reproducibility Statement###
#########################################

#####################
###1. Project Overview###
#####################
This study investigates the determinants of traffic-related copper cable theft in New South Wales, Australia, with a focus on copper price fluctuations, scrap copper imports, unemployment rates, and general property crime trends. All data used for model estimation have been carefully documented, preprocessed, and merged, ensuring full reproducibility of the analysis.


####################
###2. Folder Structure###
####################
01_README/: This folder. Contains an overview of the data structure and usage guidance.
02_Data_description/: Detailed descriptions of each variable, including source URLs, units, data collection methods, download paths, and preprocessing instructions.
03_Raw_original_data/: Raw datasets, downloaded manually from platforms such as CEIC, BOCSAR, and ABS. No modifications were applied.
04_Processed_data/: Preprocessed and merged datasets used for model estimation. Includes the main file "02_Processed_data.xlsx".


##################################
###3. Reproducibility of Data Processing###
##################################
All raw datasets were manually downloaded and stored in the "03_Raw_original_data/" folder. R programming language was used to clean, reformat, and align the datasets over time. These were subsequently merged into a unified panel dataset stored in "04_Processed_data/".

The preprocessing steps include:
(1) Copper Price: Time alignment and extraction of monthly median values
(2) Scrap Copper Imports: Time alignment and data format conversion
(3) Unemployment Rate: Time alignment and value transformation
(4) Theft Rates: Subcategory filtering and time alignment
(5) Copper Cable Theft: Unified date formatting and used as the main dataset to join all other variables via left joins

The final combined_data is clean, chronologically aligned, and contains no missing values, making it suitable for time series modeling and regression analysis.

##########################
###4. Maintainer Information###
##########################
Maintainer: Hongbo Zhao
Contact: hongbo.zhao@uqconnect.edu.au
Last Updated: 23 July 2025