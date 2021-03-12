---
layout: page
title: Error and Uncertainty in GIS
date: Friday, March 12th, 2021
---

- ways that space is represented are never complete -- leads to uncertainty, creates problems
- impossible to make an accurate representation of the world -- you can never tell every story of every place with one map


I am particularly interested in your interpretation and reaction to figure 6.1 in Longley et al (2008) with regards to the three questions/prompts below:

- accuracy -- discrepancy of reality and our representation of reality (Gerard Heuvelink)
- real world to analysis leads to data distortion. I'd go one step further to say this is a cycle -- there are a lot of distortions in regards to understandings of the "real world" going into this, as our perceptions of the world around us are shaped by maps and representations we've seen before. 

- ## Do you have first-hand knowledge or experience with uncertainty in spatial/geographic research?

In many cases

Through my senior thesis, I am researching inclusive mapping in the field of environmental conservation. A big issue with maps is that they are taken to be a completely factual representation of a place, and cartographers do little to dissuade these assumptions. 

- Data quality -- helping people understand legitimacy of data. Lots of scenarios where its obscured
- units of analysis are incredibly important, also lead to distortion
representation of space/relationships can't always be shown in a 2D, grid/coordinate based way -- there are relationships and units that go beyond the spatially plottable
- vagueness in plottable data (aggregation, boundaries, etc.)
- historic data -- how do we make accurate data-driven maps of the past
- automations of represenations. Fuzzy, subjective probabilities (i.e. soil mapping). Field testing with remote sensing can help -- assessing accuracy
- crisp drawing of boundaries is frequent when there arent crisp boundaries. Raster vs. Vector -- raster might have more info/accurate/up-front abt probabilities, but vector seems easier to read, maybe more of a generalization
- Confusion matrices
- accuracy and precision -- GPS that always gives same reading @ elevation (precise), but is 5m too high (inaccurate)


- ## What responsibilties do geographers have with regards to uncertainty in research?
Deeper investigation of data sources and accuracy -- there's been an ecouragement to be accuracte to 0.5mm at scale of map, but this doesnt always mean a point is where it should be. As scale of map increases 1:100 --> 1:10000000, that 0.5mm accuracy means something different. Maybe off by 0.5m on the groud in 1:100, but off by 5000m in 1:10000000
lots of data that isnt well documented
internal validation of errors with GIS
uncertain vs. crisp bounaries -- putting data disclaimers into work, explaining why they make the choices they do. Openly acknowledge uncertainty in data -- ask for questioning and confirmation in all our research


- ## What strategies might geographers use to fulfill those responsibilities?
spatial autocorrelation -- relationships of errors at different places --> spatial elevation errors in DEMS often happen in patterns, not every unique pixel


### Works cited:

- NASEM. 2019. Reproducibility and Replicability in Science. Washington, D.C.: National Academies Press. https://www.nap.edu/catalog/25303.
- Longley, P. A., M. F. Goodchild, D. J. Maguire, and D. W. Rhind. 2008. Geographical information systems and science 2nd ed. Chichester: Wiley. (only chapter 6: Uncertainty, pages 127-153)
