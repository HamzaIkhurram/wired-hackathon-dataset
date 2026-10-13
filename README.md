# WIRED Grid Data Challenge

**Data-Driven Grid Reconfiguration and Optimal Power Flow under Extreme Weather**

Wildfire smoke cuts rooftop solar output. The challenge is to forecast that and reconfigure the grid around it.

## Module 1: Forecasting

It's in this repo: **`load-forecasting-demo.ipynb`**. Clone it and run it.

```bash
pip install -r requirements.txt
jupyter lab load-forecasting-demo.ipynb
```

Hourly electricity demand for the PJM region, April 1998 to January 2002. About 32,900 readings of one number: system load in megawatts, ranging from 17,461 to 54,030. Strong daily, weekly and seasonal cycles. No duplicates, and the only 8 gaps are daylight saving clock changes.

The notebook cleans the series, builds lag and calendar features, then benchmarks LightGBM, Lasso, Ridge, random forest and others on 24-hour-ahead forecasts with prediction intervals. Expect roughly 4 to 5 percent MAPE over a full year.

There are no weather columns. Adding them is your first move.

## Module 2: Optimization

**`ieee33-opf.ipynb`** solves an optimal power flow on the IEEE 33-bus distribution feeder, the network used for the rest of the challenge.

```bash
pip install -r requirements.txt
jupyter lab ieee33-opf.ipynb
```

It uses the branch flow (DistFlow) model in Pyomo and minimizes total line losses over 24 hourly steps, using the standard benchmark line and load data. There is no PV or storage yet. You also need the IPOPT solver; the notebook installs it for you if it's missing.

If it runs correctly you should see about 202.7 kW of losses and a minimum voltage of about 0.913 p.u. at bus 17. Every cell has a short explanation above it, so read along as you run it.

Once it works, try changing the load, the substation voltage or the objective. Those are the pieces you will change in the final challenge.

## Then go here

The official challenge runs on the Grid Data Hub: **https://datahub.wiredcenter.org/**

Register with CILogon or ORCID, do the onboarding challenge, then work the modules. Final prompt October 5. Submissions close October 30.

Questions: pramonettivega@ucsd.edu
