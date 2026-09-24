# manure-spotter (manure-on-snow detection)
GEE + Python workflow for Random Forest–based manure-on-snow detection from Sentinel-2 and Landsat 8/9, exporting map-ready outputs.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aaronksuiter/manure-spotter-releases/blob/main/manure_spotter_public.ipynb)

This repository contains a Google Earth Engine (GEE) + Python workflow (Colab/Jupyter) that trains and applies a Random Forest classifier to detect potential manure-on-snow signals, on croplands, using Sentinel-2 and Landsat 8/9 imagery. The workflow generates vector detections suitable for mapping and (optionally) exports image chips for rapid human review.

## Requirements
- A Google account with access to Google Earth Engine
- Python 3.10+ (tested in Google Colab)
- Python packages: geemap, earthengine-api, geopandas, shapely (see `requirements.txt`)

## How to run
1. Open `manure_spotter_public.ipynb` in Google Colab.
2. Run the install cell(s) and authenticate Earth Engine.
3. Edit the configuration section (paths + your GEE project/asset root).
4. Run all cells.

## Expected outputs
- Vector detections exported to Google Drive as GeoJSON (destination folder set in the notebook config).
- Optional image-chip exports for each detection (destination folder set in the notebook config).
- (Optional) A trained Random Forest classifier exported to a GEE Asset (if enabled in the notebook).

## Data
Data are available on Zenodo at DOI: 10.5281/zenodo.18225627
