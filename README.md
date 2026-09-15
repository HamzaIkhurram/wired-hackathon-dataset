# WIRED Grid Data Challenge

**Data-Driven Grid Reconfiguration and Optimal Power Flow under Extreme Weather**

Wildfire smoke cuts rooftop solar output. The challenge is to forecast that and reconfigure the grid around it.

## The data

It's in this repo: **`load-forecasting-demo.ipynb`**. Clone it and run it.

```bash
pip install -r requirements.txt
jupyter lab load-forecasting-demo.ipynb
```

Hourly electricity demand for the PJM region, April 1998 to January 2002. About 32,900 readings of one number: system load in megawatts, ranging from 17,461 to 54,030. Strong daily, weekly and seasonal cycles. No duplicates, and the only 8 gaps are daylight saving clock changes.

The notebook cleans the series, builds lag and calendar features, then benchmarks LightGBM, Lasso, Ridge, random forest and others on 24-hour-ahead forecasts with prediction intervals. Expect roughly 4 to 5 percent MAPE over a full year.

There are no weather columns. Adding them is your first move.

## Then go here

The official challenge runs on the Grid Data Hub: **https://datahub.wiredcenter.org/**

Register with CILogon or ORCID, do the onboarding challenge, then work the modules. Final prompt October 5. Submissions close October 30.

Questions: pramonettivega@ucsd.edu
