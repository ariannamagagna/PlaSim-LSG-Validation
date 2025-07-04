# PlaSim-LSG Validation

This repository contains the code and tools used to **validate the PlaSim-LSG coupled climate model** against **ERA5 reanalysis data**. The analysis focuses on climatological comparisons of key selected variables, including sea-level pressure, sea surface temperature, and sea ice cover.

<p align="center">
  <img src="https://github.com/user-attachments/assets/589fa99b-7cb8-4fa4-aab6-a5c4ef3d1d68" alt="Sea Ice Bias Spin" />
</p>


---

## Notebook Overview

The main notebook [`plasimlsg_validation.ipynb`](plasimlsg_validation.ipynb) performs the following:

- Loads and preprocesses model and ERA5 climatologies
- Computes bias fields (model - ERA5)
- Visualizes spatial differences using polar projections
- Calculates statistical metrics:
  - Mean Bias Error (MBE)
  - Root Mean Square Error (RMSE)
  - Mean Absolute Error (MAE)
  - Pearson correlation coefficient
- Generates histograms of bias distributions for Arctic and Antarctic regions

---


## Requirements

This project uses Python and the following libraries:

- `numpy`
- `matplotlib`
- `scipy`
- `cartopy`
- `netCDF4`
- `xarray` (optional)

Install them via:
```bash```
```pip install numpy matplotlib scipy cartopy netCDF4 xarray ```

---

## Data inputs 
 
The notebook expects preprocessed climatological fields from:

- PlaSim-LSG model output

- ERA5 reanalysis (downloadable from Copernicus)

These should be stored as NetCDF files and loaded into variables like ice_cover_climatology_model, ice_cover_climatology_era5, etc. ERA5 data can be loaded with its native grid, as the code performs interpolation with the model resolution.

---

## Outputs

For each of the variables of interest:  

- contour plots of bias fields

- histogram of bias per grid point

- printed metrics

---

## Author

**Arianna Magagna**  
BSc Physics - University of Trento  
MSc Science of Climate — University of Bologna  
📫 Contact: arianna.magagna@studio.unibo.it
