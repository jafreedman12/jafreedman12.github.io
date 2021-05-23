---
layout: page
title: Spatial Twitter Blog Post
date: Wednesday, April 28th, 2021
---

### 1. Summarize the analytical techniques applied and how the results of those techniques were communicated in text, numbers, tables, or data visualizations

This analysis was done to assess the spatial patterns of wildfire awareness around San Diego during the wildfires of May, 2014. By filtering tweets for text where "fire" and "wildfire" are included, followed by a more specific filtering of tweets with geographic locations (Bernardo and San Marcos) and coordinate data, these data were used to spatially and temporally analyze wildfire-centered Twitter posts. The spatial patterning of tweets was expressed through a map of Kernel Density Estimation (KDE) (Dual KDE = Cell value of tweets / Cell value of population --> proportional number of tweet in each pixel) of wildfire tweet density. The temporal distribution of tweets about fire/wildfire, along with fires in Bernardo and San Marcos, were expressed through bar charts of tweet frequencies by day. The most frequent conservation topics were determined by a k-means clustering of conversation topics, illuminating the general themes that people were discussing on Twitter. Lastly, the spatial patterns of interconnectivity were explored by how frequently one's tweets were re-tweeted (or how often users retweeted others) through charts and maps illustrating network connectivity of news outlets and government officials. In conclusion, this study finds that the highest density of tweets comes from both the most heavily impacted and densely populated areas, and that networks of sharing knowledge often come from centralized and well-respected sources (news outlets, government officials).


### 2. Consder whether you consider this research paper to be reproducibile and whether you consider this paper to be replicable. Refer to the National Academies of Sciences, Engineering and Medicine definitions of reproducibility and replicability and our prior discussions about GIS as a Science.

I think this analysis by Wang et al. (2016) is both reproducible in the context of wildfires in San Diego and replicable to analysis of natural disasters occurring in other time frames and landscapes. Building on research by the National Academies of Sciences, Engineering, and Medicine (2019), there are opportunities for this research by Wang et al. (2016) to be reproduced in this same context, as they were fairly transparent with their data, methods, and aggregation strategies. I believe that this study could be replicated in other landscapes, although with some modifications towards certain figures and outputs. For example, some of the maps and graphics used by Wang et al. (2016) could be improved for larger contextual understanding, such as Fig. 6, where the spatial distribution of population could be better represented by a dot-density or choropleth map. Within Fig. 5 (Dual Kernel Density), the analysis could be expanded beyond the sharp, county boundaries to provide larger context of the spatial distribution of natural disaster awareness and harm. By improving some of the techniques used in this research, this analysis of spatial patterns of tweets could be replicated to natural disasters in other contexts. Nevertheless, an exact replication of this study would be impossible, as we cannot download the original tweets that were used in this research analysis.


### Works Cited

National Academies of Sciences, Engineering, and Medicine. 2019. *Reproducibility and Replicability in Science*. Washington, D.C.: National Academies Press. [DOI: 10.17226/25303](https://doi.org/10.17226/25303)

Wang, Z., X. Ye, and M. H. Tsou. 2016. Spatial, temporal, and content analysis of Twitter for wildfire hazards. Natural Hazards 83 (1):523–540.
