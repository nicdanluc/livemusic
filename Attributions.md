Attributions and Licensing
============


## Attribute Data

### S2401 OCCUPATION BY SEX FOR THE CIVILIAN EMPLOYED POPULATION 16 YEARS AND OVER [2016-2020 American Community Survey 5-Year Estimates]

#### Provided by the United States Census Bureau / American Community Survey.

##### This project uses the "Arts, design, entertainment, sports, and media occupations" field to roughly estimate the population of professional live artists and entertainers as a percent of the civilian employed population 16 years and over within each county.

##### While the ACS measures this statistic for several states and U.S. territories, only data pertaining to D.C. and Maryland are included in this repository.

Referenced in files: `data/count_dat/occuptn/s2401_dc.csv`, `data/count_dat/occuptn/s2401_md.csv`, `data/count_dat/b19_s24_combo.csv`.

Original located at data.census.gov

Used in the public domain.

### B19013 MEDIAN HOUSEHOLD INCOME IN THE PAST 12 MONTHS (IN 2020 INFLATION-ADJUSTED DOLLARS) [2016-2020 American Community Survey 5-Year Estimates]

#### Provided by the United States Census Bureau / American Community Survey.

##### This project uses the "Median household income in the past 12 months (in 2020 inflation-adjusted dollars)" field as supplemental data to compare alongside the population of venues and professional artists.

Referenced in files: `data/count_dat/med_incm/b19_dc.csv`, `data/count_dat/med_incm/b19_md.csv`, `data/count_dat/b19_s24_combo.csv`

Original located at data.census.gov

Used in the public domain.


## Spatial Data

### D.C./Maryland Venue Data (Split across `dc_venues.csv`, `md_venues.csv`, `md_vn_east.csv`)

#### Compiled by Nicholas Dante Lucchetto from free and publicly accessible sources, including:

1. Business listings from OpenStreetMap via several queries of D.C. and the State of Maryland.
2. Select values from the `MusicVenues` feature class of the "Live application services for Maryland" project by Esri, Inc. and the State of Maryland.
	* Only those venues relevant to my research criteria (as outlined in the Readme) are included in my venues.csv file.
	* Located at: https://www.arcgis.com/home/item.html?id=afd462fd42634cd49e0a769b84d303fb
	* No special restrictions or limitations on using, modifying, or redistributing the item's content have been specified.

Geocoded within ArcGIS Pro using ESRI geoprocessing tools with 3rd party geoprocessing servers (see "Geocoding APIs").

Referenced in files: `data/count_dat/num_venues.csv`, `data/count_dat/3VarCorrel.xlsx`.

Located in directory: `data/`

License: Creative Commons Attribution 4.0 International (see `LICENSE.txt` for full details).

### 2021 TIGER/Line Shapefiles: Counties (and equivalent)

#### Provided by the United States Census Bureau Geography Division via TIGER/Line.

##### This project uses TIGER boundaries for counties within D.C. and Maryland clipped from the shapefile containing all U.S. counties.

The unabridged shapefile is **not included** in my repo due to size limitations on GitHub non-LFS uploads. The relevant abridged shapefiles for DC/MD counties only are included in the geodatabase.

Original located at https://www.census.gov/cgi-bin/geo/shapefiles/index.php

Used in the public domain.

### 2021 TIGER/Line Shapefiles: Water

#### Provided by the United States Census Bureau Geography Division via TIGER/Line.

##### This project merges the Area Hydrography shapefiles from several files, for all water-adjacent counties in Maryland, to display the coastline as a contextual feature.

Referenced in directory: `data/coastline/hydrography`.

Original located at https://www.census.gov/cgi-bin/geo/shapefiles/index.php

Used in the public domain.

### Metro Lines Regional (WMATA)

#### Provided by Open Data D.C. / City of Washington, D.C.

##### Used to provide context for access to, and geographical distribution of, venues in relation to the reach of the WMATA (D.C.) Metro system.

Referenced in directory: `data/metrolines/dc_metro`.

Original located at https://opendata.dc.gov/datasets/DCGIS::metro-lines-regional/about

Used under the CC BY 4.0 license (https://creativecommons.org/licenses/by/4.0/).

### Baltimore Metro SubwayLink + Light RailLink Lines

#### Provided by the Maryland Department of Information Technology / State of Maryland.

##### Used to provide context for access to, and geographical distribution of, venues in relation to the reach of the Baltimore Metro Subwaylink and Balitmore Light Raillink systems.

Shapefiles and metadata of the respective systems were downloaded from two separate locations, and thus are designated by different labels which preface their file extensions (`TRAN_BaltimoreMetroSubwayLines_MTA` and `TRAN_LightRailLines_MTA`). However, for simplicity of navigation and use, both systems have been combined into one directory.

Referenced in directory: `data/metrolines/balt_metro`.

Original files for Metro SubwayLink located at: https://data.imap.maryland.gov/datasets/6b4de6f1fc1f498ebf008b9eda56127e/explore?location=39.348419%2C-76.687300%2C12.87

Original files for Light Raillink located at: https://data.imap.maryland.gov/datasets/maryland::maryland-transit-light-rail-lines/explore?location=39.262848%2C-76.624765%2C11.18

Used under a Custom License located at either original source link.


## Geocoding APIs

### MD_AddressPointLocator

#### Provided by the Maryland Department of Information Technology / State of Maryland.

##### Geocoder for the state of Maryland. Uses one row, four table cells per address (Street, City, State, ZIP separated).

Referenced in file: `GeocodeServer on geodata.md.gov.ags`.

Originally located at: https://geodata.md.gov/imap/rest/services/geocodeservices

Documentation/Metadata: https://geodata.md.gov/imap/rest/services/GeocodeServices/MD_AddressPointLocator/GeocodeServer

Used in the public domain.

### DCOZ_Geocoder

#### Provided by the D.C. Office of the Chief Technology Officer.

##### Geocoder for the District of Columbia. Uses one row, one table cell per address (Street, City, State, ZIP combined).

Referenced in file: `DCOZ on maps2.dcgis.dc.gov.ags`.

Originally located at: https://maps2.dcgis.dc.gov/dcgis/rest/services/DCOZ/

Documentation/Metadata: https://maps2.dcgis.dc.gov/dcgis/rest/services/DCOZ/DCOZ_Geocoder/GeocodeServer

Used in the public domain.