# Thesis

New home for R thesis work

## File Descriptions

**combining_holc_files.RMD:** creates on shapefile containing all of the relevant HOLC city files by combining all the files in the "Shapefiles/Richmond HOLC Files" folder. Adds in variables for city name, state, and map year based on the the HOLC fodler names for each city downloaded from the Richmond Mapping Inequality website.

**overlay_calcs.RMD** takes in the area overlay file from ArcGIS and assigns HOLC grades to each Census tract. Also creates an indicator for any tracts that are less than 50% covered by HOLC areas and any tract that receives a grade that represents less than 50% of the graded area in that tract. Creates the "all_cities_tract_grades" dataset which holds all the census tracts and assigned grades for analysis. 

**To Generate Data**

1) Combine all files with *combining_holc_files.RMD*
2) Upload resultant shape file *"all_holc_shape_files.shp"* to QGIS
3) Perform intersection with 1960 Census tract boundaries
4) Calculate relevant areas for intersection
5) Save as csv to re-import to r as *"all_cities_overlay.csv"*
6) Run *overlay_calcs.RMD* to produce the final dataset