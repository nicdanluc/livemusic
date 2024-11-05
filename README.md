Dollars and Cents: Mapping the Accessibility of Local Live Music
============
## (in D.C. and Maryland)

![](https://github.com/DanteNaimo/dev2-livemusic/blob/main/livemusic_poster.png)

***Dollars and Cents*** is a project designed to explore the accessibility of a stable career in the live music performance field, primarily through spatial analysis.

This project attempts to understand the career prospects of field through the **lens of geographical accessibility**. It aims to analyze some present-day conditions for beginning and sustaining a career in live music while eliminating as many extraneous variables as possible.

This spatial analysis of the relationship between venue location and artist population spread aims to visualize the convenience of accessing D.C. and Maryland's music venues to the professional artists who depend on them for income and inspiration.

____The District of Columbia and the State of Maryland were established as the two sample research areas mainly out of my interest in how two metro areas in close proximity to each other (Washington, D.C., and Baltimore) may compare statistically (alongside my personal curiosity about the east coast live music scene.)
________e

#### Major Contributors

Map Author: Nicholas Dante Lucchetto

Instruction and Feedback: Dr. Craig Dalton, Hofstra University Department of Global Studies and Geography

Compiled for the GEOG160 Intermediate GIS Course at Hofstra University, taught by Dr. Craig Dalton

#### Research Question

Do full-time musicians and performers have convenient, adequate access to live music venues for paid gig work and inspiration?

#### Hypothesis

Counties with a greater % of the population who identified as professional artists (`% Prof. Artists`) will contain a greater number of venues, assuming that an artistically-vibrant community can attract and sustain the business of venues. Thus, musical artists in these counties maintain adequate access to employment and cultural enrichment tailored to their profession. Inversely, in counties with a lower `% Prof. Artists`, fewer venues will be operational, and thus possess poor accessibility to professional success factors.

#### Methodology

I compared the number of dedicated music venues per county within the research area with the percentage of employed civilians per county who self-identified as professional artists or entertainers on the 2020 American Community Survey 5-Year Estimates (ACS).

* This percentage (`% Prof. Artists`) is calculated by dividing the total number of professional artists per county by the total employed civilian population over the age of 16 per county (included in the ACS). `% Prof. Artists` is calculated exclusively from the employed population of each county, rather than the entire county population, to eliminate the extraneous influences of unemployment and retirement.

I have included businesses as "dedicated music venues" only if I identified that each has met the following criteria:

	1. The venue must be an operational business in Maryland or the District of Columbia as of this project's completion (May 2022).
	2. The venue offers live music performances as its primary attraction (which ensures that the venue operator books several artists to perform regularly).
	3. The venue consistently hosts and attracts professional artists from its surrounding communities.

Individual venues are represented by their accurate locations on the map (through the use of geocoders), or the unlabeled red diamonds found on the final poster (`livemusic_poster.png`). Geocoding the exact locations of all venues allows for several observations regarding their spatial distribution - an especially important detail when considering the logistics of transportation to and from these destinations.

The `% Prof. Artists` variable is represented on the map with graduated colors specific to each county, following a 5-color scale (which is displayed on the right of the large map included on `livemusic_poster.png`).

Counties that are both darkly shaded and enclose a dense concentration of venues are counties deemed to have convenient and adequate access to live music for professional artists.

Correlation calculations have been run to numerically represent the average association between the total number of venues and three variables across all counties, all of which I considered to have a potentially significant association with venue population:

	1. % Prof. Artists
	2. Total Employed Population
	3. Median Income

The results of these calculations can be found in the footer of the final poster (`livemusic_poster.png`) or in `3VarCorrel.xlsx`. A deeper explanation of my calculation process is located in `CorrelCalcMethod.txt`.

#### Conclusion

Spatial analysis conducted through this method reveals a strong association between the presence of full-time professional musicians and performers in each county (`% Prof. Artists`) and the number of local live music venues, supporting a close association between the two variables.

Local venues are especially prominent in the D.C. and Baltimore metropolitan areas, where some of the highest shares of employed people over 16 years of age are professional artists. Generally, fewer venues are in counties where lower shares of professional artists live - and no local live music venues are present in counties where the share of professional artists is fewer than 1.20% of the employed.

One could also reasonably conclude from this data that artists across these counties, but especially in the cities of D.C. and Baltimore, generally enjoy adequately accessible spaces to share their work and be compensated for their talents.

The strong correlation coefficient between total venues and the share of professional artists shows a level of association exceeding that of the two other potentially extraneous variables that were compared.

#### Further Questions and Improvements

Recalculating correlation on a different region which holds a larger sample size of venues, and perhaps collecting data on the artist population through a survey which could ask more specific questions relating to this project's cause than the Census (which also combines several adjacent professions into the Artists classification, potentially skewing the current data), could both improve the accuracy of this project (if such data becomes publicly available). For now, since the Census provides a database that holds quite a broad reach across the population, it stands as a reasonable substitute for new, manually collected artist population data.

Going forward, I would be interested in researching how a high presence of both music venues and local musicians in one community influence each other in a real-world setting, and whether more of either population truly creates a better environment for the other.

* Is it reasonable to assume that professional musicians obtain higher odds of achieving financial stability when they are located near such venues?
* Is it also reasonable to assume that live music venues are likely to remain in business when they are located within an artistically vibrant community?

## Repo, Software Tools, Adaptation

#### Root Contents Overview

1. ArcGIS Project File (`160final.aprx`), Geodatabase (`160final.gdb`), and other dependent files/directories (`160final.tbx`, `ImportLog`, `Index`)
2. Raw Data (`data` folder)
	* A shapefile for U.S. counties was utilized in this project but is **not included** in my repo due to size limitations on GitHub non-LFS uploads. The more relevant, abridged shapefiles for DC/MD counties only are included in the geodatabase.
3. Methods Used for Calculating Correlation (`CorrelCalcMethod.txt`)
4. Geocoder References (all ending in `.ags`)
5. Overall Project License (`LICENSE.txt`)
6. Attributions and Use Cases for All Data (`Attributions.md`)
7. Complete Poster for Map and Data Display (`livemusic_poster.png`)

#### Software Utilized

1. **Esri ArcGIS Pro - Advanced** (Plotting and Geoprocessing)

2. **Microsoft Excel** (Data Collection and Calculations)

3. **Adobe Illustrator** (Final Map Design)

#### Geoprocessing Tools

1. **Spatial Join** (Joining multiple layers of geocoded points onto one combined layer)

2. **Add Join (Table Joins)** (Joining databases)

3. **Geocode Addresses** (Precisely locating venues from attached databases using geocoding servers)

#### Adaptations and Open Data Statement

1. This project uses entirely free and publicly accessible data to fulfill its purpose, accompanied by licenses that permit the public use and redistribution of such data.
2. I have simplified my file structure as much as possible to allow for any inspired projects to follow the same common workflow - whether these projects analyze the same or different industries, regions, or populations.
3. This is a learning experience for me - and my first independent research project using GIS tools. My methods in analyzing population factors and spatial properties should be transparent, as I believe that with critique, refining, and feedback, my methods here can significantly improve in the future (more in the "Further Questions and Improvements" section).
