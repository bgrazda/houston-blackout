# Identifying the Impacts of Extreme Weather
# Great Texas Freeze: Houston, TX 2021
### Author: Brooke Grazda

![icicles_pipeline.jpg](images/icicles_pipeline.jpg)


## About

In February 2021, Texas experienced a severe winter storm that resulted in extreme power outages throughout Houston. These extreme temperatures as a result of climate change noted a need for greater climate resiliency. Also known as the Great Texas Freeze, this weather event had cascading effects on buildings that lost power throughout the state. This repository highlights the city of Houston, analyzing night satellite imagery to observe differences in median income levels of census tracts that lost power.

## Purpose
- Utilize `sf` and `terra` packages to combine raster and vector data
- Identify census tracts that experienced power outages using centroids
- Map effects of power access before and after extreme weather effect 
- Visualize distribution of median household incomes for homes that lost power

## Repository Structure

```bash
houston-blackout
│
├── data                        
│   ├── ACS_2019_5YR_TRACT_48_TEXAS.gdb # See folder for more files
│   ├── VNP46A1  # Before and after weather event tiles
│        ├── VNP46A1.A2021038.h08v05.001.2021039064328
│        ├── VNP46A1.A2021038.h08v06.001.2021039064329
│        ├── VNP46A1.A2021047.h08v05.001.2021048091106
│        ├── VNP46A1.A2021047.h08v06.001.2021048091105
│   ├── gis_osm_buildings_a_free_1.gpkg
│   ├── gis_osm_roads_free_1.gpkg
│   
├── houston-blackout.qmd # Quarto markdown for analysis
├── houston-blackout.html  # Render HTML
├── houston-blackout.Rproj
├── houston-blackout-files
|   ├── figure-html
|        ├── unnamed-chunk-7-1.png  # Data visualizations 
|        ├── unnamed-chunk-7-2.png
|        ├── unnamed-chunk-7-3.png
├── README.md  
├── LICENSE                      
├── .gitignore  
│
├── images/                       
│   ├── icicles_pipeline.jpg  # Image used in the README
│                
```

## Data
This data utilizes NASSA's Worldview to explore the storm data surrounding the storm. These 10x10 degree tiles located in the VNP46A1 folder show clear images of before and after the event, indicated by the dates `h08v05` and `h08v06` of the data files. The roads data files show the highway data from this winter storm, provided by OpenStreetMap (OSM). OSM also has a shapefile for the roads and building data in the Houston metropolitan area, which are used in this analysis. The US Census Bureau's American Community Survey's geodatabase on socioeconomic information was used to locate a geometry of Texas census tracts. 

## Acknowledgements

Dr. Ruth Oliver and Ale Vidal-Meza, thank you for your guidance and instruction in EDS 223: Geospatial Analysis and Remote Sensing. 

## Data References
Wikipedia. 2021. “2021 Texas power crisis.” Last modified October 2, 2021. https://en.wikipedia.org/wiki/2021_Texas_power_crisis.↩︎

Geofabrik GmbH and OpenStreetMap Contributors. (2018). OpenStreetMap Data. Retrieved from https://www.geofabrik.de.

U.S. Census Bureau. (n.d.). American Community Survey. U.S. Department of Commerce. Retrieved from https://www.census.gov/programs-surveys/acs

