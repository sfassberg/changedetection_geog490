# Detecting Change After the 2013 California Rim Fire

## By Sam Fassberg, Bowie Hutcheson, and Jasper Zhou

We are going to use Landsat-8 imagrey acquired from Google Earth API from before, after, and well after the California Rim Fire that happened in 2013. We are going to calculate NDVI, calculate + anaylze change in NDVI and NLCD, and visualize results on graphs and maps. 

**Objective:** We want to calculate the pixel change in NDVI and NLCD after the 2013 Rim Fire to see trends and potenital vegetation recovery.

* Expected outcomes: 
	* By calculating and comparing NDVI and vegetation change that the area surrounding the 2013 Rim Fire will show strong evidence of vegetation change. The changes that we expect to see are low vegetation health before the fire, low vegetation health after the fire, and better vegetation health after a long periods of time. 
	* In terms of pixel change, we expect to see more pixels classified as "healthy vegetation" in the imagery after the fire compared to vegetation pixels before the fire.

* Any other relevant information, images/tables, references, etc.:
	* The imagery that is going to be used will be derived from Landsat remote sensing images that contain raster data. The images in this project will consist of imagery from before the fire (2011), right after the fire (2013), and short-term after the fire (2016), and long-term after (2019).  
	* The images will be focused/cropped to fit the area of interest. In this case, the area burned from the 2013 Rim Fire in California. Plots showing the change following the fire will be presented in plots using the matplotlib package. 
	* Change detection will be measured based on amounts of classified pixels that were lost/gained or changed to a different class over time. The maps that we will be making to show the land cover class change will be done using Leaflet. 

* References:
	* USGS (Landsat imagery)
	* Google Earth Engine
