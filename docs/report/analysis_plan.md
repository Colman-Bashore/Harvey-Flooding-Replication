# Title of Study

### Authors

- Colman Bashore\*, cbashore@middlebury.edu, GitHub: @colman-bashore, Department of Geography, Middlebury College

\* Corresponding author and creator

### Abstract

This study is a reproduction of a Middebury Geography Indroductory GIS Lab problem titled "Exposure to Environmental Hazards: Hurricane Harvey." The original study focused on comparing levels of flooding across block groups of different majority demographics. The original study used the desktop GIS QGIS to determine the majority racial group in every block group in Harris County, Texas and then compared these data to the extent of flooding from Hurricane Harvey. This reproduction study aims to reproduce the same results from the original lab problem using a Python computation notebook (ipynb) as opposed to a desktop GIS workflow. The notebook will potentially serve as an opportunity to demonstrate using Python to complete simple GIS problems in the context of an introductory Human Geography with GIS class. 

[Link to original study prompt](https://drive.google.com/file/d/1l_bylAyBrcuvR5PYj_I3jSKbu04dz5Wh/view)

### Study metadata

- `Key words`: Comma-separated list of keywords (tags) for searchability. Geographers often use one or two keywords each for: theory, geographic context, and methods.
- `Subject`: select from the [BePress Taxonomy](http://digitalcommons.bepress.com/cgi/viewcontent.cgi?article=1008&context=reference)
- `Date created`: November 23, 2023
- `Date modified`: December 17, 2023
- `Spatial Coverage`: Harris County, Texas [OpenStreetMap Link](https://www.openstreetmap.org/relation/1560395)
- `Spatial Resolution`: Census Block Group Level
- `Spatial Reference System`: EPSG:4326
- `Temporal Coverage`: September 2017
- `Temporal Resolution`: Yearly Census Data
- `Funding Name`: Middlebury College
- `Funding Title`: N/A
- `Award info URI`: N/A
- `Award number`: N/A

#### Original study spatio-temporal metadata

- `Spatial Coverage`: Harris County, Texas [OpenStreetMap Link](https://www.openstreetmap.org/relation/1560395)
- `Spatial Resolution`: Census Block Group Level
- `Spatial Reference System`: EPSG:4326
- `Temporal Coverage`: September 2017
- `Temporal Resolution`: Yearly Census Data

## Study design

Describe how the study relates to prior literature, e.g. is it a **original study**, **meta-analysis study**, **reproduction study**, **reanalysis study**, or **replication study**?

Also describe the original study archetype, e.g. is it **observational**, **experimental**, **quasi-experimental**, or **exploratory**?

Enumerate specific **hypotheses** to be tested or **research questions** to be investigated here, and specify the type of method, statistical test or model to be used on the hypothesis or question.

## Materials and procedure

### Computational environment

While the original study exlusively used QGIS this reproduction will use a Python computational notebook (ipynb).

### Data and variables

Describe the **data sources** and **variables** to be used.
Data sources may include plans for observing and recording **primary data** or descriptions of **secondary data**.
For secondary data sources with numerous variables, the analysis plan authors may focus on documenting only the variables intended for use in the study.

Primary data sources for the study are to include ... .
Secondary data sources for the study are to include ... .

blockgroups.shp
◦ Block Groups of Harris County, Texas
◦ One block group contains only 9 people, but you may include all block groups in your analysis.
◦ Source: United States Census API https://www.census.gov/developers/ via R tidycensus
https://walkerke.github.io/tidycensus

blockgroup_demographic_data.csv
◦ Data table of block group demographics.
◦ Explanation of attribute variable codes from this 5-year American Community Survey 2012-2017 data are found in
block group metadata.xls
◦ Source: United States Census API https://www.census.gov/developers/ via Rtidycensus
https://walkerke.github.io/tidycensus

predicted_flood.shp
◦ This vector layer contains FEMA’s 100-yr flood zones for Harris County. A 100-year flood zone indicates a 1%
chance of flooding every year.
◦ Source: FEMA’s National Flood Hazard Layer (NFHL) Viewer https://hazards-
fema.maps.arcgis.com/apps/webappviewer/index.html?id=8b0adb51996444d4879338b5529aa9cd

actual_flood.shp
◦ This vector layer contains FEMA’s 100-yr flood zones for Harris County. A 100-year flood zone indicates a 1%
chance of flooding every year.
◦ Source: FEMA’s National Flood Hazard Layer (NFHL) Viewer https://hazards-
fema.maps.arcgis.com/apps/webappviewer/index.html?id=8b0adb51996444d4879338b5529aa9cd

actual_flood_10.tif
◦ This raster layer contains the value 1 in each cell that was flooded and nodata (raster equivalent of
NULL) in all other locations.
◦ The layer's coordinate system units are meters, and the cell size is 10 meters by 10 meters.
◦ Sources: The Flood Observatory https://floodobservatory.colorado.edu/ and the Harris County Flood
Control District: https://www.hcfcd.org/Hurricane-Harvey


Each of the next subsections describes one data source.

### Prior observations  

At the time of this study pre-registration, the authors had completed the original lab problem focusing on the Hurricane Harvey flooding using qgis.
This study is related to no prior studies by the authors

For each secondary source, declare the extent to which authors had already engaged with the data:

- [ ] data is not available yet
- [ ] data is available, but only metadata has been observed
- [ ] metadata and descriptive statistics have been observed
- [x] metadata and a pilot test subset or sample of the full dataset have been observed
- [ ] the full dataset has been observed. Explain how authors have already manipulated / explored the data.

If pilot test data has been collected or acquired, describe how the researchers observed and analyzed the pilot test, and the extent to which the pilot test influenced the research design.

### Bias and threats to validity

Given the research design and primary data to be collected and/or secondary data to be used, discuss common threats to validity and the approach to mitigating those threats, with an emphasis on geographic threats to validity.

These include:
  - uneven primary data collection due to geographic inaccessibility or other constraints
  - multiple hypothesis testing
  - edge or boundary effects
  - the modifiable areal unit problem
  - nonstationarity
  - spatial dependence or autocorrelation
  - temporal dependence or autocorrelation
  - spatial scale dependency
  - spatial anisotropies
  - confusion of spatial and a-spatial causation
  - ecological fallacy
  - uncertainty e.g. from spatial disaggregation, anonymization, differential privacy

One of the main geographic threat to validity in this study is the modifiable areal unit problem. In the case of the original study the data sources are aggregated at the level of census block groups. In many cases the unit of aggregation used for a study can dramatically change the output of an analysis. For example, the map of majority racial groups in Harris County aggregated at the block group level would be much more complex than a map at the tract level but it would not be as detailed may show different trends than a map produced with data at the block level. The original study unit size is based upon the scale of data available, which often determines the unit used. However, we cannot be sure that the results of our analysis wouldn't be different if we used a finer unit of analysis, therefore the unit of aggregation is a threat to validity in this study. Additionally, another threat to this study is the confusion of spatial and a-spatial causation. Flooding is an example of a variable that is often considered to be based exlusivily on the physical geographic of a place. However, this may lead to a lack of focus on variables such as emergency preparedness that may impact the extent of flooding. Another threat to validity is the common assumption that all locations within a delineated region are the same. In the case of the Harvey flooding study we may see that a region that has a predominantly white population has a lot of flooding, but we are not taking into consideration the distribution of population within that area and cannot tell whether the flooding in that region is overlapping with the white population or if there are other factors at play such as flooding in undeveloped wetlands within the region, which would not have a significant human geography impact. Finally, there may be a boundary effect from the border of Harris County. The northwest border of Harris County is a river, thus it follows that the lowland area surrounding it would be more likely to flood. Thus, by not extending the extent of the study, we may see higher flooded percentages in regions that touch this border. 

### Data transformations

Describe all data transformations planned to prepare data sources for analysis.
This section should explain with the fullest detail possible how to transform data from the **raw** state at the time of acquisition or observation, to the pre-processed **derived** state ready for the main analysis.
Including steps to check and mitigate sources of **bias** and **threats to validity**.
The method may anticipate **contingencies**, e.g. tests for normality and alternative decisions to make based on the results of the test.
More specifically, all the **geographic** and **variable** transformations required to prepare input data as described in the data and variables section above to match the study's spatio-temporal characteristics as described in the study metadata and study design sections.
Visual workflow diagrams may help communicate the methodology in this section.

Examples of **geographic** transformations include coordinate system transformations, aggregation, disaggregation, spatial interpolation, distance calculations, zonal statistics, etc.

Examples of **variable** transformations include standardization, normalization, constructed variables, imputation, classification, etc.

Be sure to include any steps planned to **exclude** observations with *missing* or *outlier* data, to **group** observations by *attribute* or *geographic* criteria, or to **impute** missing data or apply spatial or temporal **interpolation**.

#### Goal 1: Load census data into block groups 

The first step of the workflow is to join blockgroup_demographic_data.csv dataframe data to the blockgroups shapefile by the join field "GEOID." This will create a new shapefile/geodataframe we call bgData.shp that will contain block group geometries and demographic data.

#### Goal 2: Create regions by majority groups

First step of goal 2 is calculate new fields is bgData.shp. These new fields will be pctAsian, pctBlack, pctLatinx, pctWhite. 
The next step will be to calculate another field named majorGrp which will take the value of the name of a racial group if that group makes up more than 60% of the population of that block group. If no group takes up more than 60% then the block group is labelled as "mixed." Next we will group blocks by majority group and dissolve adjacent block groups of the same majority groups. This will create a new shapefile named major_grps.

#### Goal 3: Find flooded area in each group and calculate pct.

First step of goal 3 is to run a zonal statistic on actual_flood_10.tif and major_grps which will calculate the area of each majority group region that was flooded during the hurricane. This new layer will be named bgMajFlood. We will then calculate new fields in this layer. These fields will be flooded area, total area, and then percentage flood based on the previous two fields. 


### Analysis

We are trying to describe the spatial patterns of environmental justice in Harris County and the main way we will do this is by calculating the percentage flooded in each of the majority group regions. 

## Results

We will present our results in table and graph form as well as producing two main maps. One map of the majority racial group regions and actual flooded areas. The second map will show percent flooded by majority group regions. 


## Discussion

We will discuss how this study reveals the patterns of environmental justice in Harris County as well as how our use of a reproducible python notebook more easily allows our study to be modified and expanded upon. 

## Integrity Statement

Include an integrity statement - The authors of this preregistration state that they completed this preregistration to the best of their knowledge and that no other preregistration exists pertaining to the same hypotheses and research.
If a prior registration *does* exist, explain the rationale for revising the registration here.

## Acknowledgements

- `Funding Name`: name of funding for the project
- `Funding Title`: title of project grant
- `Award info URI`: web address for award information
- `Award number`: award number

This report is based upon the template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences, DOI:[10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)

## References
