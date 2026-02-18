# Backcasted End-of-Month and Monthly Average Crude Oil Prices (1973–Present)

[![DOI](https://zenodo.org/badge/DOI/placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

Standard macroeconomic databases typically only report monthly average crude oil prices. This repository provides a comprehensive dataset of both **monthly average** and **end-of-month spot prices** for WTI and Brent crude oil, backcasted to January 1973.

This dataset (`MasterFile_CDataM.xlsx`) is specifically designed for empirical macroeconomics, time-series analysis, and high-frequency forecasting. It resolves common data limitations by extending end-of-month closing prices into the historical sample. The end-of-month data allows researchers to test against the random walk hypothesis in forecasting and reduces shock mistiming in structural analysis.

**Update Schedule:** The dataset is constructed using the real-time data available on the last day of the preceding month at 11:59 pm EST. This data package is updated on the first Wednesday of every month. 
*(Note: Real-time data for the global crude oil market, including complete vintages of the Refiner's Acquisition Cost, are provided in a [separate repository](https://github.com/SSEconomics/real-time-crude-oil-data)).*

## How to Cite

When using this data in your research or analysis, please cite the appropriate sources.

**For the primary dataset, please cite:**
> Ellwanger, R. and S. Snudden, (2023a). Forecasts of the Real Price of Oil Revisited: Do they Beat the Random Walk? *Journal of Banking and Finance*, 154(106962): 1-8.

**For the backcasted (Pre-1986) data, please cite:**
> Ellwanger, R. and Snudden, S. (2023b). Futures Prices are Useful Predictors of the Spot Price of Crude Oil. *The Energy Journal*, 44(4): 45-62.

**If utilizing the imputed 1973 Nominal RAC data, please also cite:**
> Mork, K. A. (1989). Oil and the macroeconomy when prices go up and down: an extension of Hamilton's results. *Journal of Political Economy*, 97(3), 740-744.

<details>
<summary><b>Click to copy BibTeX entries</b></summary>

```bibtex
@article{ellwanger2023rw,
  title={Forecasts of the Real Price of Oil Revisited: Do they Beat the Random Walk?},
  author={Ellwanger, R. and Snudden, S.},
  journal={Journal of Banking and Finance},
  volume={154},
  pages={106962},
  year={2023}
}

@article{ellwanger2023futures,
  title={Futures Prices are Useful Predictors of the Spot Price of Crude Oil},
  author={Ellwanger, R. and Snudden, S.},
  journal={The Energy Journal},
  volume={44},
  number={4},
  pages={45--62},
  year={2023}
}

@article{mork1989oil,
  title={Oil and the macroeconomy when prices go up and down: an extension of Hamilton's results},
  author={Mork, K. A.},
  journal={Journal of Political Economy},
  volume={97},
  number={3},
  pages={740--744},
  year={1989}
}

```

</details>

## Data Dictionary

The core file is `MasterFile_CDataM.xlsx`.

| Variable | Description | Start Date | Source / Notes |
| --- | --- | --- | --- |
| `WTI` | Monthly average of daily closing spot prices for West Texas Intermediate (Dollars per Barrel). | 1973-01 | EIA. Backcasted prior to 1986M1 using front futures contract and RAC. |
| `Brent` | Monthly average of daily closing spot prices for Brent (Dollars per Barrel). | 1973-01 | EIA. Backcasted prior to 1987M5 using front futures contract and RAC. |
| `WTI_lastday` | Closing price on the last trading day of the month for WTI. | 1973-01 | EIA. Backcasted prior to 1986M1. |
| `Brent_lastday` | Closing price on the last trading day of the month for Brent. | 1973-01 | EIA. Backcasted prior to 1987M5. |
| `RAC` | Nominal Refiner's Acquisition Cost of Crude Oil (Dollars per Barrel). | 1973-01 | EIA Monthly Energy Review (MER). Weighted monthly average. Typical delay is 2 months. 1973 data imputed following Mork (1989). |
| `CPI` | US Consumer Price Index (Monthly Seasonally Adjusted). | 1973-01 | Philadelphia Fed Real-Time Database (PCPI). Typical delay is 1 month. |

## Quick Start: Code & Examples *(Coming Soon!)*

To ensure this data is as accessible as possible, starter code will be provided in both **R** and **Stata**. These scripts are currently in development and will be uploaded shortly.

Once available, the scripts will demonstrate how to:
1. Directly load `MasterFile_CDataM.xlsx` from this repository.
2. Graph the historical series.
3. Construct the end-of-month RAC using the provided backcasted spot prices.
4. Construct one-month-ahead baseline forecasts.

### [R Users]

See `scripts/analysis_r.R` *(Coming Soon)*.

### [Stata Users]

See `scripts/analysis_stata.do` *(Coming Soon)*.

## Replication Materials

This repository is maintained as a living dataset for ongoing research and forecasting. If you are looking to perfectly replicate the results of the original papers, please use the static replication packages available on my [research page](https://stephensnudden.com/research/):

* [Replication Package: Ellwanger & Snudden (2023a) - *Forecasts of the Real Price of Oil Revisited: Do they Beat the Random Walk?*](https://www.dropbox.com/scl/fi/flxmw6a23ft00dk4g6yfi/Forecasts_M_Revisited.zip?rlkey=cebwndtl5kdcjljqdsmqw6tuf&dl=0)
* [Replication Package: Ellwanger & Snudden (2023b) - *Futures Prices are Useful Predictors of the Spot Price of Crude Oil*](https://www.dropbox.com/scl/fi/q5zfryq4ftamh7n8rwhpf/ReplicationCode.zip?rlkey=ids5orur80dtnfmfwo0orcoc1&dl=0)

