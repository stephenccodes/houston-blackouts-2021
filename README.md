# Houston Winter Blackouts of 2021
## Analyzing deomgraphic correlation

By [Stephen Carroll](https://stephenccodes.github.io./) [@stephenccodes](https://github.com/stephenccodes)

## About

In February 2021, Texas faced a series of severe winter storms that highlighted vulnerabilities in the state's power grid. The resulting power outages had a disproportionate impact on different socioeconomic groups in Houston. This analysis uses four datasets (VIIRS, roads, housing, and socioeconomic data) to examine the effects of these outages on Houston's residents, with a focus on how the distribution of outages relates to median household income.

## Skills

This analysis harnesses the following skills:

- Vectorizing rasters

- Buffering features

- Reclassifying rasters

- Transforming Coordinate Reference Systems

- Mapping with tmap

- Masking rasters


The `stars` and `terra` packages were useful for working with raster data, and the `sf` package was used for working with vector data. 

## Repository Structure
```
├── houston_blackouts_files
├── .gitignore
├── houston_blackouts.Rproj
├── houston_blackouts.html # Rendered document
├── houston_blackouts.qmd # Quarto document detailing the analysis
└── README.md
```
## Data Access

All the data used in this analysis was downloaded from a pre-prepared [Google Drive](https://drive.google.com/file/d/1bTk62xwOzBqWmmT791SbYbHxnCdjmBtw/view?usp=drive_link). It was downloaded, unzipped, and housed in a data/ folder that was not pushed to the repository due to its size. The data in the drive was originally obtained from the following sources:

**VIIRS Data:**

The [Visible Infrared Imaging Radiometer Suite (VIIRS)](https://ladsweb.modaps.eosdis.nasa.gov/) data is remotely-sensed night lights data acquired from the Suomi satellite. It includes 4 files: two tiles (h08v05 and h08v06) per date (2021-02-07 and 2021-02-16). Those dates were chosen due to the least cloud cover, allowing for the best contrast in night lights during the power crisis.

**Roads and Houses Data:**

[Geofabrik's download site](https://download.geofabrik.de/) is a third-party distributor for [OpenStreetMap (OSM)](https://planet.openstreetmap.org/) data. Here, we can find roads and houses data for Texas (downloaded as .gpkg files).

**Socioeconomic Data:**

The [U.S. Census Bureau's American Community Survey](https://www.census.gov/programs-surveys/acs) data is census-tract level data from 2019 (downloaded as a .gbd file). 

## References & Acknowledgements

All materials were created by [Ruth Oliver](https://github.com/ryoliver) for EDS-223.

GeoFabrik. (2024). Shapefiles [Roads, Houses]. Retrieved from [https://download.geofabrik.de/](https://download.geofabrik.de/)

NASA LAADS DAAC. (2021). VIIRS [Night Light]. NASA EOSDIS Land, Atmosphere Near Real-Time Distributed Active Archive Center. Retrieved from [https://viirsland.gsfc.nasa.gov/Val_overview.html](https://viirsland.gsfc.nasa.gov/Val_overview.html)

U.S. Census Bureau. (2024). American Community Survey. U.S. Department of Commerce. Retrieved from [https://www.census.gov/programs-surveys/acs](https://www.census.gov/programs-surveys/acs)
