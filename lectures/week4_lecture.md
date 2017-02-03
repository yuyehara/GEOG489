<!-- $theme: gaia -->


# Applied GIS (GEOG 489)
**Week 4: Suitability Modeling (Case studies)**
Slides of this class: https://git.io/vDG0Q

<br>
Instructor: Yi Qiang

Email: yi.qiang@hawaii.edu

---
# Recall: Basic steps of suitability modeling
1. Defining criteria
2. Mapping criteria
3. Standardize criteria
4. Assigning weights
5. Combining into final suitability map

---
# Example 1: Wind and solar farm

Janke, J. R. (2010). **Multicriteria GIS modeling of wind and solar farms in Colorado**. *Renewable Energy*, 35(10), 2228-2234.[pdf](../readings/suitability_modeling/Janke_2010.pdf)


---
# Objective
<img src="../labs/lab2_data/misc/objective.png" width="800">

---
##### Study Area (Colorado)
<img src="../labs/lab2_data/misc/co.png" width="800">

---
# Defining Criteria
![]()
<img src="../labs/lab2_data/misc/CO_criteria1.png" width="900">

---
#### Identifying Data and Mapping Criteria
<img src="../labs/lab2_data/misc/CO_criteriamapping.png" width="800">

---
Authors' comment on raster and vector
<img src="../labs/lab2_data/misc/CO_comment.png" width="1100">

---
# Mapping Criteria
<img src="../labs/lab2_data/misc/mapped_criteria.png" width="1100">

---
### Standardize Criteria and Assign Weights
<img src="../labs/lab2_data/misc/CO_weight.png" width="650">

---
###  Final suitability score of wind farm

<img src="../labs/lab2_data/misc/wind_farm.png" width="800">

---
###  Final suitability score of solar farm
<img src="../labs/lab2_data/misc/solar_farm.png" width="800">

---
#### Example 2: Find suitable locations for wetland mitigation sites
<br>

Van Lonkhuyzen, R. A., LaGory, K. E., & Kuiper, J. A. (2004). **Modeling the suitability of potential wetland mitigation sites with a geographic information system**. *Environmental Management*, 33(3), 368-375.[pdf](../readings/vanlonkhuyzen.pdf)

<br><br>
Study site: DuPage County, Illinois, USA

---
Criteria and weights
<img src="../labs/lab2_data/misc/criteria.png" width="1600">

---
##### Mapping Criteria
<img src="../labs/lab2_data/misc/criteria_map.png" width="500">

---
### Equation used to combine criteria
<img src="../labs/lab2_data/misc/multiply_combine.png" width="900">

---
## Final output
<img src="../labs/lab2_data/misc/final.png" width="900">

---
# Question:
# What is the major issue of the above analyses?
---
# The linear weighted combination is too arbitary
* Subjective suitability score for each criterion
* Subjective weghts
* Subjective equation to combine criteria
* No empirical analysis
* No validation
---
# Example 3: Sensitivity Analysis

##### Test how the suitability map differs with different weights

Chen, Y., Yu, J., & Khan, S. (2010). **Spatial sensitivity analysis of multi-criteria weights in GIS-based land suitability evaluation**. *Environmental Modelling & Software*, 25(12), 1582-1591.[pdf](../readings/Chen_2010.pdf)

---
# Model to be tested 
Suitability for irritated cropping landuse in Queensland, Australia

<img src="../labs/lab2_data/misc/au_studyarea.png" width="500">

---
# Criteria 
* Rank suitability of each criteria
<img src="../labs/lab2_data/misc/au_criteria.png" width="1000">

---
* Define benchmark wegiths using Analytical Hierarchy Process
<img src="../labs/lab2_data/misc/ahp.png" width="600">

---
#### Simulation by changing the weight of KS
<img src="../labs/lab2_data/misc/simulation.png" width="1000">

---
* Some tipping point can be found - suitability map changes significantly with only a small change of the weight 
<img src="../labs/lab2_data/misc/sensitivity.png" width="1000">

---
## Example 4: Predict Wolf Habitat Suitability

Glenz, C., Massolo, A., Kuonen, D., & Schlaepfer, R. (2001). **A wolf habitat suitability prediction study in Valais (Switzerland)**. *Landscape and Urban Planning*, 55(1), 55-65.[pdf](../readings/Glenz_2001.pdf)

---
# Study Area
<img src="../labs/lab2_data/misc/valais.jpg" width="580"><img src="../labs/lab2_data/misc/valais_tour.jpg" width="280">
Canton of Vailas, Switzerland

---
# Criteria and data source
<img src="../labs/lab2_data/misc/CH_criteria.png" width="900">

---
# Criteria Mapping

Data for the calculation of the wild ungulate diversity index were in **numerical and cartographical form** and have been processed for further analysis in GIS. **The habitat variables were calculated on a 4 km<sup>2</sup> grid**, in order to consider pronounced variations of the geo-morphological conditions in the study region, as well as its environmental and demographic peculiarities.

---
# Building Equation
* An empirical study using logistic regression model
* Building relation (equation) between wolf presence and environmental variables

<img src="../labs/lab2_data/misc/log_reg.jpg" width="1000">

---
# Building Equation

<img src="../labs/lab2_data/misc/log_coef.png" width="1000">

---
# Estimating Wolf Presence Probability

<img src="../labs/lab2_data/misc/CH_suitability.jpg" width="700">

---
#### With empirical analysis, the equation and weights are not subjective. <br><br>
#### Question: Any other issues with this approach?

---

#### Logistic regression still assumes a linear relation between suitability and criteria, which is not usually true in the real-world.

---
# Some thinkings
* What are the difference of using vector/raster in suitability modeling, and what are the pros and cons.
* What are the major issues in suitability modeling? What are the solutions?

---
# Continue Lab Exercise 2:
Download the assignment from **https://git.io/vDeAZ**


Submission due Feb. 17