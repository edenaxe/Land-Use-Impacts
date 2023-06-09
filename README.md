# Land-Use-Impacts

### Summary
This R markdown script provides an assessment of land use impacts for large industrial development portfolios. It includes summary statistics and project specific visuals. The resulting html report can be found [here](https://edenaxe.github.io/Land-Use-Impacts/Exports/Land-Use-Impacts.html).

### Requirements and Inputs
The script only requires a user to input a .kmz file (from google earth) that outlines each project to be analyzed. There is an example project portfolio .kmz file provided in the repo for illustration purposes. The NLCD land cover raster data is pulled in using `FedData`, and the US EPA eco-regions shapefiles are provided in this repo. The eco-regions file has been clipped, dissolved, and simplified in order to reduce file size and processing speed. 

### Process and Outputs
At a high level, the script overlays project outlines, land cover data, and biome data in order to generate summary tables and plots. Each project outline is used to extract exact raster coverage from the NLCD land use data set. Then, acraege is aggregated by classification and eco-region. This process is repeated for every project in the .kmz file and appended in to one cohesive data frame. This data frame is the basis for all remaining summaries and visuals. 

*Figure 1. (Top) Google earth outline of sample project and (bottom) resulting output plot*  
<img src="/Exports/process.PNG" width="75%" height="75%">

*Figure 2. Summary table of acreage by NLCD class and eco-region*  
<img src="/Exports/summary_table.PNG" width="75%" height="75%">
