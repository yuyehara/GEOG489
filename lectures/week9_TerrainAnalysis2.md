Week 9: Watershed Analysis (2)
========================================================
author: Yi Qiang
date: Mar. 10, 2017
autosize: true
font-family: 'Helvetica'
css: style.css

Stream and Watershed Delineation
========================================================
Flow direction
Flow accumulation
Stream delineation
Stream network/order
Watershed delineation


What is watershed
========================================================

Definition: An area of land where all of the water that falls in it and drains off of it goes to a common outlet.
<img src="http://www.maine.gov/dep/land/watershed/images/watershed_diagram_sm.jpg" width="1000">

What is watershed
========================================================
A hierachical system - 6 levels in the U.S. (Hydrologic Unit Code)
  - regions, subregions, basins, subbasins, watersheds, and subwatersheds
<img src="https://water.usgs.gov/pubs/wri/wri934076/usimage/huc_region.gif" width="1000">

Watershed delination in a contour map
========================================================
General steps:
  1. Determine the outlet point (mark as a circle)
  2. Identify high points around the upperstream of the outlet point (mark as crosses)
  3. Starting from the outlet point, drawing a line to link all high points (crosses)
    - The line should be in the right angle to the contour lines

Watershed delination in a contour map
========================================================
<img src="https://www.nrcs.usda.gov/Internet/FSE_MEDIA/nrcs144p2_014463.jpg" width="800">

Watershed delination in digital elevation model
========================================================
How to delineate watershed in DEM
<img src="../labs/lab4_data/misc/DEM1.jpg" width="1000">

Watershed delination in digital elevation model
========================================================
General steps:
  1. Pit/Peak filling - remove error pixels
  2. Flow direction - where water flow at each pixel
  3. Flow accumulation - water in how many pixels will eventually flow to this pixel
  4. Watershed and stream delineate
  
Pit/peak filling
=======================================================
- Sinks (and peaks) are often errors due to the resolution of the data or rounding of elevations to the nearest integer value. (Fill tool in ArcGIS)
- Sinks & peaks should be filled to ensure proper delineation of basins and streams. If the sinks and peaks are not filled, a derived drainage network may be discontinuous.



<img src="http://desktop.arcgis.com/en/arcmap/10.3/tools/spatial-analyst-toolbox/GUID-891C65E2-06F2-45D3-B4A0-AE7473231116-web.gif" width="700">

<img src="http://desktop.arcgis.com/en/arcmap/10.3/tools/spatial-analyst-toolbox/GUID-43E23C7B-0190-4C60-B632-8A5CF967E695-web.gif" width="700">


Pit/peak filling
=======================================================
<img src="../labs/lab4_data/misc/pit_filling.jpg" width="1200">

Pit/peak filling
=======================================================
<img src="https://blogs.esri.com/esri/arcgis/files/2013/03/Fig3.jpg" width="1000">

Flow direction
=======================================================
The direction from each cell to its steepest downslope neighbor.<br>
Coded as: 2<sup>x</sup> (x=1,2,... 8) from east and clockwise  <br>
<img src="http://pro.arcgis.com/en/pro-app/tool-reference/spatial-analyst/GUID-A541AFD3-922C-41DA-952C-0D4524F85B39-web.gif" width="800">

Flow direction
=======================================================
  1.Identify the neighbor pixels with lower elevation than the central pixel
  2.Calculate the downslopes, find the neighbor pixel with highest downslope rate.
  Note: different from aspect
<img src="../labs/lab4_data/misc/Flow_direction.jpg">

Stream delineation
=======================================================
Linking cells by their flow directions
<img src="../labs/lab4_data/misc/Flow_direction2.jpg" width = "1100">

Stream delineation
=======================================================
1. Flow accumulation - the number of pixels flowing into the pixel
2. Stream delineation - All cells with flow accumulation above a threshold form a stream (Reclassify or Raster Calculator)
<img src="../labs/lab4_data/misc/Flow_direction2.jpg"  width = "1000">

Stream segmentation in DEM
=======================================================
Numbering streams in a stream raster
<img src="../labs/lab4_data/misc/stream_segmentation.jpg" width = "800">

Stream delineation
=======================================================
<img src="../labs/lab4_data/misc/threshold.jpg"  width = "1000">

Stream network and order
=======================================================
- Stream network is hierachical
- Strahler method: The stream order increases when streams of the same order intersect. Otherwise, the higher-order stream continues. (Stream Order tool)

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/Flussordnung_%28Strahler%29.svg/310px-Flussordnung_%28Strahler%29.svg.png" width = "800">


Watershed delineation
=======================================================
1. Identify watershed outlet (pour point) - Snag to pour point tool in ArcGIS
<img src="../labs/lab4_data/misc/pour_point.jpg" width = "800">





