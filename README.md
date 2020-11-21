# Thesis

New home for R thesis work

## File Descriptions

**combining_holc_files.RMD:** creates on shapefile containing all of the relevant HOLC city files by combining all the files in the "Shapefiles/Richmond HOLC Files" folder. Adds in variables for city name, state, and map year based on the the HOLC fodler names for each city downloaded from the Richmond Mapping Inequality website.

**overlay_calcs.RMD** takes in the area overlay file from ArcGIS and assigns HOLC grades to each Census tract. Also creates an indicator for any tracts that are less than 50% covered by HOLC areas