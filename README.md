README
======

This repository gathers different map (elements of) projects made with and around the Knight Foundation course for journalists about GIS and Mapping, using the QGIS software. 

Although it doesn't provide the essential reproducibility features of R programming and its packages dedicated to plots and maps (sf, ggplot2, etc.), QGIS is a highly powerful program which can turn into a wonderful investigation tool. That's why learning it with the Knight Foundation for journalists was a great choice.



Detail of Maps of this repo: goal, skills, sources
---------------------------------------------------

**First map**
=============

- Importing files
- Understanding shapefiles
- Discovering the QGIS interface and the diverse selection tools
- Accessing the attribute table and exploring properties

<https://www.naturalearthdata.com/downloads/> (small scale map, cultural)


**Fertility rates by country in the world**
===================

Making a choropleth map showing the fertility rates across the globe.

Skills learned:
- explore the World Bank databases by indicator
- merging two files for a map with additional features
- set the right parameters for a successful choropleth map with the symbology property
- setting the breaks manually instead of automatically
- reflecting on the choice of colors and the number of breaks. 

Sources: 
<https://www.naturalearthdata.com/downloads/> (Small Scale 1:110m,Cultural); 
<http://www.worldbank.org/> (fertility indicator)


**San Marino**
==============

This map intends to show a dot-density map for the small state of San Marino: each point represents here an habitant.

Skills learned:
- isolate a country from a world map to create a new map, 
- exploit the corresponding csv file, modify if necessary from within QGIS
- shape the dot-density map appropriately.

Source: 
<<https://www.naturalearthdata.com/downloads/> 



**Airports**
============

The idea is to run a point-in-polygon analysis so as compute and visualize how many airports are in each country.

Skills:
- explore further the Natural Earth website databases
- use the "count-points-in-polygon" VECTOR analysis tool
- use the attribute table of the count layer for choropleth maps
- save the count layer to a distinct shapefile for later use

Sources:

<https://www.naturalearthdata.com/downloads/10m-cultural-vectors/> (scroll down to 'Airport' section)

<https://www.naturalearthdata.com/downloads/> (large scale data 1:10m, Cultural)


US hospitals
============

Showing US hospitals on a map and creating point buffers.

Sources:
<https://hifld-geoplatform.opendata.arcgis.com>