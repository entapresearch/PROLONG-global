# PROLONG-global
Code and data for the article Jakhmola A., Jewell J., Vinichenko V., Cherp A. (2026). Probabilistic projections of global wind and solar power growth based on historical national experience. 

The projections generated in this article can be explored using an interactive web app: https://entap.net/prolong-interactive/

### Notes
* Each R file provided can run standalone, provided that the working directory is set to the folder containing the supplementary files. 
* Each R script is designed to handle all package dependencies, load the data, and run the analysis pipeline.  
* A working internet connection is required to ensure all necessary packages can be properly loaded. 
* All data required for running the provided code can be found in /data/input.
* Further information about the code pipeline is available within each script. 
* The wind_model_training and solar_model_training scripts are computationally intensive and take several hours to run with the default settings (2-4 hours each on a MacBook Pro with an M1 Pro chip and 16GB RAM). It is recommended to first test the code with a reduced number of runs. 
* All other scripts have expected runtimes under 10 minutes each on "normal" desktop computers. This includes installation time for necessary packages. 
* The analysis was run on a MacBook Pro 16" with an M1 Pro chip and 16GB RAM using R version 4.5.0 (2025-04-11). No additional hardware was used. 
* The code was tested on macOS 14 Sonoma, macOS 15.4.1 Sequoia, and macOS 26.2 Tahoe.  



## R code files

**PROLONG_v2.R** - source code for PROLONG, the modelling framework introduced in this article;

**wind_model_training** – code for applying PROLONG to onshore wind;

**solar_model_training** – code for applying PROLONG to solar PV;

**fitting_functions.R** – code for fitting growth curves to empirical deployment data - originally developed in Cherp et al. (2021);

**national_takeoff_and_growth_analysis.R** – code for identifying takeoff and fitting growth curves to technology deployment data;

**regional_allocation_algorithm.R** – code for allocating growth in our stylised counterfactual scenarios to different world regions;

**regional_scenarios_wind.R** – code for deriving regionally-differentiated deployment trajectories for onshore wind (also used for Extended Data Figure 9);

**regional_scenarios_solar.R** – code for deriving regionally-differentiated deployment trajectories for solar PV (also used for Extended Data Figure 9);

**figure2.R** – code for producing an illustration of different growth patterns for onshore wind and solar PV (replication of Figure 2);

**figure4.R** – code for hindcasting projections made using PROLONG and other projections (replication of Figure 4);

**figure5.R** – code for plotting projections made using PROLONG, counterfactual scenarios and IPCC AR6 scenario summaries (replication of Figure 5, and Extended Data Figure 8);

**figure_ed1.R** – code for plotting global and national takeoff thresholds for onshore wind, solar PV, CCGTs and mobiles (replication of Extended Data Figure 1);

**figure_ed2.R** – code for plotting the diffusion of technologies across countries and growth phases (replication of Extended Data Figure 2);

**figure_ed7.R** – code for hindcasting projections made using PROLONG from 2014 and 2018 against IPCC AR5 and SR1.5°C scenarios (replication of Extended Data Figure 7);

**hindcasting_different_models.R** – code for hindcasting using PROLONG and other data-driven models and plotting projection performance vis-a-vis out-of-sample empirical data (replication of Extended Data Figure 6, Supplementary Figure 6);

**figure_sup5.R** – code for hindcasting using different PROLONG model variants and plotting projection performance vis-a-vis out-of-sample empirical data (replication of Supplementary Figure 5);

**figure_sup7.R** – code for plotting the projections from hindcasting using PROLONG and a bottom-up approach aggregating logistic extrapolations for individual countries (replication of Supplementary Figure 7);

**hindcasting_out_of_sample_simulations.R** – code for hindcasting using PROLONG and plotting projection performance vis-a-vis out-of-sample, simulated test data (replication of Supplementary Figures 3 and 4);

**uncertainity_quantification.R** – code for hindcasting and uncertainty quantification for PROLONG (replication of Supplementary Figure 8);

**other_data_driven_projections.R** – code for making projections using other data-driven methods




## Data files

**f2_XXX.csv** – source data for Figure 2;

**f4_XXX.csv** – source data for Figure 4;

**f5_XXX.csv** – source data for Figure 5;

**ed1_XXX.csv** – source data for Extended Data Figure 1;

**ed2_XXX.csv** – source data for Extended Data Figure 2;

**ed7_XXX.csv** – source data for Extended Data Figure 7;

**sf5_XXX.csv** – source data for Supplementary Figure 5;

**sf7_XXX.csv** – source data for Supplementary Figure 7;

**counterfactual_trajectories_w_baseline.csv** – time series with Early and Late acceleration scenarios for onshore wind and solar PV plus the Baseline scenarios;

**error_analysis_data.csv** – time series with projections from different data-driven models and empirical values used for projection performance analysis;

**simulated_out_of_sample_test_data.csv** – simulated time series used for PROLONG projection performance analysis;

**global_electricity.csv** – time series for global electricity generation; 

**national_electricity.csv** – time series for national electricity generation;

**global_onshore_wind.csv**  –  time series for global onshore wind generation; 

**global_solarpv.csv** – time series for global solar PV generation; 

**national_onshore_wind.csv**  –  time series for national onshore wind generation;

**national_solarpv.csv** – time series for national solar PV generation; 

**national_solar_parameters_share.csv** – parameters for growth parameters fit to systematically curtailed national solar PV deployment data;

**national_onwind_parameters_share.csv** – parameters for growth parameters fit to systematically curtailed national onshore wind deployment data;

**regional_classification.csv** – classification of countries into 10 world regions based on the IPCC’s classification

**on_wind_historical_by_region_agg.csv** – time series for region-wise historical onshore wind deployment ;

**on_wind_historical_by_region_disagg.csv** –  time series for region-wise historical onshore wind deployment with each region disaggregated into constituent countries;

**on_wind_initialisation.csv** – initialisation data for calculating regional onshore wind growth in the counterfactual scenarios; 

**solarpv_historical_by_region_agg.csv** – time series for region-wise historical solar PV deployment; 

**solarpv_historical_by_region_disagg.csv** –  time series for region-wise historical solar PV deployment with each region disaggregated into constituent countries;

 **solarpv_initialisation.csv** – initialisation data for calculating regional solar PV growth in the counterfactual scenarios 
 

