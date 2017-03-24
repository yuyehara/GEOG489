Week 7: Terrain Analysis
========================================================
author: Yi Qiang
date: Feb. 24, 2017
autosize: true
font-family: 'Helvetica'
css: style.css

Terrain Analysis
========================================================
- The Earth Surface is not flat

<img src="http://i.imgur.com/ITHz4X2.gif" width="800">

Terrain Analysis
========================================================
- In addition to X, Y, there is Z (height)
- Also called 3D Analysis

<img src="http://www.gruner.com/baffin/18s_cropped.jpg" width="800">

Why analyze terrain?
========================================================
- Different types of terrain - different patterns of X, Y, and Z
- Formed by different processes - geological, hydrological, and volcanic
- [Human activities (anthropocene)](http://anthropocene.info/)
 <img src="../labs/lab4_data/misc/terrain.JPG" width="800">


Why analyze terrain?
========================================================
Spatial metrics, such as distance, area and volumne

 <img src="../labs/lab4_data/misc/sad.jpg" width="900">
 
Why analyze terrain?
========================================================
Surface adjusted distance

<img src="../labs/lab4_data/misc/sad2.jpg" width="900">

Why analyze terrain?
========================================================
hydrological modeling
 
<img src="http://www.microimages.com/documentation/html/useTNTfor/images/watershed00.jpg" width="900">

Why analyze terrain?
========================================================
Landslide modeling

<img src="../labs/lab4_data/misc/land_slide.jpg" width="900">

Why analyze terrain?
========================================================
Suitability modeling

<img src="http://www.tellurideskiresort.com/content/uploaded/images/maps/TSR-TM-16-17_1242x874.jpg" width="900">


Modeling Surface in GIS
=========================================================
## Two Most Common Terrain Data Models:

- Digital Elevation Data (DEM) (Raster)
- Triangular Irregular Network (TIN) (Vector)

Digital Elevation Model (DEM)
=========================================================
- DEM is basically a normal raster of elevation -it's called DEM because it is specific for a topographic surface 
- A DEM is the simplest form to represent a topographic surface
- One of the most widely used data layers in many GIS applications
- The critical parameter is the resolution (or grid cell size)
- 1m resolution DEM for HI, 30m resolution for the US and 1km resolution for the globe are freely available


Digital Elevation Model (DEM)
=========================================================
Essentially a raster of elevation (2D matrix)

<img src="../labs/lab4_data/misc/DEM1.jpg" width="900">

Digital Elevation Model (DEM)
=========================================================
DEM in 3D

<img src="http://www.innovativegis.com/basis/present/gita_denver05/Default_files/image004.jpg" width= "600">


Triangular Irregular Model
=========================================================

A vector model for 3D terrain

<img src="http://www.edc.uri.edu/nrs/classes/nrs409509/Lectures/8Models/AnalysisGraphics/TIN_Model.gif" width="800">

Triangular Irregular Model
=========================================================
Delaunay Triangulation between sampling points

<img src="../labs/lab4_data/misc/TIN1.jpg" width="750">

Triangular Irregular Model
======================================================
A facet of TIN in 3D
<img src="../labs/lab4_data/misc/TIN2.jpg" width="900">

Triangular Irregular Model
======================================================
Resolution of TIN - number of triangles

<img src="../labs/lab4_data/misc/TIN3.jpg" width="700">

Basic Terrain Analysis
=========================================================
- Surface-adjusted metrics (distance and area)
- Slope (Landslide susceptibility)
- Aspect (Solar insolation, vegetation)
- Profile (elevation change along a line)
- Viewshed (visibility)
- Hillshade (visualization)
- Area solar radiation
- *Flow path, watershed delination, flow accumulation (hydrology)*
- *Indices (e.g., terrain ruggedness)*

Distance calculation in DEM (Pixel-to-pixel approach)
=========================================================
- Convert a vector line to a raster line
- The sum of actual run between every pair of adjacent pixels

<img src="../labs/lab4_data/misc/distance.jpg" width="900">

Distance calculation in DEM (Sampling approach)
=========================================================

- Define sampling points along a transect
- The sum of distance between each pair of points

<img src="../labs/lab4_data/misc/cc_dist.jpg" width="400">

Distance calculation in TIN
=========================================================

- Define a number of sampling points along a transect
- The elevation of a point is estimated from the triangle it is located in or the surrounding triangles
- The sum of distance between each pair of sampling points

<img src="../labs/lab4_data/misc/distance_tin.jpg" width="1000">

No guidelines of distance calculation
=========================================================
- ~ 10 different measurement approaches
- Caculation accuracy = f(DEM/TIN resolution, landscape, interpolation method, sampling size)
- Trade-offs between accuracy and data size, accuracy and computation time.

<img src="../labs/lab4_data/misc/sad3.jpg" width="1000">


Area caculation
=========================================================

Surface adjusted area is the total area of all the triangular facets

<img src="https://www.mathworks.com/matlabcentral/mlc-downloads/downloads/submissions/42204/versions/2/screenshot.png" width="500">


Slope Calculation
=========================================================
- Angle of the slope (degree)
- Ratio of the slope (percentage)

<img src="../labs/lab4_data/misc/slope.jpg" width="900">


Calculate slope in DEM
=========================================================

- In DEM, maximum rate of change in value from that cell to its neighbors.<br>

<img src="http://www.innovativegis.com/basis/mapanalysis/topic11/Topic11_files/image043.png" width="900">

Slope calculation in ArcGIS
=========================================================
Geometric combination of vertical (x direction) descent and horizontal (y direction) descent <br>
<img src="../labs/lab4_data/misc/slope2.jpg" width="1000">


Calculate slope in DEM
=========================================================
Elevation to Slope

<img src="http://desktop.arcgis.com/en/arcmap/10.3/tools/spatial-analyst-toolbox/GUID-3922F5AA-019D-4625-8C19-B67E7DF5B092-web.png" width="1200">

Aspect
=========================================================
- The direction of the slope 

<img src="http://pro.arcgis.com/en/pro-app/tool-reference/spatial-analyst/GUID-A3590481-6E96-4BD8-BF50-25093FD55F00-web.gif" width="250"><br>
<img src="http://pro.arcgis.com/en/pro-app/tool-reference/spatial-analyst/GUID-8A2021F8-6D40-4EDA-B677-4C376C6DC246-web.png" width="700">


Profile
=========================================================
Most GIS packages provide tools for examining the profile of a surface along a selected straight line or series of straight line segments (polyline).

<img src="http://www.spatialanalysisonline.com/HTML/clip0250.png" width="1200">


Profile
=========================================================
Profile along multiple straight transects

<img src="http://www.spatialanalysisonline.com/HTML/clip0251.png" width="600">


Profile
=========================================================
- Profile of a path/route

<img src="../labs/lab4_data/misc/TDF.jpg" width="1200">

Viewshed
=========================================================
- Areas visible to a set of observer features.
- Viewshed tool in ArcGIS

<img src="http://pro.arcgis.com/en/pro-app/tool-reference/3d-analyst/GUID-E0E64C10-1AE7-4925-88DB-6EDD7ACE91A8-web.png" width="800">


Viewshed
=========================================================
- Listening Posts/Observation Posts (LP/LO)
- Weapons placement
- Antenna placement for radar, radios, or cell phones
- Special surveillance equipment placement

<img src="../labs/lab4_data/misc/viewshed11.jpg" width="800">

Hillshade
=========================================================
- Hypothetical illumination of a surface by determining illumination values for each cell in a raster
- Enhance the visualization of a surface for analysis or graphical display
- Parameters: altitude and azimuth

<img src="../labs/lab4_data/misc/viewshed1.jpg" width="1200">


Altitude (Hillshade)
==========================================================
- The altitude is the angle of the illumination source (e.g. the sun) above the horizon. 
- The units are in degrees, from 0 (on the horizon) to 90 (overhead). The default is 45 degrees.
<img src="http://pro.arcgis.com/en/pro-app/tool-reference/3d-analyst/GUID-65020708-B706-4B97-A9F3-A8F4EBA2A834-web.gif" width="600">


Azimuth (Hillshade)
==========================================================
- Azimuth is the angular direction of the sun, measured from north in clockwise degrees from 0 to 360. 
- An azimuth of 90 degrees is east. The default azimuth is 315 degrees (NW).
- Why default azimuth is 315 (NW), given most people are living in the North Hemisphere where the Sun azimuth is South?


<img src="http://pro.arcgis.com/en/pro-app/tool-reference/3d-analyst/GUID-B0CF4608-E687-460F-BA90-133EC5D6DACD-web.gif" width="600">

Hillshade
==========================================================
## Sink or hill?
<img src="../labs/lab4_data/misc/hs_135.jpg" width="500">

Hillshade
==========================================================
## Sink or hill?
<img src="../labs/lab4_data/misc/hs_315.jpg" width="500">

Hillshade
==========================================================
Original DEM - hill <br>
<img src="../labs/lab4_data/misc/origin_dem.jpg" width="500">

Hillshade
=========================================================
- Combining viewshed with elevation

<img src="../labs/lab4_data/misc/viewshed2.jpg" width="1200">

Solar Radiation Analysis
=========================================================
Cumulative solar radiation in a day (Area Solar Radiation tool in ArcGIS)

<img src="http://www4.ncsu.edu/~emohler/gis582/582images/a10/figure2sm.png" width="800">

Viewshed
=========================================================
Solar Radiation: Summer Solstice

<img src="http://www4.ncsu.edu/~emohler/gis582/582images/a10/figure7sm.png" width="900">

Viewshed
=========================================================
Solar Radiation: Winter Solstice
<img src="http://www4.ncsu.edu/~emohler/gis582/582images/a10/figure8.png" width="900">

Anouncement
=========================================================
Change of topics:
Topic 5: Spatial Interpolation -> Hazard risk and vulnerability assessment
Topic 6: Advanced spatial modeling -> Web mapping
Next class -> Project discussion

Lab 4 Assignment (Terrain analysis)
=========================================================

Due date March 17

[https://github.com/qiang-yi/GEOG489/blob/master/labs/lab4_terrain_analysis.docx](https://github.com/qiang-yi/GEOG489/blob/master/labs/lab4_terrain_analysis.docx)
