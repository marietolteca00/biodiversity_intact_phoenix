# Biodiversity Intactness Index (BII) in Arizona Phoenix
### Author: Marie Tolteca
### Date: 12-06-2025

# About
This repository explores changes in the Biodiversity Intactness Index (BII) across the Phoenix subdivision between 2017 and 2020 using global 100-meter BII datasets produced by Impact Observatory. The project quantifies the extent of biodiversity loss within the region and visualizes areas where once-intact habitat declined during this period. The analysis uses raster-based spatial processing, geospatial masking, and visualization tools to highlight where BII ≥ 0.75 in 2017 was lost by 2020.

# Data
The Biodiversity Intactness Index (BII) was retrieved via the [Microsoft Planetary Computer STAC Catalog](https://planetarycomputer.microsoft.com/dataset/io-biodiversity#overview). The Arizona boundaries were obtained from the U.S. Census Bureau, which were subsetted to isolate the Phoenix area and used to clip the BII rasters.

# Data Access
To access the data used on this notebook, Download the shapefile for Arizona boundaries from the U.S Census Bureau
- https://www.census.gov/cgi‑bin/geo/shapefiles/index.php?year=2025&layergroup=County+Subdivisions
For the IO- Biodiversity Dataset,use Mircosoft Planetetary Computer STAC Catalog, on the following link,
- https://planetarycomputer.microsoft.com/dataset/io-biodiversity#overview

# Libraries Used
The libraries used in this notebook are the following:
```
import os
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import geopandas as gpd
import rioxarray as rioxr
from shapely import box
import pystac_client
import planetary_computer
import contextily as ctx
import matplotlib.patches as mpatches
from IPython.display import Image 
```

# Repository Structure
### Add data into `.gitignore` to avoid any issue pushing onto github.
```
└── biodiversity_intact_phoenix
    ├── data
    │   └── tl_2025_04_cousub
    │       ├── tl_2025_04_cousub.shp
    ├── final_task2_biodiv_intact.ipynb
    └── README.md
```

### Citation
- Final Project. EDS 220 Working with Environmental Datasets. Task 2: Biodiversity Intactness Index change in Phoenix, AZ. https://meds-eds-220.github.io/MEDS-eds-220-course/assignments/final-project.html
- Microsoft Planetary Computer. io‑biodiversity Dataset. https://planetarycomputer.microsoft.com/dataset/io-biodiversity#overview
- U.S. Census Bureau. 2025TIGER/Line® Shapefiles: County Subdivisions. https://www.census.gov/cgi‑bin/geo/shapefiles/index.php?year=2025&layergroup=County+Subdivisions
