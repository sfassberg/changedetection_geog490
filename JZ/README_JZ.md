* Datasets in this project
  * In this project, we will acquire most data from [Google Earth Engine](https://earthengine.google.com/):
    * [Landsat](https://developers.google.com/earth-engine/datasets/catalog/landsat)
      * [Landsat 7 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C02_T1_L2)
      * [Landsat 8 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2)
    * [Sentinel](https://developers.google.com/earth-engine/datasets/catalog/sentinel)
      * [Sentinel 2 MSI: MultiSpectral Instrument, Level-2A](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
  * NLCD data from [Multi-Resolution Land Characteristics (MRLC)](https://www.mrlc.gov/data)
* Required Python packages:
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
