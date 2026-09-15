# WIRED Grid Data Challenge

**Data-Driven Grid Reconfiguration and Optimal Power Flow under Extreme Weather**

Wildfire smoke cuts rooftop solar output. The challenge is to forecast that and reconfigure the grid around it.

## The data

- **Residential load** — 342 households, 30-minute intervals, one year
- **Rooftop PV** — 57 kW array at University of Calgary, 15-minute intervals, 2018 to present
- **Wildfire smoky days** — Environment and Climate Change Canada, hourly, May 2018 to May 2024
- **Test system** — IEEE 33-bus, 12.66 kV, 3.72 MW / 2.3 MVAR

## Start here

Everything official lives on the Grid Data Hub: **https://datahub.wiredcenter.org/**

Register with CILogon or ORCID, do the onboarding challenge, then work the modules. Final prompt drops October 5. Submissions close October 30.

Questions: pramonettivega@ucsd.edu

## This repo

`load-forecasting-demo.ipynb` is a warm-up on public PJM hourly load. Not challenge data. Run it to get comfortable with lag features, time series cross validation, and prediction intervals before the real thing.

```bash
pip install -r requirements.txt
jupyter lab load-forecasting-demo.ipynb
```
