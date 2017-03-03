Week 8: Proposal Feedback
========================================================
author: Yi Qiang
date: Mar. 3, 2017
autosize: true
font-family: 'Helvetica'
css: style.css

Proposals
========================================================
## 8 proposals received.
  - 6/8 of them are suitability modeling
  - 2/8 may be vulnerability/risk assessment
  - 8/8's study area is Hawaii
  

Common issues
=======================================================
## Lacking justification of criteria being used and weights assigned to criteria
## Solution:
- Consult literature and domain expert
- Validate with existing distribution
- Adjust your model by Trial-and-Error approach
- Build a regression model between existing distribution (dependent variable) and criteria (predictive variables)



Data sources
========================================================
Office of Planning - State of Hawaii http://planning.hawaii.gov/gis/download-gis-data/

Climate, Rainfall Atlas, Evapotranspiration, Solar Radiation of Hawaii - UH Geography
http://climate.geography.hawaii.edu/

UH Coastal Geology Group
http://www.soest.hawaii.edu/coasts/data/

UH Manoa Library
http://magis.manoa.hawaii.edu/gis/data.html

ArcGIS online
Data with 'Add' button are downloadable


Data processing
========================================================
1. Specify a study area - In an administrative boundary or mannually delineate
2. Clip all large data layers into the study area
3. Convert all data layer into the same projection system
  - If you have raster data (e.g. dem, land cover), convert all other data into the projection of raster data
4. You can use tools to convert projection (Projection) and clip data (Clip for vector, Extract by Mask for raster).
Or you can specify projection and clipped area in Environment setting.

Lab 3&4
=======================================================
Lab 3 Land cover change
https://github.com/qiang-yi/GEOG489/blob/master/labs/lab3_assignment.docx
Due March 3rd (Today)

Lab 4 Land cover change
https://github.com/qiang-yi/GEOG489/blob/master/labs/lab4_assignment.docx
Due March 17th
