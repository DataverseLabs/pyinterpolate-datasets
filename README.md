# pyinterpolate-datasets

Datasets used throughout tutorials and examples in `pyinterpolate` [Pyinterpolate Repository](https://github.com/DataverseLabs/pyinterpolate) 

## Datasets



### Point Kriging

#### `csv`

- `pl_dem.csv` : sample of DEM readings for region near the Polish city Gorzow Wielkopolski. Sample retrieved from *Copernicus Land Monitoring Service*, [EU-DEM dataset](https://land.copernicus.eu/imagery-in-situ/eu-dem).
- `meuse/meuse.csv` and `meuse/meuse_grid.csv` : from Pebesma, Edzer. (2009). The meuse data set: a tutorial for the gstat R package. URL: https://cran.r-project.org/web/packages/gstat/vignettes/gstat.pdf

#### `numpy`

- `armstrong_data` : data from book *Basic Linear Geostatistics* written by **Margaret Armstrong** with DOI: [https://doi.org/10.1007/978-3-642-58727-6](https://doi.org/10.1007/978-3-642-58727-6)

#### `txt`

- `pl_dem.txt` : see `pl_dem.csv`,
- `pl_dem_epsg2180.txt` : the same dataset as `pl_dem.txt` but reprojected to metric system.

---

### Block Kriging

#### `cancer_data.gpkg`

Breast cancer rates are taken from the Incidence Rate Report for U.S. counties and were clipped to the counties of the Northeastern part of U.S. [National Cancer Institute - Incidence Rates Table: Breast Cancer: Pennsylvania State](https://www.statecancerprofiles.cancer.gov/incidencerates/index.php?stateFIPS=42&areatype=county&cancer=055&race=00&sex=2&age=001&stage=999&year=0&type=incd&sortVariableName=rate&sortOrder=default&output=0#results). Observations are age-adjusted and multiplied by 100,000 for the period 2013-2017.

Population centroids are retrieved from the U.S. Census Blocks 2010 [United States Census Bureau - Centers of Population for the 2010 Census](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.2010.html). Breast cancer affects only females but for this example the whole population for an area was included. Raw and transformed datasets are available in a dedicated Github repository.

**meta**:

- **block / polygon layer**: `areas`,
- **point support / population layer**: `points`,
- **point support value**: `POP10`,
- **block and point support geometry column**: `geometry`,
- **block index column**: `FIPS`,
- **block values column**: `rate`.
- [Raw data and transformation steps](https://github.com/SimonMolinsky/pyinterpolate-paper/tree/main/paper-examples/example-use-case/raw)


