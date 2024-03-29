# Farthest-On-Circle

## Introduction
Tool that uses ArcGIS technology to find out how far a vessel may get in a certain period of time. This could be useful if you need to estimate a ship's location. 

<p align="center">
  <img width="460" height="300" src="https://github.com/jfrygeo/Farthest-On-Circle/blob/master/FarthestOnCircle/Images/farthestOnCircle.PNG">
</p>

<i>Farthest on Circle Output Showing progress in hourly increments</i>

This tool could be used to get an understanding where a vessel may be located in a number of hours.

A user interacts with the tool by dropping a location of the ship's current, or last known location, and puts in a speed (in kts) and range for the analysis to be conducted. The output will display the amount of time a ship will get to a certain location. 

The farthest on circle uses a mask layer of suitable locations. For instance, boats travel on the water and a mask would have all water areas =1, and land areas = 0. The model will calculate the least cost distance from the ship’s location.  The mask of suitable locations can be created from various inputs, such as bathymetry information, or a generic mask of only water areas. 

## Sample Data
In this instance, the mask layer (watermaskworld1km) is a raster layer of water locations at 1km resolution. This dataset was created from the Esri's Countries Layer Package, where all country values (land areas) were marked as not suitable for navigation and all areas that are ocean are suitable. One could use a mask layer that is more restrictive, such as one that takes into account bathymetry, or restricted areas that ship cannot or will not pass through.

### Known issues
The sample dataset, (watermaskworld1km), has some issues as not all water areas are located in the dataset. For instance, inland bodies are water are not included, as well as small bodies of water such as canals, or narrow straits. 
