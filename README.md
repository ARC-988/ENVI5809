# Hydrodynamic Modelling of Cyclone Alfred (2025) – Capricorn Bunker

## **Hypothesis**

Cyclone Alfred (Feb–Mar 2025) generated spatially variable wave energy across the Capricorn Bunker Reefs, with the strongest hydrodynamic forcing near One Tree Island. Variations in significant wave height (Hs), peak period (Tp), and wave direction (Dp) may help explain observed geomorphic and ecological changes at OTI following the event.

---

## **Analysis Plan**

- Load and clean **wave**, **buoy**, and **cyclone** datasets using `xarray` and `pandas`.  
- Compute time series of:
  - Significant wave height (**Hs**)
  - Peak wave period (**Tp**)
  - Dominant wave direction (**Dp**)
  - Group velocity and wave energy flux (**Cge**, **P**)  
- Map spatial exposure patterns and cyclone proximity for northern, central, and southern reef sectors.  
- Perform statistical analyses:
  - S–T regression (temporal wave growth/decay)
  - Multivariate regression (**Hs ~ wind + distance + pressure**)
  - Circular statistics for directional changes
  - Cross-correlation of wind vs Hs lead–lag relationships  
- Visualise outcomes with `matplotlib`, `cartopy`, and interactive dashboards (`holoviews`/`panel`).  

---

## **Data Resources**

- **CSIRO Hindcast Dataset** — Modelled wave conditions for the Capricorn Bunker region (NetCDF)  
- **NSW Government Wave Buoy (OTI)** — Observed nearshore wave parameters at One Tree Island (CSV)  
- **BOM IBTrACS Cyclone Alfred Track** — Cyclone path, wind, and pressure data (NetCDF)  
- **ERA5 (CDAIP)** — Local wind speed and sea-level pressure reanalysis data (NetCDF)

---

## **Tools and Environment**

Python 3.11 with:
- `xarray`, `pandas`, `numpy`, `matplotlib`, `cartopy`
- `statsmodels`, `pingouin`, `scikit-learn`
- Jupyter Notebook / VS Code

---

## **Outputs**

- Time series plots of **Hs**, **Tp**, **Dp**, and **energy flux**
- Maps of **cyclone proximity** and **maximum Hs** across reef sectors
- Regression diagnostics and statistical tables
- Visual summaries of **wind–wave relationships** and **lead–lag effects**
