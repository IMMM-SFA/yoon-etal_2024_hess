_your zenodo badge here_

# yoon-etal_2021_natsustain

**Farmer cropping adaptation alleviates simulated water shortage in the United States**

Jim Yoon<sup>1\*</sup>, Nathalie Voisin<sup>1</sup>, Christian Klassert<sup>1</sup>, Travis Thurber<sup>1</sup>, Wenwei Xu<sup>1</sup>

<sup>1 </sup> Pacific Northwest National Laboratory, Richland, WA., USA

\* corresponding author:  jim.yoon@pnnl.gov

## Abstract
Threats to water security are a paramount global concern, largely driven by human pressures on scarce water resources. The irrigation of croplands, which accounts for the lion’s share of human water consumption, is critical in understanding water security trajectories. Despite irrigation’s defining role, large-scale water security modeling frameworks typically impose trajectories of land use that underlie irrigation demand, neglecting dynamic feedbacks in the form of human instigation of and subsequent adaptation to water scarcity via irrigated cropping changes. We introduce a large-scale, multi-agent hydroeconomic model applied to the United States to evaluate water shortage outcomes that emerge from the interplay between hydrologic-driven water availability, reservoir management, and farmer cropping adaptation. Farmer cropping adaptivity is specified using a positive economic approach calibrated to observed data. Comparative experiments reveal that neglecting farmer cropping adaptation leads to pronounced overestimation of water shortages, with adaptation alleviating U.S.-wide annual water shortage by as much as 58 percent in a numerical experiment that mimics U.S. hydrology from 1950-2009.

## Journal reference
TBD

## Data reference

### Input data
1. Heimlich, Ralph. USDA Agricultural Information Bulletin No. (AIB-760) 2 pp. (2000). Farm Resource Regions [Online]. Available at https://www.ers.usda.gov/publications/pub-details/?pubid=42299 (accessed 2021-04-12; verified 2021-04-12). USDA-NASS, Washington, DC.
2. USDA 2012 Census of Agriculture. (2013 and 2008). Table 4. Estimated Quantity of Water Applied By Source [Online]. Available at https://www.nass.usda.gov/Publications/AgCensus/2012/Online_Resources/Farm_and_Ranch_Irrigation_Survey/fris13_1_004_004.pdf (accessed 2021-04-12; verified 2021-04-12). USDA-NASS, Washington, DC.
3. USDA 2012 Census of Agriculture. (2013 and 2008). Table 12. On-Farm Energy Expense for Pumping Irrigation Water by Water Source and Type of Energy [Online]. Available at https://www.nass.usda.gov/Publications/AgCensus/2012/Online_Resources/Farm_and_Ranch_Irrigation_Survey/fris13_1_012_012.pdf (accessed 2021-04-12; verified 2021-04-12). USDA-NASS, Washington, DC.
4. USDA 2012 Census of Agriculture. (2013 and 2008). Table 35. Crops Harvested in the Open from Irrigated Farms [Online]. Available at https://www.nass.usda.gov/Publications/AgCensus/2012/Online_Resources/Farm_and_Ranch_Irrigation_Survey/fris13_2_035_035.pdf (accessed 2021-04-12; verified 2021-04-12). USDA-NASS, Washington, DC.
5. USDA 2012 Census of Agriculture. (2013 and 2008). Table 36. Estimated Quantity of Water Applied and Primary Method of Distribution by Selected Crops Harvested in the Open [Online]. Available at https://www.nass.usda.gov/Publications/AgCensus/2012/Online_Resources/Farm_and_Ranch_Irrigation_Survey/fris13_2_036_036.pdf (accessed 2021-04-12; verified 2021-04-12). USDA-NASS, Washington, DC.
6. USDA Economic Research Service using data from USDA’s Agricultural Resource Management Survey (ARMS) and other sources. (1995-2017). Published Commodity Costs and Returns [Online]. Available at https://www.ers.usda.gov/data-products/commodity-costs-and-returns/commodity-costs-and-returns (accessed 2021-05-12; verified 2021-05-12). USDA-NASS, Washington, DC
7. USDA National Agricultural Statistics Service Cropland Data Layer. (2008-2018). Published crop-specific data layer [Online]. Available at https://nassgeodata.gmu.edu/CropScape/ (accessed 2021-04-05; verified 2021-04-05). USDA-NASS, Washington, DC.
8. Voisin, N. et al. (2018). MOSART-WM-ABM Input Data. [Data set]. Zenodo. https://doi.org/10.5281/zenodo.4836886.

### Output data
9. Yoon, Jim et al. (2021). Supporting data for Yoon et al. 2021 - Nature Sustainability. [Data set]. Zenodo. https://doi.org/10.5281/zenodo.5573041.

## Code reference
10. Yoon, Jim. (2021, TBD). IMMM-SFA/wm-abm_pmp: Water Management Agent Based Model (v1.0.0). Zenodo. http://doi.org/10.5281/zenodo.5570864.
11. Yoon, Jim, & Thurber, Travis. (2021, May 5). IMMM-SFA/iwmm: MOSART-WM-ABM (Version v1.1.2.abm). Zenodo. http://doi.org/10.5281/zenodo.4739516.
12. Yoon, Jim. (2021, TBD). IMMM-SFA/wm-abm_data_processing: PMP calibration and simulation for MOSART-WM-ABM (v1.0.0). Zenodo. http://doi.org/10.5281/zenodo.5570501.

## Contributing modeling software
| Model | Version | Repository Link | DOI |
|-------|---------|-----------------|-----|
| wm-abm_pmp | v1.0.0 | https://github.com/IMMM-SFA/wm-abm_pmp | http://doi.org/10.5281/zenodo.5570864 |
| wm-abm_data_processing | v1.0.0 | https://github.com/IMMM-SFA/wm-abm_data_processing | http://doi.org/10.5281/zenodo.5570501 |
| MOSART-WM-ABM | v1.1.2.abm | https://github.com/IMMM-SFA/iwmm | http://doi.org/10.5281/zenodo.4739516 |

## Reproduce my experiment
__0a.__ Preprocess the USDA data to produce these files:
   * `usda farm budget summary (machine readable).xlsx` - Combine the data for relevant crops from __[6]__ into a single Excel file.
   * `usda irrigation summary.xlsx` - Reformat the data from __[4]__ into a machine-readable format.
   * `usda irrigation water requirement.xlsx` - Reformat the data from __[5]__ into a machine-readable format.
   * `nldas_states_counties_regions.csv` - Map grid cells to U.S. state IDs, county IDs, and ERS farm regions; developed as part of this experiment using data from __[1]__ and spatial joins in ArcMap.
   * `water_proportions.csv` - Reformat the data from __[2]__ into a machine-readable format.
   * `water_costs.csv` - Aggregate surface water costs from __[5]__ and aggregate groundwater costs by dividing volume of groundwater irrigation __[2]__ by total groundwater energy cost __[3]__.
   * `cdl_gcam_lookup_v3_notavailcorr.csv` - Map CDL crop types to Global Change Analysis Model (GCAM) crop types; developed as part of this experiment.

__0b.__ Download the Cropland Data Layer (CDL) files for 2008-2018 from __[7]__ and preprocess:
   * For each year, sum the pixels for each CDL Crop category within each 1/8 degree North American Land Data Assimilation System (NLDAS) grid cell using ArcMap or similar tool; producing files like `cdl_{year}_clean.csv`
   * Run the script `cdl_processing.py` from __[10]__ to combine the yearly files into a single file in the expected format: `all_nldas_cdl_data_v3.txt`

__0c.__ Preprocess the output from steps __0a__ and __0b__ for use in MOSART-WM-ABM:
   * `crop_ids_by_farm.p` - Pickled dictionary mapping farm ID to the list of crop IDs on the farm; developed as part of this experiment.
   * `NLDAS_Grid_Reference.csv` - Maps NLDAS IDs to latitude/longitude coordinates; developed as part of this experiment by spatially joining an NLDAS shapefile with a U.S. counties shapefile in GIS.
   * `nldas.txt` - Subset of columns from `NLDAS_Grid_Reference.csv`.
   * `nldas_ids.p` - Pickled list of NLDAS IDs to be included in the optimization; developed as part of this experiment.
   * Run the script `wmabm_data_process.py` from __[10]__ to generate the following files:
      * `max_land_constr_20201102_protocol2.p`
      * `MOSART_WM_PMP_inputs_20201028.xlsx`
   * Run the script `hist_water_availability_abm.py` from __[12]__ which ingests some output files from a historical MOSART-WM simulation to generate the following files:
      * `hist_dependent_storage.csv`
      * `hist_avail_bias_correction_20201102.csv`
   * Run the script `MOSART_WM_PMP_stage1_noloop.py` from __[12]__ to generate the following files:
      * `gammas_new_20201102_protocol2.p`
      * `net_prices_new_20201102_protocol2.p`

__1.__ The results of step __0a__ are available as part of the code repository __[10]__; the results of step __0b__ can be downloaded from __[9]__; the results of step __0c__ are available as part of the code repository __[11]__.

__2.__ Download and unpack the MOSART-WM-ABM input data from __[8]__ into a supercomputing environment.

__3.__ Clone the MOSART-WM-ABM repository __[11]__ into a supercomputing environment; modifications to the source code may be necessary to run on unsupported machines.

__4.__ From the repository root directory, setup the model with the following shell commands (replacing sections surrounded by curly braces with the specifics of your environment):
   * `./cime/script/create_newcase --case {absolute path to a directory to create for your run} --res NLDAS_NLDAS --compset mosart_runoff_driven --project {cost center for your use of supercomputer}`
   * `cd {absolute path to your run directory}`
   * `./xmlchange DIN_LOC_ROOT={absolute path to your unpacked data directory from step 2}`
   * `./xmlchange DLND_CPLHIST_DIR={absolute path to your unpacked data directory from step 2}`
   * `./xmlchange LND_DOMAIN_PATH={absolute path to your unpacked data directory from step 2}`
   * `./xmlchange RUN_STARTDATE=1940-01-01`
   * `./xmlchange STOP_OPTION=nyears`
   * `./xmlchange STOP_N=70`
   * `./xmlchange JOB_WALLCLOCK_TIME=35:00:00`
     (_you may need more or less wallclock time depending on machine_)
   * `./xmlchange JOB_QUEUE={name of a job queue in your supercomputing environment}`
   * `./case.setup`

__5.__ Make the following modifications to the file `user_nl_mosart` in the root of your run directory:
   * Change the value of `parafile` to `'{absolute path to your unpacked data directory from step 2}/US_reservoir_8th_NLDAS3_updated_CERF_Livneh_naturalflow.nc'`.
   * Add a new line with: `frivinp_rtm = '{absolute path to your unpacked data directory from step 2}/MOSART_NLDAS_8th_20160426.nc'`

__6.__ Build the model with the shell command: `./case.build`

__7.__ Submit the model run to the job queue with the shell command: `./case.submit`

__8.__ If all is well, the model will eventually run, generating output and log files into your directory within the supercomputer's scratch file system, including the output data found in __[9]__.

## Reproduce my figures
Reproduce my figures:

The figures for the manuscript are generated based on post-processing of MOSART-WM-ABM output files in Python, Tableau, QGIS, and Inkscape. The WM-ABM working directory contains two general types of output files: 1) monthly netCDF output files with the MOSART-WM results (e.g., river flows, water demand, water shortage, etc.) and, 2) csv files containing annual ABM results (crop types, crop areas, etc.). The general steps are laid out below:

__1.__ The monthly netCDF files are post-processed into a consolidated csv file using the "WM_output_PIC_ncdf.py" script. The script reads in monthly the MOSART-WM netCDF files from __[9]__, calculates various annual summary statistics (e.g., average supply for each cell by year), saves the summary statistics into a pandas dataframe, and finally outputs the pandas dataframe as a csv (e.g., "wm_summary_results.csv").

__2.__ The "abm_output_processing.py" script is used to further post-process output, taking the annual abm output csv files and the wm summary file generated in step 1 as inputs.

__3.__ Figure 1a is generated based upon taking post-processed output from step 2 and developing the final visualizations in Tableau. Final touch ups (e.g., drought labels) are added in Inkscape.

__4.__ Figure 1b is generated based upon taking post-processed output from step 2 and generating the final maps in QGIS. A Stamen Terrain Background map is used for the visualization using QuickMapServices in QGIS. Final touch ups (e.g., modification of label locations) are conducted in Inkscape.

__5.__ The crop area bump charts (left side) of Figure 2 are generated based upon taking post-processed output from step 2 and developing the final visualizations in Tableau. See guide here: http://www.datatableauandme.com/2017/08/how-to-area-bump-chart-in-tableau.html.

__6.__ The shortage and adaptivity maps (right side) of Figure 2 are generated taking post-processed output from step 2 and developing the final visualizations in QGIS with final touch ups conducted in Inkscape.

__7.__ Figure 3 is generated based upon taking post-processed output from step 2 and developing the final visualizations in Tableau. Final touch ups (e.g., drought labels) are added in Inkscape.

__8.__ Figure 4 is developed in Powerpoint and does not rely on any data inputs.
