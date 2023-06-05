Jacob Arnold
21-jul-2021

Using .e00 files. 
These must be converted to shapefiles in order to use them. 
Unfortunately this is not easy, it can be done with arcGIS one file at a time. 
There were however ~ 2000 files to convert so that was not an option. 

~~~TWO EXAMPLES ARE PROVIDED AND RENAMED read_e00_Year and CtoF_year

Open source software AVCE00 with program avcimport facillitates conversion of .e00 files to ArcInfo binary coverages
Open source software GDAL with program ogr2ogr facillitates conversion of ArcInfo coverages to shapefiles

simply loop through all files and run avcimport <filename.e00> <outdirectory name>  
next loop throgh the newly generated coverage directories running ogr2ogr -f "ESRI Shapefile" <out shapefile dir name> <in coverage dir name>

executable files read_e00 (in each year's directory) and CtoF (in year/Convert1) do this. 

Note 1997-2000 the data are divided into 6 regions
     2001-2002 the data are hemispheric so they are named differently and the read_e00 and CtoF programs are altered accordingly

final output data is to be found in year/Convert2


*******THE PAL series of shapefiles data seem to be the correct ones, the others house less/incomplete polygon information.*********


converted data can be read in matalb with data = m_shaperead('filename_withNOextension')
 

