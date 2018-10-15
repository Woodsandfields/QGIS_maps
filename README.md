README
------

**This repository gathers different (elements of) mapping projects made with QGIS software.**

<a href="www.taz.de">Go to 'World Fertility' presentation + map</a>

[create an anchor](#first-map)

 <img align = "right" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/COUNTRY_AIRPORTS/WorldAirports.png" alt="Airport map" width="200"/> **QGIS is a free and open-source popular cross-platform desktop GIS application** allowing plugins written in Python and C++. GIS stands for "geographic information system". It is a system designed to capture, store, manipulate, analyze, manage, and present spatial or geographic data.

These repository projects are essentially practice maps made **during, around, and after a Knight Foundation course for journalists about GIS and Mapping**, using the QGIS software. 

Although the maps might look rudimentary, **this README will help you** navigate through the projects and learn what they intend to achieve. I have finalized the maps presented here as an illustration for the projects. Previous versions of these maps made on the go during training are to be found in the different folders.

<img align="right" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/HOSPITALS/US_hospitals_FINAL_MAP.png" width="200"/> QGIS doesn't provide the essential reproducibility features that R programming offers together with R's packages for plots and maps (sf, ggplot2, etc.). Yet, **QGIS is a powerful program used by many corporations and organizations, among them many journalists from the greatest newspapers** around the world as it provides a wonderful tool not only for illustration, but also for investigation. Further coding through GeoJSON leads even to greater results. 

That's why **learning QGIS with the Knight Foundation for journalists was a great choice:** The course itself provided additional readings, videos, examples, reflections, and collective debates as well as opportunities for writing essays.


Repo folder detail: goal, skills, sources, maps
===============================================

First map
---------

- Importing files
- Understanding shapefiles
- Discovering the QGIS interface and the diverse selection tools
- Accessing the attribute table and exploring properties

*Sources:*
- <https://www.naturalearthdata.com/downloads/> (small scale map, cultural)

<img align="center" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/THEFIRSTMAP/physicalRegions.png" /><img align="center" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/THEFIRSTMAP/AtlanticCountries.png"  /><img align="center" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/THEFIRSTMAP/Europe.png"  /><img align="center" src="https://github.com/Woodsandfields/QGIS_maps/blob/master/THEFIRSTMAP/Tropics.png"  />


**Fertility rates by country in the world**
-------------------------------------------

Making a choropleth map showing the fertility rates across the globe.</div>

*Skills learned:*
- explore the World Bank databases by indicator
- merge two files for a map with additional features by identify relatable factors and adding a layer
- set the right parameters for a successful choropleth map with the symbology property
- set the breaks manually instead of automatically
- reflect on the choice of colors and the number of breaks. 

*Sources:* 
- <https://www.naturalearthdata.com/downloads/> (Small Scale 1:110m,Cultural)
- <http://www.worldbank.org/> (fertility indicator)

*Comment on the map:* I used "pretty breaks" to make it less statistical and more casual: How many children do women have? I tried to select soft font and colors that would work warm enough without giving in to stereotypes, yet reminding the viewer that women, not households, are the main subject of this statistic.

![Fertility Map](https://github.com/Woodsandfields/QGIS_maps/blob/master/WORLD_FERTILITY/World%20Fertility%20Rates.png)

**San Marino**
--------------

This map intends to show a dot-density map for the small state of San Marino: each point represents here an habitant.

*Skills learned:*
- isolate a country from a world map to create a new map, 
- exploit the corresponding csv file, modify if necessary from within QGIS
- shape the dot-density map appropriately with the vector research random point in polygon function.

*Source:*
- <https://www.naturalearthdata.com/downloads/> 

*Comment on the map:* the blue is the official blue of San Marino. I tried to find a symbol with size and color that would both render people and let them be visible enough individually.

![San Marino Map](https://github.com/Woodsandfields/QGIS_maps/blob/master/SAN_MARINO/SanMarino.png)


**Country Airports**
---------------------

The idea is to run a point-in-polygon analysis so as compute and visualize how many airports are in each country.

*Skills:*
- explore further the Natural Earth website databases
- use the "count-points-in-polygon" VECTOR analysis tool
- use the attribute table of the count layer for choropleth maps 
- save the count layer to a distinct shapefile for later use

*Sources:*
- <https://www.naturalearthdata.com/downloads/10m-cultural-vectors/> (scroll down to 'Airport' section)
- <https://www.naturalearthdata.com/downloads/> (large scale data 1:10m, Cultural)

*Comment on the map*: I set breaks manually in order to reflect the high disparity between countries, choosing blue to represent air.

![final Airport Map](https://github.com/Woodsandfields/QGIS_maps/blob/master/COUNTRY_AIRPORTS/WorldAirports.png)

US hospitals
------------

Showing US hospitals on a map and creating point buffers to show how many people in the country live within35 miles of a hospital.

*skills:*
- importing properly a csv file that has longitude and latitude as factors as a delimited-text layer.
- modify symbols.
- create buffer zones bu using the vector geoprocessing tool buffer for the desired layer.
- convert from degrees to miles (1°=70 miles or 110 km)
- change layer hierarchy to see both hospitals and buffer zones
- export/save buffer layer independently to shapefile in order to have the possibility to later play with several buffers 

*Sources:*
- <https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals> (spreadshit)
- <https://www.naturalearthdata.com/downloads/> (small scale, Cultural)

*Comment on the map:* I changed the original settings to get buffer zones melt with each other, which is easier to read and let non-covered zones appear more clearly. Legend made with QGIS.

![US hospital buffer map](https://github.com/Woodsandfields/QGIS_maps/blob/master/HOSPITALS/US_hospitals_FINAL_MAP.png)

geocoding health services Austin 
--------------------------------

Goal: Geocode data about health services in Austin to map them

*Skills:*
- import csv files with addresses into a geocoding service and set parameters to get geolocation
- import geocoded data into QGIS like a normal text limited file with geometry, and check for errors


*Sources:*
- <https://www.geocod.io/> for geocoding
- <https://data.austintexas.gov/> (Austin Public Health Location, Export CSV)
-  several datasets from www.naturalearthdata.com (physical and cultural): countries, rivers, North America roads, urban areas.

*Comment on the map*: Added roads, river, and urban area to help the data make sense within an identifiable urban environment.

![Austin area and health services](https://github.com/Woodsandfields/QGIS_maps/blob/master/GEOCODING_AUSTIN/Austin_Public_Health_Services_locations.png)



Simplifying maps
----------------

Simplifying maps helps get to the adequate level of details while saving on file size, which can prove more convenient, e.g. in order to publish it on the web.

*Skills:*
- simplify within QGIS with the vector simplify function properly parametered and saving of the created layer
- simplify with mapshaper.org	
- organize the folder with different parameters/layers/shapefiles
- know the 0-100, 0-1 scale and its impact on the level of detail, as well as the different ways to choose
- consider different simplication models

*Source:*
- Naturalearthdata.com, countries (as usual)
- mapshaper.org (tool)

*Comment on the maps:* I played around with the print layer interface to produce those documents. I chose to focus on a small region to see how simplification plays at a restricted level, - and on a world view, because it looks good. Many other options were possible. I chose to use only one kind of simplification method because the two available produce quite the same details. 

![Simplifying the world map](https://github.com/Woodsandfields/QGIS_maps/blob/master/MAPS_SIMPLIFIED/severalDegreesOfSimplicationMapShaper.png) 

![The Silicon Valley Region](https://github.com/Woodsandfields/QGIS_maps/blob/master/MAPS_SIMPLIFIED/LA_SanDiego_Region.png)
