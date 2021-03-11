---
layout: page
title: Gravity Model of Spatial Interaction
---

The purpose of these two models is to create hospital service zones in line with those created by researchers at the Dartmouth Institute for Health Policy and Clinical Practice. The model for [preprocessing hospital data](https://jafreedman12.github.io/gravity/gravity_models/preprocess_hospital_data_v2.model3) consolidates the number of beds from hospitals in a given zip code into one, central point for the zip code. The [simplified distance matrix](https://jafreedman12.github.io/gravity/gravity_models/distance_matrix_potentialzones_v2.model3) creates hospital service zones based on the friction of distance between the centralized hospital points and surrounding towns. Each hospital cachement zone is constructed of the towns have the highest potential to go to that hospital. You can view the final map [here](assets/).

These models can be viewed here:

### [Hospital Preprocessing Model](https://jafreedman12.github.io/gravity/gravity_models/preprocess_hospital_data_v2.model3)
![Image of Hospital Preprocessing model](https://jafreedman12.github.io/gravity/gravity_models/hospdata_preprocess_v2.png)

The hospital points from the [U.S. Department of Homeland Security](https://hifld-geoplatform.opendata.arcgis.com/datasets/6ac5e325468c4cb9b905f1728d6fbf0f_0) were processed to only include hospitals servicing the widest proportion of people (Critical Access, Long Term Care, General Acute Care, Children, Women). This excludes psychiatric, military, and rehabilitation hospitals. All hospitals that have zero beds or are closed are excluded from this analysis. The hospitals are aggregated by zip code and the number of beds from all hospitals in the given zip code are summarized.


### [Simplified Distance Matrix](https://jafreedman12.github.io/gravity/gravity_models/distance_matrix_potentialzones_v2.model3)
![Image of Simplified Distance Matrix model](https://jafreedman12.github.io/gravity/gravity_models/distmatrix_image_v2.png)

This model takes the simplified hospital points (as created above) and town boundaries with population data as gathered from the [ACS 2018 5-year average](https://gis4dev.github.io/lessons/02a_gravitymodel.html). By creating a distance matrix of the hospitals and nearest 20 towns, the potential for visitation is calculated with the weight from number of beds (in hospitals) and population (in each town). The service regions are the aggregations of towns that have the highest potential to visit a given hospital/hospital zip code region.

### Analysis
When our model is compared to the service regions given by the Dartmouth Health Atlas, there are some apparent discrepancies. Our hospital preprocessing model constructs the centroid of all the hospitals in the given area (zip codes here) and assigns the number of beds of all hospitals in the zip code to the central point. This creates some inaccurate hospital service regions, as these zip codes can be very spatially close to one another and do not reflect local patterns of roads and access to certain hospitals. Our analysis does not exclude bodies of water, implying that the friction for travel over lakes, oceans, and rivers is equal to friction of travel over land.

I would imagine that the Dartmouth Cachement Zones were created with the 'hub and spoke' model and the exact zip codes of patients, weighting certain hospitals more highly not just by the number of beds but also the services they can provide. For example, hospitals that have the capacity to handle higher levels of trauma generally have more beds, though this is not always the case with specialized hospitals.

### Data sources (and collaboration!):
- The town boundaries and population data for this analysis was retrieved from the [ACS 2018 5-year average](https://gis4dev.github.io/lessons/02a_gravitymodel.html).
- Hospital points were retrieved from the [U.S. Department of Homeland Security](https://hifld-geoplatform.opendata.arcgis.com/datasets/6ac5e325468c4cb9b905f1728d6fbf0f_0).
- Hospital Service Area boundaries were gathered from the [Dartmouth Atlas of Healthcare website](https://atlasdata.dartmouth.edu/downloads/supplemental#boundaries), using HSA zones. Additional credit is given to the participants and instructors of the GEOG0323 - Open Source GISciences course at Middlebury College (Spring, 2021). Without their help, none of this modeling would have been possible.
