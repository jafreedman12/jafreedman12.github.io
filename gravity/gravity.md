---
layout: page
title: Gravity Model of Spatial Interaction
---

The purpose of these two models is to create hospital service zones in line with those created by researchers at the Dartmouth Institute for Health Policy and Clinical Practice. The model for [preprocessing hospital data](https://jafreedman12.github.io/gravity/gravity_models/preprocess_hospital_data.model3) consolidates the number of beds from hospitals in a given zip code into one, central point for the zip code. The [simplified distance matrix](https://jafreedman12.github.io/gravity/gravity_models/distance_matrix_potentialzones.model3) creates hospital service zones based on the friction of distance between the centralized hospital points and surrounding towns. Each hospital cachement zone is constructed of the towns have the highest potential to go to that hospital.

These models can be viewed below here.

![Image of Hospital Preprocessing model](https://jafreedman12.github.io/gravity/gravity_models/hospdata_preprocess.png)

![Image of Simplified Distance Matrix model](https://jafreedman12.github.io/gravity/gravity_models/distmatrix_image.png)

The town boundaries and population data for this analysis was retrieved from the [ACS 2018 5-year average](https://gis4dev.github.io/lessons/02a_gravitymodel.html) (see bottom of page). Hospital points were retrieved from the [U.S. Department of Homeland Security](https://hifld-geoplatform.opendata.arcgis.com/datasets/6ac5e325468c4cb9b905f1728d6fbf0f_0). Hospital Service Area boundaries were gathered from the [Dartmouth Atlas of Healthcare website](https://atlasdata.dartmouth.edu/downloads/supplemental#boundaries), using HSA zones.

When our model is compared to the service regions given by the Dartmouth Health Atlas, there are some apparent discrepancies. Perhaps most notably, our model contains tiny service zones for hospitals that just service a specific town. For example, in Central Massachusetts, the vast majority of patients go to hospitals within the 01605 Zip Code (UMass Medical, UMass Memorial, St. Vincent's), but a small number of patients in Leicester and Clinton appear more likely to go to their local, ~40 bed hospitals.

I would imagine that the Dartmouth Cachement Zones were created with the 'hub and spoke' model, weighting certain hospitals more highly not just by the number of beds but also the services they can provide. In this light, the Leicester and Clinton hospitals are excluded

Errors/shortcomings:
- does not include bodies of water
- uses towns as the statistical service area (zip codes would be more appropriate)
- Another error with this preprocessing model is that rather than creating a centroids of all the hospitals in each town, the model constructs the centroid of the zip code and assigns the number of beds of all hospitals in the zip code to the central point.

link to .model3 files, and inlcude images of our models, which we can store in the assests folder alongside the map

Link to [our map](assets/)!



follow a tutorial on publishing the work to GitHub, ultimately including:
- a model3 file for the gravity model of spatial interaction
- a model3 file for preprocessing hospital data

a GitHub page detailing
- purpose of the models
- data sources and references, including appropriate links
reproducible documentation of methods, where documentation includes…
images of the models
links to the .model3 model files
interpretation of model results vis-a-vis the Dartmouth Health Atlas

a web map of your results with four layers
- hospital clusters
- calculated hospital catchments
- hospital catchments given by the Dartmouth Atlas (you may exclude this one from your static map)
- OSM basemap
