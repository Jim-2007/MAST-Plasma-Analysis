# MAST Tokamak Plasma Analysis
Analysis of publicly available MAST (Mega Ampere Spherical Tokamak) level 2 
data from the UKAEA [public data store](https://mastapp.site/index.html).

## Projects
This is my analysis of the MAST public dataset, where I explore data handling methods.
I hope to improve my understanding of data analysis as well as fusion physics
following each project. 

### 1. Radiated Power Notebook
Plots profiles of key parameters across single shots. Analysis of radiated power 
across multiple shots. Includes instability detection using statistical thresholding, 
comparison of stable vs unstable shots, and multi-shot scatter analysis between several 
parameters.

### 2. Energy Confinement Scaling
Analysis of energy confinement time across MAST shots. Includes validation against 
the ITER-89P empirical scaling law, multi-parameter linear regression with VIF 
analysis, and Random Forest regression analysis.

### 3. Plasma Drop Prediction
Trains Random Forest and LightGBM classifiers to predict plasma current disruptions in MAST shots 18500-30500. Extracts rolling window features from key parameters (ip, wmhd, q95, li, vloop, beta) and labels timesteps where plasma current drops by >40% within 50ms.

## Data
Data is accessed from the MAST public S3 bucket at [store](https://mastapp.site/index.html). 
Experiment lists can be found [here](https://opendata.ukaea.uk/mast-data/).

## Requirements
- zarr
- xarray
- numpy
- pandas
- matplotlib
- scipy
- scikit-learn
- seaborn
- statsmodels
- lightgbm
- fastparquet
- fsspec
- s3fs

## Usage
Run notebooks in order. Data is cached locally in `.cache/` on first run.
