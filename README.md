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

2. Extra_Islands.csv
    * For most of the L3 and L4 regions included in December_Database_Backup.csv, we used the "island" or "not island" labels used by GloNAF. The L3 and L4 regions in this file are not included in GloNAF, so we assigned these "island"/"not island" labels manually based on individual searches of each location. 
    * In the "island" column, 1 = island and 0 = not island. 

3. January_Climate_Overlaps_Removed_Backup.csv
    * This is an edited version of December_Database_Backup that we used only for the climate analyses.  
    * See Final_Climates.Rmd file below to see the steps that created this file. 

4. L3_Better_Climate_data.csv
    * Using shapefiles from the WGSRPD GitHub (see link above) and the climate map from Kottek et al. 2006 (see manuscript for full citation), we calculated the most common Köppen climate within each L3 region.
    * Numbers in "MAJORITY" column correspond to the following Köppen climates: 1 = Af, 2 = Am, 3 = As, 4 = Aw, 5 = BWk, 6 = BWh, 7 = BSk, 8 = BSh, 9 = Cfa, 10 = Cfb, 11= Cfc, 12 = Csa, 13 = Csb, 14 = Csc, 15 = Cwa, 16 = Cwb, 17 = Cwc, 18 = Dfa, 19 = Dfb, 20 = Dfc, 21 = Dfd, 22 = Dsa, 23 = Dsb, 24 = Dsc, 25 = Dsd, 26 = Dwa, 27 = Dwb, 28 = Dwc, 29 = Dwd, 30 = EF, 31 = ET, 32 = Ocean/Water.

5. L4_Better_Climate_data.csv
    * Same as L3_Better_Climate_Data.csv except for L4 regions instead of L3 regions. 



<br/><br/>
__R Code Files:__ 

