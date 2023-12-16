- `Title`: blockgroup_demographic_data.csv
- `Abstract`: Data table of American Community Survey demographic data by Census Block groups for Harris County, Texas.
- `Spatial Coverage`: Harris County, Texas. [OpenStreetMap Link](https://www.openstreetmap.org/relation/1560395)
- `Spatial Resolution`: Census Block Groups
- `Spatial Reference System`: None
- `Temporal Coverage`: 2012-2017
- `Temporal Resolution`: ACS 5-year estimates
- `Lineage`: https://www.census.gov/programs-surveys/acs/guidance/estimates.html
- `Distribution`: Distributed publicly indefinetely by the US Census.
- `Constraints`: None
- `Data Quality`: None
- `Variables`: For each variable, enter the following information. If you have two or more variables per data source, you may want to present this information in table form (shown below)
  - `Label`: variable name as used in the data or code
  - `Alias`: intuitive natural language name
  - `Definition`: Short description or definition of the variable. Include measurement units in description.
  - `Type`: data type, e.g. character string, integer, real
  - `Accuracy`: e.g. uncertainty of measurements
  - `Domain`: Expected range of Maximum and Minimum of numerical data, or codes or categories of nominal data, or reference to a standard codebook
  - `Missing Data Value(s)`: Values used to represent missing data and frequency of missing data observations
  - `Missing Data Frequency`: Frequency of missing data observations: not yet known for data to be collected

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| GEOID | GEOID | Unique identifier for each block group | Integer | N/A | 482011000001 to 482019801001 | N/A | None |
| BO3002_001 | Total Population | Number of people in the block group | Integer | See ACS | 9-21758 | N/A | None |
| BO3002_003 | White Population | Number of people in the White racial/ethnic group in the block group | Integer | See ACS | 0-9199 | N/A | None |
| BO3002_004 | Black Population | Number of people in the Black racial/ethnic group in the block group | Integer | See ACS | 0-5258  | N/A | None |
| BO3002_006 | Asian Population | Number of people in the Asian racial/ethnic group in the block group | Integer | See ACS | 0-3418 | N/A | None |
| BO3002_012 | Latinx Population | Number of people in the Latinx racial/ethnic group in the block group | Integer | See ACS | 0-11408 | N/A | None |
