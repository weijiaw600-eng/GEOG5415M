# GEOG5415M
Socioeconomic Deprivation & Urban Green Space Accessibility in Leeds

1.Project Overview：

This project explores the spatial relationship between community wealth (Socioeconomic Deprivation) and access to public parks in Leeds, UK. By integrating geospatial data from the 2019 Index of Multiple Deprivation (IMD) and OpenStreetMap (OSM), the study evaluates whether "environmental injustice" exists in the allocation of natural resources.

2.Data Sources：

Socioeconomic Data: UK Index of Multiple Deprivation (IMD) 2019 at the LSOA level.
Spatial Data: Green space features (tagged leisure=park) extracted via the osmnx library from OpenStreetMap.
Boundary Data: Leeds City LSOA community boundaries (GeoJSON) from the ONS Geography Portal.


3.Technical Stack：

The analysis is implemented in Python using the following libraries:
Data Processing: pandas, geopandas 
Spatial Analysis: osmnx, shapely 
Visualization: matplotlib, seaborn, mapclassify (for choropleth maps) 

4.Key Methodology：
Preprocessing: Filtered 482 LSOA units in Leeds and reprojected data to EPSG:27700.
Distance Calculation: Calculated the straight-line distance from each community's geometric centroid to the nearest park.
Visualization: Produced bar plots by deprivation decile and spatial choropleth maps showing accessibility patterns.

5.Main Findings：
Poorer neighborhoods (IMD Decile 1-4) actually have a shorter average distance to parks (~250-300m) compared to the wealthiest areas (IMD Decile 10, >500m).
A "core-periphery" pattern exists, where the city center enjoys high accessibility, while the urban-rural fringe (eastern and northwestern edges) faces significant resource deprivation.

6.How to Run：

Ensure all dependencies are installed: pip install osmnx geopandas matplotlib seaborn mapclassify.
Load the IMD CSV and LSOA GeoJSON files into the /content/ directory. 
Execute the Jupyter Notebook project1.ipynb.



Coordinate System: UK National Grid (EPSG:27700) for accurate metric distance calculations.
