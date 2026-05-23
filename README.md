# MAST Tokamak Plasma Analysis
Analysis of publicly available MAST (Mega Ampere Spherical Tokamak) level 2 
data from the UKAEA [public data store](https://mastapp.site/index.html).

## Projects

### 1. Radiated Power Notebook
Time plots of key parameters across single shots. Analysis of radiated power fraction 
across multiple shots. Includes instability detection using statistical thresholding, 
comparison of stable vs unstable shots, and multi-shot scatter analysis between several 
parameters.

### 2. Energy Confinement Scaling
Analysis of energy confinement time across MAST shots. Includes validation against 
the ITER-89P empirical scaling law, multi-parameter linear regression with VIF 
analysis, and Random Forest regression analysis.

## Data
Data is accessed from the MAST public S3 bucket at [store](https://mastapp.site/index.html). 

## Requirements
- zarr
- xarray
- numpy
- pandas
- matplotlib
- scipy
- sklearn
- seaborn
- statsmodels

## Usage
Run notebooks in order. Data is cached locally in `.cache/` on first run.
