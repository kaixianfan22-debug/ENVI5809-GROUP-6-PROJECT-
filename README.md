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
