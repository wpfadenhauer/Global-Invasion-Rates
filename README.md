# Twenties Rule

The following files include the raw data and R code used in the "Twenties Rule" manuscript (URL/DOI to be updated once manuscript is published). 
Please reach out if you have any questions about content or organization in this repo. 

<br/><br/>
__Raw Data Files:__
1. December_Database_Backup.csv 
    * This is the main database. Includes species names, invasion status (established or invasive), Native L1-L4 regions, Established L1-L4 regions, and Invasive L1-L4 regions for each species.
    * Species names are standardized using WCVP through the TNRS R package. 
    * Invasion status is based on whether we found evidence of negative impacts for that species in at least one location. If the species has negative impacts anywhere, it is listed as invasive, otherwise it is established. See Supplemental Methdos in manuscript for data sources and collection methods. 
    * The following columns will be empty for all established species: Invasive_L1, Invasive_L2, Invasive L3, Invasive L4. 
    * L1, L2, L3, and L4 codes are from WGSRPD. See their GitHub (https://github.com/tdwg/wgsrpd) and Wikipedia (https://en.wikipedia.org/wiki/List_of_codes_used_in_the_World_Geographical_Scheme_for_Recording_Plant_Distributions) for more information. 
    * Plant records at finer spatial scales have been converted to their corresponding coarser scales for completeness. For example, species reported as invasive in the state of Massachusetts, U.S.A. (column Invasive_L3 = MAS) were also recorded as invasive in the Northeastern U.S.A. (column Invasive_L2 = 75) and Northern America (column Invasive_L1 = 7). 
    * Since some data was only available at the country or continental level, our this database includes the most information at the L1 (continental) scale and the least information at the L4 (province/state) scale. 



<br/><br/>
__R Code Files:__ 

