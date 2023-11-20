# FUN-BioCROP with LIDET Parameters

[![DOI](https://zenodo.org/badge/528962010.svg)](https://zenodo.org/badge/latestdoi/528962010)

 Version of FUN-BioCROP model (https://github.com/BrzostekEcologyLab/FUN-BioCROP) with LIDET-derived litter decomposition parameters

**Model name:** “FUNBioCROP_LIDET Study.Rmd”

**Creators:** Stephanie Juice, Joanna Ridgeway, Melannie Hartman, William Parton, Danielle Berardi, Benjamin Sulman, Kara Allen, Edward Brzostek

**Contact information:** stephanie.juice@mail.wvu.edu, erbrzostek@mix.wvu.edu 

**Software**: R

**Accompanying files**: 

1.    CORPSE function code: **CORPSE Functions_Bioenergy_V2.R**

2.    Data streams to load into the script: <br>
    a. **bulk.csv, bulk_till.csv, rhizo.csv, rhizo_till.csv, litter.csv**: initial C and N (kg C or N/m<sup>2</sup>) pool values for each soil compartment, final values from spin up. <br> 

All five files have the same columns:

| **Column**    | **Description**                       | **Units**                  |
| -------------- | ------------------------------------- | -------------------------- |
| uFastC         | Unprotected fast decomposing carbon   | kg  carbon/m<sup>2</sup>   |
| uSlowC         | Unprotected slow decomposing carbon   | kg  carbon/m<sup>2</sup>   |
| uNecroC        | Unprotected necromass carbon          | kg  carbon/m<sup>2</sup>   |
| pFastC         | Protected fast decomposing carbon     | kg  carbon/m<sup>2</sup>   |
| pSlowC         | Protected slow decomposing carbon     | kg  carbon/m<sup>2</sup>   |
| pNecroC        | Protected necromass carbon            | kg  carbon/m<sup>2</sup>   |
| livingMicrobeC | Carbon in living microbial biomass    | kg  carbon/m<sup>2</sup>   |
| uFastN         | Unprotected fast decomposing nitrogen | kg  nitrogen/m<sup>2</sup> |
| uSlowN         | Unprotected slow decomposing nitrogen | kg  nitrogen/m<sup>2</sup> |
| uNecroN        | Unprotected necromass nitrogen        | kg  nitrogen/m<sup>2</sup> |
| pFastN         | Protected fast decomposing nitrogen   | kg nitrogen/m<sup>2</sup>  |
| pSlowN         | Protected slow decomposing nitrogen   | kg  nitrogen/m<sup>2</sup> |
| pNecroN        | Protected necromass nitrogen          | kg  nitrogen/m<sup>2</sup> |
| inorganicN     | Inorganic nitrogen                    | kg  nitrogen/m<sup>2</sup> |
| CO2            | Carbon in carbon dioxide              | kg  carbon/m<sup>2</sup>   |
| livingMicrobeN | Nitrogen in living microbial biomass  | kg  nitrogen/m<sup>2</sup> |

 

​	b.    **FluxTower_AvgSoilT.csv**: Average daily soil temperature (<sup>o</sup>C) at 10 cm depth at University of Illinois Urbana-Champaign (UIUC) Energy Farm flux tower from 7/2008-3/2016. (One year of averaged data)

​	c.    **FluxTower_AvgSoilVWC.csv**: Average daily soil volumetric water content (VWC) at 10 cm depth at UIUC Energy Farm flux tower from 7/2008-3/2016. (One year of averaged data)

​	d.   **input_CCS_LIDET Study.csv**: This file has daily data to run FUN-BioCROP: 

| **Column**           | **Description**                                              | **Units**              |
| -------------------- | ------------------------------------------------------------ | ---------------------- |
| yr                   | calendar year                                                | year                   |
| doy                  | day of year (1 to 365) (no leap year)                        | day                    |
| anpp                 | aboveground NPP (DayCent)                                    | kg C/m<sup>2</sup>/day |
| bnpp                 | belowground NPP (DayCent)                                    | kg C/m<sup>2</sup>/day |
| aglivc               | live aboveground biomass carbon (DayCent)                    | kg C/m<sup>2</sup>     |
| bglivcj              | live juvenile fine root biomass carbon (DayCent)             | kg C/m<sup>2</sup>     |
| bglivcm              | live mature fine root biomass carbon (DayCent)               | kg C/m<sup>2</sup>     |
| aglivn               | live aboveground biomass nitrogen (DayCent)                  | kg N/m<sup>2</sup>     |
| bglivnj              | live juvenile fine root biomass nitrogen (DayCent)           | kg N/m<sup>2</sup>     |
| bglivnm              | live mature fine root biomass nitrogen (DayCent)             | kg N/m<sup>2</sup>     |
| nyr                  | simulation year                                              | year                   |
| cult                 | indicates a cultivation event (0 or 1)                       |                        |
| crop                 | indicates a new crop (0 or 1)                                |                        |
| fert                 | indicates a fertilizer event (0 or 1)                        |                        |
| frst                 | indicates the first day of the growing season (0 or 1)       |                        |
| harv                 | indicates a harvest event (0 or 1)                           |                        |
| last                 | indicates the end of the growing season (0 or 1)             |                        |
| croptype             | crop type (0=none; 1=alfalfa; 2=corn; 3=grass clover pasture; 4=soybean; 5=wheat) |                        |
| cropsrl              | crop specific root length                                    | mm/g root              |
| cultrhizmix          | fraction of rhizosphere mixed with bulk soil during cultivation (0.0-1.0) | fraction               |
| cultlitmix           | fraction of litter mixed with bulk soil during cultivation (0.0-1.0) | fraction               |
| harvremov            | fraction of above ground biomass removed during harvest (0.0-1.0) | fraction               |
| fertamt              | fertilization amount                                         | g N/m<sup>2</sup>      |
| lifehist             | plant life history (0 = annual, 1 = perennial)               |                        |
| froot_turnover_c     | amount of C in fine root turnover                            | kg C/m<sup>2</sup>     |
| froot_turnover_n     | amount of N in fine root turnover                            | kg N/m<sup>2</sup>     |
| agrd_turnover_c      | amount of C in aboveground biomass turnover                  | kg C/m<sup>2</sup>     |
| agrd_turnover_n      | amount of N in aboveground biomass turnover                  | kg N/m<sup>2</sup>     |
| leaf_litter_fastfrac | Fast decomposing fraction of leaf litter (0.0-1.0)           | fraction               |
| root_litter_fastfrac | Fast decomposing fraction of root litter (0.0-1.0)           | fraction               |
| root_diameter        | root diameter                                                | mm                     |
| root_length          | root length                                                  | mm root/m<sup>2</sup>  |
| rhizo_frac           | fraction of total soil volume that is rhizosphere (0.0 - 1.0) | fraction               |
| date                 | date in format YYYY-MM-DD                                    |                        |

  

**Instructions:** 

1) Save the model code (“FUN-BioCROP_LIDET Study.Rmd”) and accompanything files (data streams and CORPSE function code) in the same folder. 

2) In “Chunk 3: Load CORPSE Data Streams” set the working directory (setwd) to the folder with the files saved in step #1.

3) In "Chunk 5: Define LIDET parameter sets" select the litter decomposition parameter set to be used in the run, and comment out all other sets.
   
5) If changing any parameter values, edit them in “Chunk 6: Load parameters.” 

6) Run all chunks up to and including “Chunk 10: Prepare Data for Export.”

7) In “Chunk 11: Export Output Data” edit data frames for export and filenames, as necessary. 

8) “Chunk 12: Graph Total Soil C” makes a figure of C remaining over the model run period.

**Description:** 

This model is a reparameterized version of the original FUN-BioCROP model (Fixation and Uptake of Nitrogen-Bioenergy Carbon, Rhizosphere, Organisms, and Protection, https://github.com/BrzostekEcologyLab/FUN-BioCROP). Leaf litter decomposition in the litter compartment was reparameterized using the Long-term Inter-site Decomposition Experiment Team dataset (LIDET) and a modified Monte Carlo simulation. 

**Description of each chunk:** 

1. **Chunk 1: Remove all functions, clear memory.** Removes all functions from R environment, clears the memory. 

2. **Chunk 2: Load Packages.** Loads packages necessary to run the code. 

3. **Chunk 3: Load CORPSE Data Streams.** Sets the working directory and loads the data files necessary to run CORPSE.

4. **Chunk 4: Load CORPSE Functions.** Loads the R script with CORPSE functions from the working directory, “CORPSE Functions_Bioenergy_V2.R”.

5. **Chunk 5: Define LIDET parameter sets.** Has ten different parameter sets for litter decomposition tested in this study: Baseline parameters, LIDET parameters, and the other 8 best performing parameter sets identified in the modified Monte Carlo. To run the model, all but one parameter set must be commented out. 
    
7. **Chunk 6: Load Parameters.** Loads all fixed parameters to run the model. Data frame with definitions of parameters is in the CORPSE function script “CORPSE Functions_Bioenergy_V2.R”

8. **Chunk 7: Prepare Data Streams.** Takes data streams loaded in Chunk 3 and puts them in the format necessary to run the model. The model is coded to run at least two sites at a time, so if only one site is being run it must be run in duplicate. Individual data tables of daily values are created in this chunk from the input data file.

9. **Chunk 8: Set Initial Conditions.** Creates data tables of soil C and N pools for each soil compartment (rhizo_till, rhizo, bulk_till, bulk, litter) and loads initial values into the data tables. Creates lists for each soil compartment to hold model output. 

10. **Chunk 9: Load FUN Data and Set Up Matrices.** Uses DayCent data to calculate FUN input data: root and leaf N demand, total N demand, plant CN, leaf N available for retranslocation, and litter production. Creates matrices for FUN model outputs. 

11. **Chunk 10: Run Model.** Runs the model. 

12. **Chunk 11: Prepare Data for Export.** Combines data from each day saved as lists into data frames for each soil compartment. Adds values from all soil compartments together to calculate total soil values, creates separate data frames for each soil C and N pool (e.g., protected slow C) for the total soil value. Adds different C and N pools together to calculate total soil C and N for all layers. Creates data frame of ratio of protected to unprotected SOC. Organizes FUN data for export. 

13. **Chunk 12: Export Results.** Exports CSV files of model results to the working directory. 

14. **Chunk 13: Graph Total Soil C.** Makes figure of C remaining over time. 

    

**Related Links:**

Original FUN-BioCROP model: https://github.com/BrzostekEcologyLab/FUN-BioCROP <br>
LIDET dataset: https://andlter.forestry.oregonstate.edu/data/abstract.aspx?dbcode=TD023
