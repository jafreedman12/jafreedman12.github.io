---
layout: page
title: Gravity Model of Spatial Interaction
---

The purpose of these two models is to create hospital service zones in line with those created by researchers at the Dartmouth Institute for Health Policy and Clinical Practice. The model for [preprocessing hospital data](https://jafreedman12.github.io/gravity/gravity_models/preprocess_hospital_data.model3) consolidates the number of beds from hospitals in a given zip code into one, central point for the zip code. The [simplified distance matrix](https://jafreedman12.github.io/gravity/gravity_models/distance_matrix_potentialzones.model3) creates hospital service zones based on the friction of distance between the centralized hospital points and surrounding towns. Each hospital cachement zone is constructed of the towns have the highest potential to go to that hospital. You can find the final map [here](assets/)!

These models can be viewed here:

**[Hospital Preprocessing Model](https://jafreedman12.github.io/gravity/gravity_models/preprocess_hospital_data.model3)**
![Image of Hospital Preprocessing model](https://jafreedman12.github.io/gravity/gravity_models/hospdata_preprocess.png)

The hospital points from the [U.S. Department of Homeland Security](https://hifld-geoplatform.opendata.arcgis.com/datasets/6ac5e325468c4cb9b905f1728d6fbf0f_0) were processed to only include hospitals servicing the widest proportion of people (Critical Access, Long Term Care, General Acute Care, Children, Women). This excludes psychiatric, military, and rehabilitation hospitals. All hospitals that have zero beds or are closed are excluded from this analysis 


**[Simplified Distance Matrix](https://jafreedman12.github.io/gravity/gravity_models/distance_matrix_potentialzones.model3)**
![Image of Simplified Distance Matrix model](https://jafreedman12.github.io/gravity/gravity_models/distmatrix_image.png)

When our model is compared to the service regions given by the Dartmouth Health Atlas, there are some apparent discrepancies. Our hospital preprocessing model constructs the centroid of all the hospitals in the given area (zip codes here) and assigns the number of beds of all hospitals in the zip code to the central point. In addition, both our preprocessing and distance matrix models contain tiny service zones for hospitals that just service a specific town. For example, in Central Massachusetts, the vast majority of patients go to hospitals within the 01605 Zip Code (UMass Medical, UMass Memorial, St. Vincent's), but a small number of patients in Leicester and Clinton appear more likely to go to their local, ~40 bed hospitals. ![Central Massachusetts Hospital zones](put the image link). Our analysis does not exclude bodies of water, implying that the friction for travel over lakes, oceans, and rivers is equal to friction of travel over land.

I would imagine that the Dartmouth Cachement Zones were created with the 'hub and spoke' model, weighting certain hospitals more highly not just by the number of beds but also the services they can provide. In the example provided above, the Leicester and Clinton hospitals would likely be excluded in favor of the larger hospitals in Worcester. 

The town boundaries and population data for this analysis was retrieved from the [ACS 2018 5-year average](https://gis4dev.github.io/lessons/02a_gravitymodel.html) (see bottom of page). Hospital points were retrieved from the [U.S. Department of Homeland Security](https://hifld-geoplatform.opendata.arcgis.com/datasets/6ac5e325468c4cb9b905f1728d6fbf0f_0). Hospital Service Area boundaries were gathered from the [Dartmouth Atlas of Healthcare website](https://atlasdata.dartmouth.edu/downloads/supplemental#boundaries), using HSA zones. Additional credit is given to the participants and instructors of the GEOG0323 - Open Source GISciences course at Middlebury College (Spring, 2021). Without their help, none of this modeling would have been possible.
