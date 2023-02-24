# Detecting Change After the 2013 California Rim Fire

## By Sam Fassberg, Bowie Hutcheson, and Jasper Zhou

We are going to use Landsat and Sentinel imageries acquired from Google Earth API from before, after, and well after the California Rim Fire that happened in 2013. We are going to calculate NDVI, calculate + anaylze change in NDVI and NLCD, and visualize results on graphs and maps. 

**Objective:** We want to calculate the pixel change in NDVI and NLCD after the 2013 Rim Fire to see trends and potenital vegetation recovery.

* Datasets in this project
  * In this project, we will acquire most data from [Google Earth Engine](https://earthengine.google.com/):
    * [Landsat](https://developers.google.com/earth-engine/datasets/catalog/landsat)
      * [Landsat 7 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C02_T1_L2)
      * [Landsat 8 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2)
    * [Sentinel](https://developers.google.com/earth-engine/datasets/catalog/sentinel)
      * [Sentinel 2 MSI: MultiSpectral Instrument, Level-2A](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
  * NLCD data from [Multi-Resolution Land Characteristics (MRLC)](https://www.mrlc.gov/data)
* 
Required Python packages:
  * jupyter
  * geemap
  * ee
  * geopandas
  * panda
  * numpy
  * rasterio
  * seaborn
  * matplotlib
  * folium
  * altair
  * IPython.display
  * for file management:
    * os
    * glob

* Methods and approach
  - We identified a study area where the Rim Fire (37.83° N, 119.64° W) took place in 2013. The cause of this fire was due to illegal camp fire. The cost of this fire is $127.34 million (2013 USD); impacted area was 257,314 acres.
  - We acquire level-2 satellite imageries from GEE with cloud cover less that 15%. Set map center to the impacted area. We want imagery from before the fire (2011), right after fire (2013), short-term after fire (2016), long term after fire (2019). The satellite we will use in this project include Landsat and Sentinel.  
  - Compute and visualize four NDVI layers and subtract the layers to show changes in the impacted area. We will plot a time series of changes in these years based on NDVI.
  - To better visualize the land cover changes, we choose to analyze NLCD datasets. NLCD data will acquire from MRLC website. We will process the data and only show the area of impacted area and adjacent regions.
  -  We will perform some data cleaning; for instance, merge all the "Developed" land into one class, and then count pixels of each land cover class.
  - Next, creating several dataframes (e.g., NLCD_2013 vs. NLCD_2011) showing pixel count changes and pixel changes in percentage.
  - Generating a project report base on these analyses and observations.

* Expected outcomes: 
	* By calculating and comparing NDVI and vegetation change that the area surrounding the 2013 Rim Fire will show strong evidence of vegetation change. The changes that we expect to see are low vegetation health before the fire, low vegetation health after the fire, and better vegetation health after a long periods of time. 
	* In terms of pixel change, we expect to see more pixels classified as "healthy vegetation" in the imagery after the fire compared to vegetation pixels before the fire.

* Any other relevant information, images/tables, references, etc.:
	* The imagery that is going to be used will be derived from Landsat remote sensing images that contain raster data. The images in this project will consist of imagery from before the fire (2011), right after the fire (2013), and short-term after the fire (2016), and long-term after (2019).  
	* The images will be focused/cropped to fit the area of interest. In this case, the area burned from the 2013 Rim Fire in California. Plots showing the change following the fire will be presented in plots using the matplotlib package. 
	* Change detection will be measured based on amounts of classified pixels that were lost/gained or changed to a different class over time. The maps that we will be making to show the land cover class change will be done using Leaflet. 

* References:
	* Multi-Resolution Land Characteristics (MRLC)
	* Google Earth Engine
