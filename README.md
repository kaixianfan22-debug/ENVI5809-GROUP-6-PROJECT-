# Spatio-Temporal Dynamics and Environmental Drivers of *Zostera capricorni* in the Great Barrier Reef (2010–2018)

## Overview
This repository contains all Jupyter notebooks, processed datasets, and figures for the **ENVI5809 Final Project**.  
The project investigates how *Zostera capricorni* (ZC) occupancy varies across eight Great Barrier Reef (GBR) sites from 2010–2018 and identifies key environmental and biotic drivers.  
Environmental variables are sourced from the **eReefs model**, while *Halophila ovalis* (HO) is included as a **biotic covariate** to test whether its presence influences ZC occupancy.  
Forecasting focuses only on *Zostera capricorni* dynamics (2019–2023).

---

## Scientific Questions / Hypotheses

1. **Spatio-temporal dynamics:**  
   How does monthly occupancy of *Zostera capricorni* vary across eight GBR sites and seasons (2010–2018)?

2. **Environmental drivers:**  
   Which eReefs variables (temperature, salinity, sea-level anomaly η, current speed, wind), including 1-month lags, are associated with ZC occupancy?

3. **Biotic interaction:**  
   Does *Halophila ovalis* occupancy correlate with *Zostera capricorni* presence, indicating facilitation or competition?

4. **Forecasting:**  
   Can models trained on 2010–2018 ZC data forecast occupancy for 2019–2023 and outperform persistence and seasonal-naïve baselines?

### Additional Exploratory Test  
Beyond the core questions, a **sediment-type analysis** was conducted to examine whether substrate composition (sand, mud, mixed) might influence ZC occupancy patterns across sites.  
This sediment comparison is treated as a supporting test to complement the main environmental and biotic analyses.


### Why only three sites for prediction (Gladstone, Cairns, Townsville)
We restricted forecasting to these three sites for data and methodological integrity:

- **Continuous coverage 2010–2018:** Minimal gaps after monthly resampling; enough history for seasonal models.
- **Driver availability:** `salt_lag1`, `eta`, and `current_speed_lag1` present with low missingness and stable ranges.
- **Representative gradient:** The trio spans different GBR regions and environmental regimes, improving generality.
- **Model diagnostics:** Reasonable residual autocorrelation and variance; other sites failed basic checks (heavy gaps, structural breaks, or zero-variance drivers).
- **Scope control:** Limits compute and figure count to course requirements while preserving scientific value.

Sites not modeled for prediction remain in the spatio-temporal analyses but were excluded from forecasting due to one or more of the issues above.
---

## Datasets

| Dataset | Description | Source |
|----------|--------------|--------|
| **JCU TropWATER Seagrass Site Surveys (1984–2018)** | Species presence/absence, site, month, effort | JCU TropWATER |
| **eReefs Environmental Drivers** | Temperature, salinity, sea-level anomaly (η), currents, wind | CSIRO & AIMS eReefs THREDDS |


**Core input files:**
- `GBR_NESP-TWQ-3.2.1-5.4_JCU_Seagrass_1984-2018_Site-surveys.csv`-----**JCU TropWATER Seagrass Site Surveys (1984–2018)**
- `2509.28d55d4-collected.csv`-----**eReefs Environmental Drivers**
- `seagrass location.csv`-----**8 sites location**

  ## Repository Structure
01_dataloading.ipynb # Build monthly occupancy (ZC & HO), merge with eReefs, export CSVs
02_ZC_spatiotemporal.ipynb # ZC spatial-temporal analysis (heatmaps, seasonal cycles, time series) and Correlation and environmental driver inspection
03_HO_biotic_analysis.ipynb # HO occupancy visualization (biotic covariate)
04_sediment_effects.ipynb # Sediment-type GLM test (supporting analysis)
05Gladstone_pred.ipynb # PCA + SARIMAX forecast for Gladstone
06Cairns_pred.ipynb # PCA + SARIMAX forecast for Cairns
07Townsville_pred.ipynb # PCA + SARIMAX forecast for Townsville



