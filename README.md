# BII_Maricopa
Assessing the Biodiversity Intactness Index in Maricopa County

Instructions

## Data access:
#### BII data: This dataset is part of the MPC STAC catalog. You will need to access the ‘io-biodiversity’ collection and look for the 2017 and 2020 rasters covering Phoenix subdivision. You can use the following coordinates for a bounding box: 
[-112.826843, 32.974108, -111.184387, 33.863574]
#### Phoenix subdivision: You will find the Phoenix subdivision polygon in the Census County Subdivision shapefiles for Arizona: https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2022&layergroup=County+Subdivisions

- Create a map showing the Phoenix subdivision within an appropriate geographical context. You may use any vector datasets to create your map. (You can also check out the contextily package.)

- Calculate the percentage of area of the Phoenix subdivision with a BII of at least 0.75 in 2017. Obtain the same calculation for 2020.
HINTS (useful or not depending on your workflow): 
- Let x be an xarray.DataArray. We can select all the values greater than n by simply doing x>n. This will return an xarray.DataArray with boolean values. You can then transform this into an xarray.DataArray with 0s and 1s (instead of True/False) by casting it as type ‘int’. 
- To calculate the percentage area: (pixels in class)/(total pixels) * 100. 

Create a visualization showing the area with BII>=0.75 in 2017 that was lost by 2020. 
