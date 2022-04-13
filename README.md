
Short-term Forest Change Tool
===========================

Last update: April 3, 2020
Created by: NASA DEVELOP Spring 2020 Costa Rica and Panama Ecological Forecasting Project Team: Teodora Mitroi, Kate Markham, Eder Hernandez, Sharifa Karwandyar

Contact: Teodora Mitroi, mitteodora@gmail.com

The script was developed using Google Earth Engine (GEE). It uses Landsat 8 
OLI TOA Reflectance with maskL8sr cloud-mask, Sentinel MSI Level-1C with 
maskS2cloud cloud-mask, and Terra Moderate Resolution Imaging 
Spectroradiometer (MODIS). It also utilizes the Hansen Global Forest Change 
v.16 (2000-2018)to mask non-forested areas from calculations. Vegetation 
indices such as Enhanced Vegetation Index (EVI) and Normalized Difference 
Vegetation Index (NDVI) were used. The main scope of the software is to 
display changes in vegetation of forested area and identify regions of 
possible deforestation.
-----------------
PROCEDURE:
-----------------
1. Paste the code into GEE.
2. Scroll to the section ìEnter Dates of Choice and read the instructions in the comments. Enter starting month, starting day, end month, end day, and beginning year of the first year, and do the same for the second(later) date. 
3. To enter your own study area, you must first import it as an asset into GEE. Click on the Assets tab in the left window on the GEE playground and click NEW. Then, select ìShape files and search your directory for your shp, zip, dbf, prj, shx, cpg, fix, qix, sbn or shp.xml files. Next, name your asset, and rewrite your path name so it directs shapefile to your asset. Use lines 107 and 115 as examples.
4. Press Run at the top to start analyzing your input and begin processing.
5. Buttons will appear on the side where you can select what satellite and vegetation index to use, as well as time interval (before, after, change).
6. Under the Tasks tab on the upper right, the average change in EVI and NDVI by region will display as a percentage for you to export as a table. Click run to download to a folder in your drive you specify in line 166.
7. To export maps, scroll in the right panel of the user interface to the Export section. Press the button of the map you wish to download. Visit the Tasks tab once more to see your map; press ìRun.îAfter you are finished, you will be able to export the maps as GeoTIFF (.tif) in in the  folder you specified on line 166. 
-----------------
Introduction:
Since the establishment of the Mesoamerican Biological Corridor in 1997 in Central America, deforestation has continued to plague La Amistad International Park due to the expansion of agriculture and the strain of financial and natural resource management. The Athens Spring 2020 DEVELOP team and the partners created the software to assess forest disturbances and deforestation in the Corridor. The tool calculates NDVI and EVI for any two time periods and maps the change in the indices. 
-----------------
Application and Scope:
Users will be able to input their choice of region and date range and identify areas within the region that have underwent changes in forest cover.
-----------------
Capabilities:
The software has the capability to calculate NDVI and EVI for Landsat 8, Sentinel, and MODIS, and calculate the change. It also is able to output the average change of EVI and NDVI for regions date range. 
-----------------
Limitations: 
Because this tool uses the Hansen Global Forest Change dataset, it has the same limitations as this dataset. The Hansen dataset is current only through 2018. Thus, if the user were to attempt to identify changes in EVI from 2019 and 2020 (or any time after 2018), the STFC tool verifies that the change occurred in a forested area with 2018 forest cover.In addition, the canopy cover included in the Hansen dataset is not restricted to only natural forest canopy cover but also includes agricultural areas, plantations, and other vegetation types. If Hansen releases an update for 2019, that data can be easily implemented in the code. 

-----------------
*****For more detailed information about using the tool, please see the Short-term Forest Change Tool Operating Procedures Guide.
