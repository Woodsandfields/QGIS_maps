README
------

This repository gathers different (elements of) mapping projects made with QGIS software.

QGIS is a free and open-source popular cross-platform desktop GIS application allowing plugins written in Python and C++. GIS stands for "geographic information system". It is a system designed to capture, store, manipulate, analyze, manage, and present spatial or geographic data. GIS applications are tools that allow users to create interactive queries (user-created searches), analyze spatial information, edit data in maps, and present the results of all these operations.

Those projects are essentially practice maps made during and after a Knight Foundation course for journalists about GIS and Mapping, using the QGIS software. 

Although the final maps might look quite rudimentary for a bunch of them, this README gives indication about what to concretely find in the folders, as well as the skills and sources that have been used for the results. 

QGIS doesn't provide the essential reproducibility features of R programming and its related packages dedicated to plots and maps (sf, ggplot2, etc.). And yet, QGIS is a highly powerful program used by many corporations and organizations, among them many journalists from the greatest newspapers around the world as it provides a wonderful not only illustration, but also investigation tool. That's why learning it with the Knight Foundation for journalists was a great choice. The course itself provided additional examples and reflections about the use of maps in journalism and the way they could be exploited to achieve great results.


Detail of map folders in this repo: goal, skills, sources
==========================================================

**First map**
-------------

- Importing files
- Understanding shapefiles
- Discovering the QGIS interface and the diverse selection tools
- Accessing the attribute table and exploring properties

Sources:
- <https://www.naturalearthdata.com/downloads/> (small scale map, cultural)


**Fertility rates by country in the world**
-------------------------------------------

Making a choropleth map showing the fertility rates across the globe.

Skills learned:
- explore the World Bank databases by indicator
- merge two files for a map with additional features by identify relatable factors and adding a layer
- set the right parameters for a successful choropleth map with the symbology property
- set the breaks manually instead of automatically
- reflect on the choice of colors and the number of breaks. 

Sources: 
- <https://www.naturalearthdata.com/downloads/> (Small Scale 1:110m,Cultural)
- <http://www.worldbank.org/> (fertility indicator)


**San Marino**
--------------

This map intends to show a dot-density map for the small state of San Marino: each point represents here an habitant.

Skills learned:
- isolate a country from a world map to create a new map, 
- exploit the corresponding csv file, modify if necessary from within QGIS
- shape the dot-density map appropriately.

Source: 
- <https://www.naturalearthdata.com/downloads/> 



**Airports**
------------

The idea is to run a point-in-polygon analysis so as compute and visualize how many airports are in each country.

Skills:
- explore further the Natural Earth website databases
- use the "count-points-in-polygon" VECTOR analysis tool
- use the attribute table of the count layer for choropleth maps
- save the count layer to a distinct shapefile for later use

Sources:
- <https://www.naturalearthdata.com/downloads/10m-cultural-vectors/> (scroll down to 'Airport' section)
- <https://www.naturalearthdata.com/downloads/> (large scale data 1:10m, Cultural)


US hospitals
------------

Showing US hospitals on a map and creating point buffers to show how many people in the country live within35 miles of a hospital.

- importing properly a csv file that has longitude and latitude as factors as a delimited-text layer.
- modify symbols.
- create buffer zones bu using the vector geoprocessing tool buffer for the desired layer.
- convert from degrees to miles (1°=70 miles or 110 km)
- change layer hierarchy to see both hospitals and buffer zones
- export/save buffer layer independently to shapefile in order to have the possibility to later play with several buffers 

Sources:
- <https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals> (spreadshit)
- <https://www.naturalearthdata.com/downloads/> (small scale, Cultural)


geocoding health services Austin 
--------------------------------

Goal: Geocode data about health services in Austin to map them

Skills:
- import csv files with addresses into a geocoding service and set parameters to get geolocation
- import geocoded data into QGIS like a normal text limited file with geometry, and check for errors


Sources:
- <https://www.geocod.io/> for geocoding
- <https://data.austintexas.gov/> (Austin Public Health Location, Export CSV)
-  several datasets from www.naturalearthdata.com: countries, rivers, North America roads, urban areas.