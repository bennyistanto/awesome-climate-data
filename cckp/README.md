# The WBG Climate Change Knowledge Portal

The Climate Change Knowledge Portal ([CCKP](https://climateknowledgeportal.worldbank.org/)) is the hub for climate-related information, data, and tools for the World Bank Group. The Portal provides an online platform from which access and analyze comprehensive data related to climate change and development.

## Index
* [Gridded Datasets](#gridded-datasets)
* [Repo](#repo)
* [How to use?](#how-to-use)
* [Data Dictionary](#data-dictionary)
	* [1 deg spatial resolution](#1-deg-spatial-resolution)
	* [0.25 deg spatial resolution](#025-deg-spatial-resolution)
* [References](#references)

## Gridded Datasets

CCKP provide a historical ([CRU](https://crudata.uea.ac.uk/cru/data/hrg/) and [ERA5](https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5)) and projection ([CMIP5](https://pcmdi.llnl.gov/mips/cmip5/) and [CMIP6](https://pcmdi.llnl.gov/CMIP6/)) of climate  and population ([GPW](https://sedac.ciesin.columbia.edu/data/collection/gpw-v4)) data. 

Spatial data is provided as a global NetCDF file with 1 deg spatial resolution. For complete list of the data, please check the portal.

> [!NOTE]
> 
> Since 2024, CCKP provided downscaled CMIP6 with 0.25 deg spatial resolution as global gridded NetCDF files. Accessible via this link: https://climateknowledgeportal.worldbank.org/netcdf-browser?prefix=data/
> 
> CCKP also provide aggregate information based on watershed, country and subnational information via API. Check this link https://climateknowledgeportal.worldbank.org/download-data#htab-1498 for more details.

The [GOST](https://worldbank.github.io/GOST/README.html) team has downloaded some of the data (**Multi Model Ensemble**) and it accessible via GOST S3 bucket: `s3://wbg-geography01/climate/data/cckp/`

## Repo

This repo provide link for individual data (only for **Multi Model Ensemble**) that extracted and categorized from https://climatedata.worldbank.org/thredds/catalog/CRM/catalog.html (for 1 deg data) and https://climateknowledgeportal.worldbank.org/netcdf-browser?prefix=data/ (for 0.25 deg data)

## How to use?

Make sure you have `wget` in your machine. Download the `*.txt` files, in your Terminal type and run :
```bash
wget -c -i file.txt
```
If you would like to download only single `nc` file from the `*.txt`, then you can use `wget` to by typing in your Terminal :
```
wget https://wbg-cckp.s3.amazonaws.com/data/cmip6-x0.25/fd/ensemble-all-ssp126/trend-fd-annual-mean_cmip6-x0.25_ensemble-all-ssp126_climatology_p10_1971-2020.nc
```
or by paste the link in your browser address.

If you are in Windows, download `wget` from [gnuwin32](http://gnuwin32.sourceforge.net/packages/wget.htm) or Git for Windows from [https://gitforwindows.org](https://gitforwindows.org).

## Data Dictionary

CCKP used excellent folder structure and naming convention to organized the data in their THREDDS server and NetCDF Browser, but sometimes it's hard to guess what the data is if we only see the file name which consist of several acronyms.

The list below is expected to help understand the difficulties above.

### 1 deg spatial resolution

The file with 1 deg spatial resolution, located at folder `cmip6-x1`

**CMIP6 (Extremes)**

| **Category** | **Code** |
| --- | --- |
| **Variable** |     |
| Precipitation: Largest 1-Day Precipitation | `rx1day` |
| Precipitation: Largest 5-Day Cumulative Precipitation | `rx5day` |
| Precipitation: Largest Monthly Cumulative Precipitation | `rxmonth` |
| **Time Period:** |     |
| Historical: 1985-2014 (center 2000) | `1985-2014` |
| 2010-2039 (center 2025) | `2010-2039` |
| 2035-2064 (center 2050) | `2035-2064` |
| 2060-2089 (center 2075) | `2060-2089` |
| 2070-2099 (center 2085) | `2070-2099` |
| **Calculation:** (Historical Time Period) |     |
| Return Level: 5-yr | `returnlevel5yr` |
| Return Level: 10-yr | `returnlevel10yr` |
| Return Level: 20-yr | `returnlevel20yr` |
| Return Level: 25-yr | `returnlevel25yr` |
| Return Level: 50-yr | `returnlevel50yr` |
| Return Level: 100-yr | `returnlevel100yr` |
| Return Period: 25mm | `returnperiod25mm` |
| Return Period: 50mm | `returnperiod50mm` |
| Return Period: 100mm | `returnperiod100mm` |
| Return Period: 150mm | `returnperiod150mm` |
| Return Period: 200mm | `returnperiod200mm` |
| Annual Exceedance Probability: 25mm | `aep25mm` |
| Annual Exceedance Probability: 50mm | `aep50mm` |
| Annual Exceedance Probability: 100mm | `aep100mm` |
| Annual Exceedance Probability: 150mm | `aep150mm` |
| Annual Exceedance Probability: 200mm | `aep200mm` |
| **Calculation:** (Future) |     |
| Future Return Period: 5-yr | `frp5yr` |
| Future Return Period: 10-yr | `frp10yr` |
| Future Return Period: 20-yr | `frp20yr` |
| Future Return Period: 25-yr | `frp25yr` |
| Future Return Period: 50-yr | `frp50yr` |
| Future Return Period: 100-yr | `frp100yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 5-yr | `faep5yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 10-yr | `faep10yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 20-yr | `faep20yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 25-yr | `faep25yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 50-yr | `faep50yr` |
| Changes in Annual Exceedance Probability (occurrence/year): 100-yr | `faep100yr` |
| Changes in Annual Exceedance Probability (Change Factor): 5-yr | `changefactorfaep5yr` |
| Changes in Annual Exceedance Probability (Change Factor): 10-yr | `changefactorfaep10yr` |
| Changes in Annual Exceedance Probability (Change Factor): 20-yr | `changefactorfaep20yr` |
| Changes in Annual Exceedance Probability (Change Factor): 25-yr | `changefactorfaep25yr` |
| Changes in Annual Exceedance Probability (Change Factor): 50-yr | `changefactorfaep50yr` |
| Changes in Annual Exceedance Probability (Change Factor): 100-yr | `changefactorfaep100yr` |
| **Percentile:** (Future) |     |
| Median (50th) | `median` |
| 90th | `p90` |
| 10th | `p10` |
| **Scenario:** (Future) |     |
| SSP1-1.9 | `ssp119` |
| SSP1-2.6 | `ssp126` |
| SSP2-4.5 | `ssp245` |
| SSP3-7.0 | `ssp370` |
| SSP5-8.5 | `ssp585` |
| **Model:** |     |
| Multi-Model Ensemble |     |

**CMIP6 (Mean Projections)**

| **Category** | **Code** |
| --- | --- |
| **Type** |     |
| Climatology | `climatology` |
| Timeseries (2015-2100) | `timeseries` |
| **Variable** |     |
| Essential Climate Variables: Mean-Temperature | `tas` |
| Essential Climate Variables: Min-Temperature | `tasmin` |
| Essential Climate Variables: Max-Temperature | `tasmax` |
| Essential Climate Variables: Precipitation | `pr` |
| Temperature: Cold Spell Duration Index | `csdi` |
| Temperature: Cooling Degree Days (ref-65°F) | `cdd65` |
| Temperature: Number of Frost Days (Tmin <0°C) | `fd` |
| Temperature: Days with Heat Index >35°C | `hi35` |
| Temperature: Days with Heat Index >37°C | `hi37` |
| Temperature: Days with Heat Index >39°C | `hi39` |
| Temperature: Heating Degree Days (ref-65°F) | `hdd65` |
| Temperature: Number of Hot Days (Tmax >35°C) | `hd35` |
| Temperature: Number of Hot Days (Tmax >40°C) | `hd40` |
| Temperature: Number of Hot Days (Tmax >42°C) | `hd42` |
| Temperature: Number of Hot Days (Tmax >45°C) | `hd45` |
| Temperature: Maximum of Daily Max-Temperature | `txx` |
| Temperature: Maximum of Daily Min-Temperature | `tnn` |
| Temperature: Number of Ice Days (Tmax <0°C) | `id` |
| Temperature: Number of Summer Days (Tmax >25°C) | `sd` |
| Temperature: Number of Tropical Nights (Tmin >20°C) | `tr` |
| Temperature: Number of Tropical Nigths (Tmin >26°C) | `tr26` |
| Temperature: Warm Spell Duration Index | `wsdi` |
| Precipitation: Annual SPEI Drought Index | `spei12` |
| Precipitation: Max Number of Consecutive Dry Days | `cdd` |
| Precipitation: Max Number of Consecutive Wet Days | `cwd` |
| Precipitation: Days with Precipitation >20mm | `r20mm` |
| Precipitation: Days with Precipitation >50mm | `r50mm` |
| Precipitation: Average Largest 1-Day Precipitation | `rx1day` |
| Precipitation: Average Largest 5-Day Cumulative Precipitation | `rx5day` |
| Precipitation: Average Largest Monthly Cumulative Precipitation | `rxmonth` |
| Precipitation: Precipitation Percent Change | `prpercnt` |
| Precipitation: Precipitation amount during wettest days | `r95ptot` |
| Additional Variables: Growing Season Length | `gsl` |
| Additional Variables: Relative Humidity | `hurs` |
| **Time Period:** (Climatology) |     |
| Historical Reference Period, 1995-2014 | `1995-2014` |
| 2020-2039 | `2020-2039` |
| 2040-2059 | `2040-2059` |
| 2060-2079 | `2060-2079` |
| 2080-2099 | `2080-2099` |
| **Aggregation:** (Climatology) |     |
| Annual | `annual` |
| Monthly | `monthly` |
| Seasonal | `seasonal` |
| **Aggregation:** (Timeseries) |     |
| Annual | `annual` |
| **Calculation:** (Climatology) |     |
| Mean | `mean` |
| Anomaly (from Reference Period, 1995-2014) | `anomaly` |
| **Percentile:** |     |
| Median (50th) | `median` |
| 90th | `p90` |
| 10th | `p10` |
| **Scenario:** |     |
| SSP1-1.9 | `ssp119` |
| SSP1-2.6 | `ssp126` |
| SSP2-4.5 | `ssp245` |
| SSP3-7.0 | `ssp370` |
| SSP5-8.5 | `ssp585` |
| **Model:** |     |
| Multi-Model Ensemble |     |

**Naming Convention and Example Files**

In the S3 bucket `cmip6_extremes`, you will find file with name:

`returnlevel5yr-rx1day-period-mean_cmip6_period_all-regridded-bct-historical-climatology_median_1985-2014.nc`

From the filename, we can see it's: 

Historical Largest 1-Day Precipitation, with 5 year Return Level, for the period 1985-2014.

Or

`faep5yr-rx1day-period-mean_cmip6_period_all-regridded-bct-ssp119-climatology_median_2010-2039.nc`

From the filename, we can see it's: 

Future Projections of Largest 1-Day Precipitation, with 5 year Changes in Annual Exceedance Probability, and median percentile, for the period 2010-2039, using SSP1-1.9 scenario.

### 0.25 deg spatial resolution

**Collection**

|  **Code**  |  **Label**  | 
| --- | --- |
|  `cmip6-x0.25`  |  CMIP6 0.25-degree  |
|  `cru-x0.5`  |  CRU 0.5-degree  |
|  `era5-x0.25`  |  ERA5 0.25-degree  |
|  `pop-x0.25`  |  Population and Poverty  |

**Variables**

| **Code**              | **Label**                                                    | **Unit**             | **Description**                                              |
| --------------------- | ------------------------------------------------------------ | -------------------- | ------------------------------------------------------------ |
| `cdd`                 | Maximum number of consecutive dry days                       | `days`               | The maximum length of a dry spell, computed sequentially for the entire time series, then taking the maximum value during each month in the data period (a dry day is defined as any day in which the daily accumulated precipitation `< 1 mm`) |
| `cdd65`               | Cooling Degree Days (ref-65°F)                               | `degF`               | The cumulative number of degrees that the daily average temperature over a given period is above a specified threshold (here `65°F`), which is a measurement designed to quantify the demand for energy needed to cool a building. |
| `csdi`                | Cold Spell Duration Index                                    | `days`               | The number of days each year in a sequence of at least six consecutive days during which the value of the daily minimum temperature is less than the 10th percentile of daily minimum temperature calculated for a five-day window centered on each calendar day, using all data for the given calendar day-pentad from the data period for a reference climate (e.g., present-day climate). |
| `cwd`                 | Max Number of Consecutive Wet Days                           | `days`               | This series measures the maximum length of a wet spell, computed sequentially for the entire time series, then taking the maximum value during each month in the data period (a wet day is defined as any day in which the daily accumulated precipitation `≥ 1 mm`). |
| `fd`                  | Number of Frost Days (Tmin < 0°C)                            | `days`               | The average aggregated number of days where the daily minimum temperature is `< 0°C` (= Frost Days) in the data period. A negative value indicates a reduction in the number of Frost Days. |
| `gsl`                 | Growing Season Length                                        | `days`               | Span in number of days between the days defining the Growing Season Start and Growing Season End (see below) computed across each of the two hemispheres. |
| `gslend`              | Growing Season Length End                                    | `days`               | Annual series with the day of the year (1st Jan to June 30 in Southern Hemisphere, SH, and 1st July to 31st Dec in Northern Hemisphere, NH) that reflects the first span of at least 6 consecutive days with daily mean temperature T `< 5°C`. |
| `gslstart`            | Growing Season Length Start                                  | `days`               | Annual series with the day of the year (1st Jan to June 30 in Northern Hemisphere, NH, and 1st July to 31st Dec in Southern Hemisphere, SH) that reflects the first span of at least 6 consecutive days with daily mean temperature T `> 5°C`. |
| `hd30`                | Number of Hot Days (Tmax > 30°C)                             | `days`               | The number of days with daily maximum temperature `>= 30°C` that occurred during the aggregation period. |
| `hd35`                | Number of Hot Days (Tmax > 35°C)                             | `days`               | The number of days with daily maximum temperature `>= 35°C` that occurred during the aggregation period. |
| `hd40`                | Number of Hot Days (Tmax > 40°C)                             | `days`               | The number of days with daily maximum temperature `>= 40°C` that occurred during the aggregation period. |
| `hd42`                | Number of Hot Days (Tmax > 42°C)                             | `days`               | The number of days with daily maximum temperature `>= 42°C` that occurred during the aggregation period. |
| `hd45`                | Number of Hot Days (Tmax > 45°C)                             | `days`               | The number of days with daily maximum temperature `>= 45°C` that occurred during the aggregation period. |
| `hd50`                | Number of Hot Days (Tmax > 50°C)                             | `days`               | The number of days with daily maximum temperature `>= 50°C` that occurred during the aggregation period. |
| `hdcat`               | Hot Day Heat Risk Categorization                             | `risk factor`        | Categorization of the occurrence of days above four thresholds for designated Heat Risk Variable. Hot Day Risk Categorization includes, daily maximum temperature: `30°C`, `35°C`, `40°C`, and `45°C`. If at least `0.5 day` surpassed the highest threshold, then the highest category is given, reflecting that "at minimum one day of the year experienced the highest heat level". Risk Factor Categorization: 0-4 represents Low - Extreme Risk. |
| `hdd65`               | Heating degree days (ref-65°F)                               | `degF`               | The cumulative number of degrees that the daily average temperature over a given period is below a specified threshold (here `65°F`), which is a measurement designed to quantify the demand for energy needed to warm a building. |
| `hdtr`                | Number of Hot Days and Tropical Nights                       | `risk factor`        | Categorization of the occurrence of days above eight thresholds for designated Heat Risk Variable. Hot Day and Tropical Night Risk Categorization includes daily maximum temperature: `30°C`, `35°C`, `40°C`, and `45°C` and nighttime minimum temperature: `20°C`, `23°C`, `26°C`, and `29°C`. If at least `0.5 day` surpassed the highest threshold, then the highest category is given, reflecting that "at minimum one day of the year experienced the highest heat level". Risk Factor Categorization: 0-4 represents Low - Extreme Risk. |
| `hdtrhi`              | Number of Hot Days and Tropical Nights with Humidity         | `risk factor`        | Categorization of the occurrence of days above eight thresholds for designated Heat Risk Variable. Hot Day and Tropical Night with Humidity Risk Categorization includes daily maximum temperature: `30°C`, `35°C`, `40°C`, and `45°C`; nighttime minimum temperature: `20°C`, `23°C`, `26°C`, and `29°C` and heat index: `35°C`, `37°C`, `39°C`, and `41°C`. If at least `0.5 day` surpassed the highest threshold, then the highest category is given, reflecting that “at minimum one day of the year experienced the highest heat level”. Risk Factor Categorization: 0-4 represents Low - Extreme Risk. |
| `hdtrhipopdensitycat` | Temperature and Humidity-Based Heat + Population Risk Categorization | `risk factor`        | Temperature and Humidity-Based Heat + Population Risk Categorization is calculated to account for both climate conditions and high population densities. Categorization was established relative to the highest threshold: daily maximum temperature: `30°C`, `35°C`, `40°C`, and `45°C`; nighttime minimum temperature: `20°C`, `23°C`, `26°C`, and `29°C`, and heat index: `35°C`, `37°C`, `39°C`, and `41°C`, leading to categories 0, 1, 2, 3, 4. If at least `0.5 days` surpassed the highest threshold, then the highest categorization is given. Areas with extreme heat but no population are considered less ‘risky’ for a country, than areas with only high to very high heat conditions but with high population density. |
| `hdtrpopdensitycat`   | Temperature-Based Heat + Population Risk Categorization      | `risk factor`        | Temperature-Based Heat + Population Risk Categorization is calculated to account for both climate conditions and high population densities. Categorization was established relative to the highest threshold: daily maximum temperature: `30°C`, `35°C`, `40°C`, and `45°C` and nighttime minimum temperature: `20°C`, `23°C`, `26°C`, and `29°C`, leading to categories 0, 1, 2, 3, 4. If at least 0.5 days surpassed the highest threshold, then the highest categorization is given. Areas with extreme heat but no population are considered less ‘risky’ for a country, than areas with only high to very high heat conditions but with high population density. |
| `hi35`                | Number of Days with Heat Index > 35°C                        | `days`               | The number of days where the Heat Index `>= 35°C` over the aggregation period. The Heat Index is a measure of apparent temperature that includes the influence of atmospheric moisture. High temperatures with high moisture lead to high Heat Index. |
| `hi37`                | Number of Days with Heat Index > 37°C                        | `days`               | The number of days where the Heat Index `>= 37°C` over the aggregation period. The Heat Index is a measure of apparent temperature that includes the influence of atmospheric moisture. High temperatures with high moisture lead to high Heat Index. |
| `hi39`                | Number of Days with Heat Index > 39°C                        | `days`               | The number of days where the Heat Index `>= 39°C` over the aggregation period. The Heat Index is a measure of apparent temperature that includes the influence of atmospheric moisture. High temperatures with high moisture lead to high Heat Index. |
| `hi41`                | Number of Days with Heat Index > 41°C                        | `days`               | The number of days where the Heat Index `>= 41°C` over the aggregation period. The Heat Index is a measure of apparent temperature that includes the influence of atmospheric moisture. High temperatures with high moisture lead to high Heat Index. |
| `hicat`               | Heat Index Heat Risk Categorization                          | `risk factor`        | Categorization of the occurrence of days above four thresholds for designated Heat Risk Variable. Heat Index Risk Categorization includes, heat index: `35°C`, `37°C`, `39°C`, and `41°C`. If at least `0.5 day` surpassed the highest threshold, then the highest category is given, reflecting that "at minimum one day of the year experienced the highest heat level". Risk Factor Categorization: 0-4 represents Low - Extreme Risk. |
| `hurs`                | Relative Humidity                                            | `%`                  | Based on daily mean relative humidity at `2m` as reported by climate models, or derived from specific humidity reported by climate models. |
| `id`                  | Number of Ice Days (Tmax < 0°C)                              | `days`               | This variable represents the average aggregated number of days where the daily maximum temperature is `< 0°C` in the data period. |
| `popcount`            | Population Count                                             | `population`         | Population Count                                             |
| `popdensity`          | Population Density                                           | `population_density` | Population Density                                           |
| `pov190`              | Percentage of Population below $1.90/day                     | `% of population`    | Poverty as a percent of population below a given poverty classification: `$1.90/day`, as per World Bank definitions. |
| `pov320`              | Percentage of Population below $3.20/day                     | `% of population`    | Poverty as a percent of population below a given poverty classification: `$3.20/day`, as per World Bank definitions. |
| `pov550`              | Percentage of Population below $5.50/day                     | `% of population`    | Poverty as a percent of population below a given poverty classification: `$5.50/day`, as per World Bank definitions. |
| `pr`                  | Precipitation                                                | `mm`                 | Aggregated accumulated precipitation.                        |
| `prpercnt`            | Precipitation Percent Change                                 | `%`                  | Projected percent change in total precipitation; anomaly only. |
| `r20mm`               | Number of Days with Precipitation >20mm                      | `days`               | The number of heavy precipitation days during the aggregation period. A heavy precipitation day is defined as any day in which the daily accumulated precipitation is `≥ 20 mm`. |
| `r50mm`               | Number of Days with Precipitation >50mm                      | `days`               | The number of very heavy precipitation days during the aggregation period. A very heavy precipitation day for r50mm is defined as any day in which the daily accumulated precipitation is `≥ 50 mm`. |
| `r95ptot`             | Precipitation amount during wettest days                     | `mm`                 | The accumulated precipitation amount during the `5%` wettest days over the data period. |
| `rsns`              | Net Solar Radiation at the Surface                          | `W/m²`                 | Net Solar Radiation at the Surface (rsns) is the difference between downward and upward solar radiation fluxes at the Earth's surface. (Only available on `era5-x0.25`) |
| `rx1day`              | Average Largest 1-Day Precipitation                          | `mm`                 | The average highest precipitation amount in a `1-day` period during each month in the data period. |
| `rx5day`              | Average Largest 5-Day Cumulative Precipitation               | `mm`                 | The average highest precipitation amount over a consecutive `5-day` period during each month in the data period. |
| `rxmonth`             | Average Largest Monthly Cumulative Precipitation             | `mm`                 | The highest precipitation amount in a month period during each year in the data period. |
| `sd`                  | Number of Summer Days (Tmax > 25°C)                          | `days`               | The number of days where the daily maximum temperature is `>= 25°C` in the aggregation period. A positive value indicates an increase in the number of Summer Days. |
| `tas`                 | Average Mean Surface Air Temperature                         | `°C`                 | Average mean temperature over the aggregation period         |
| `tasmax`              | Average Maximum Surface Air Temperature                      | `°C`                 | Average daily maximum temperature over the aggregation period |
| `tasmin`              | Average Minimum Surface Air Temperature                      | `°C`                 | Average daily minimum temperature over the aggregation period |
| `td`                  | Number of Frost Days (Tmin<0C)                               | `°C`                 | Number of Frost Days (Tmin<0C)                               |
| `tnn`                 | Minimum of Daily Min-Temperature                             | `°C`                 | The single-day minimum value of the daily minimum temperatures over the aggregated data period. |
| `tr`                  | Number of Tropical Nights (T-min > 20°C)                     | `days`               | The number of days where the daily minimum temperature remained `>= 20°C` over the aggregation period. |
| `tr23`                | Number of Tropical Nights (T-min > 23°C)                     | `days`               | The number of days where the daily minimum temperature remained `>= 23°C` over the aggregation period. |
| `tr26`                | Number of Tropical Nights (T-min > 26°C)                     | `days`               | The number of days where the daily minimum temperature remained `>= 26°C` over the aggregation period. |
| `tr29`                | Number of Tropical Nights (T-min > 29°C)                     | `days`               | The number of days where the daily minimum temperature remained `>= 29°C` over the aggregation period. |
| `tr32`                | Number of Tropical Nights (T-min > 32°C)                     | `days`               | The number of days where the daily minimum temperature remained `>= 32°C` over the aggregation period. |
| `trcat`               | Tropical Night Heat Risk Categorization                      | `risk factor`        | Categorization of the occurrence of days above four thresholds for designated Heat Risk Variable. Tropical Night Risk Categorization includes, nighttime minimum temperature: `20°C`, `23°C`, `26°C`, and `29°C`. If at least `0.5 day` surpassed the highest threshold, then the highest category is given, reflecting that “at minimum one day of the year experienced the highest heat level”. Risk Factor Categorization: 0-4 represents Low - Extreme Risk. |
| `tx84rr`              | Excess Mortality                                             | `population`         | Excess mortality risk factor for daily maximum temperatures `> 84th` percentile of maximum temperatures in reference period. |
| ` txx`                | Maximum of Daily Max-Temperature                             | `°C`                 | The single-day maximum value of the daily maximum temperatures over the aggregated data period. |
| `wsdi`                | Warm Spell Duration Index                                    | `days`               | The number of days in a sequence of at least six consecutive days during which the value of the daily maximum temperature is greater than the `90th` percentile of daily maximum temperature calculated for a five-day window centered on each calendar day, using all data for the given calendar day-pentad from the data period for a reference climate. |

**Products**

|  **Code**  |  **Label**  |  **Unit**  |  **Description**  |
| --- | --- | --- | --- |
| `anomaly` | Anomaly | Varies (e.g., °C, mm) | A departure from the reference value. Using temperature as an example, a positive anomaly indicates that the projected temperature was warmer than the reference value, while a negative anomaly indicates that the projected temperature was cooler than the reference value. |
| `anomalysignificance` | Anomaly Significance | Dimensionless | A measure of the statistical significance of an observed anomaly, often expressed as a p-value or confidence level. |
| `climatology` | Climatology | Varies (e.g., °C, mm) | The calculation of uniform periods, typically 20, 30, 50-years, consisting of annual, seasonal, and monthly, averages of temperature, precipitation, and other climatological variables. |
| `conflictingsignal` | Conflicting Signal | Dimensionless | Indicates areas where different climate models or scenarios show disagreement in the direction or magnitude of projected changes. |
| `natvar` | Natural Variability | Varies (e.g., °C, mm) | The range of climate variability that occurs naturally in the absence of external forcing. |
| `natvarhigh` | Natural Variability-high | Varies (e.g., °C, mm) | The upper bound of the natural variability range. |
| `natvarlow` | Natural Variability-low | Varies (e.g., °C, mm) | The lower bound of the natural variability range. |
| `nochange` | No Change | Dimensionless | Indicates areas where no significant change is projected or observed. |
| `robustchange` | Robust Change | Dimensionless | Indicates areas where there is strong agreement among models or scenarios about the direction and magnitude of projected changes. |
| `timeseries` | Time Series | Varies (e.g., °C, mm) | A sequence of data points, typically annual, which occur in successive order over a designated time horizon. |
| `trend` | Trend | Varies (e.g., °C/decade, mm/year) | The detection, estimation and prediction of trends and associated statistical and physical significance are important aspects of understanding climate and changes in climate. Trend is the rate at which change occurs over a time period. The trend may be linear or non-linear. Information on trends are available to aid users in defining climate trends in relation to natural climate variability |
| `trendconfidence` | Trend Confidence | Percentage or Dimensionless | A measure of the statistical confidence in the observed or projected trend, often expressed as a confidence interval or level. |
| `trendsignificance` | Trend Significance | Dimensionless | A measure of the statistical significance of an observed trend, often expressed as a p-value or confidence level. |
| `yearofchange` | Year of Change | Year | Year of Change represents the statistically significant departure of the selected variable from the historical natural variability bounds due to the emergence of an anthropogenically forced trend. |


**Scenario**

|  **Code**  |  **Label**  |
| --- | --- |
|  `historical`  |  Historical  |
|  `ssp119`  |  SSP1-1.9  |
|  `ssp126`  |  SSP1-2.6  |
|  `ssp245`  |  SSP2-4.5  |
|  `ssp370`  |  SSP3-7.0  |
|  `ssp585`  |  SSP5-8.5  |
|  `cru-ts4.07-historical`  |  CRU version ts4.07 Historical  |
|  `era5-x0.25-historical`  |  ERA5 x0.25 Historical  |
|  `gpw-v4-rev11`  |  GPW version 4-rev11  |

**Aggregation**

|  **Code**  |  **Label**  |
| --- | --- |
|  `annual`  |  Annual  |
|  `monthly`  |  Monthly  |
|  `period`  |  Period  |
|  `seasonal`  |  Seasonal  |

**Model**

|  **Code**  |  **Label**  |
| --- | --- |
|  `ensemble-all`  |  Multi Model Ensemble  |

**Time Period**

|  **Code**  |  **Notes**  |
| --- | --- |
|  `1950-2014`  |  cmip6-x0.25 Historical  |
|  `1995-2014`  |  cmip6-x0.25 Historical  |
|  `1971-2020`  |  cmip6-x0.25 Projection  |
|  `2001-2050`  |  cmip6-x0.25 Projection  |
|  `2005-2100`  |  cmip6-x0.25 Projection  |
|  `2015-2100`  |  cmip6-x0.25 Projection  |
|  `2020-2039`  |  cmip6-x0.25 Projection  |
|  `2040-2059`  |  cmip6-x0.25 Projection  |
|  `2051-2100`  |  cmip6-x0.25 Projection  |
|  `2060-2079`  |  cmip6-x0.25 Projection  |
|  `2080-2099`  |  cmip6-x0.25 Projection  |
|  `1901-1930`  |  cru-x0.5 Historical  |
|  `1901-2020`  |  cru-x0.5 Historical  |
|  `1901-2022`  |  cru-x0.5 Historical  |
|  `1931-1960`  |  cru-x0.5 Historical  |
|  `1961-1990`  |  cru-x0.5 Historical  |
|  `1985-2014`  |  cru-x0.5 Historical  |
|  `1986-2005`  |  cru-x0.5 Historical  |
|  `1991-2020`  |  cru-x0.5 Historical  |
|  `1995-2014`  |  cru-x0.5 Historical  |
|  `1950-2022`  |  era5-x0.25 Historical  |
|  `1951-2020`  |  era5-x0.25 Historical  |
|  `1971-2020`  |  era5-x0.25 Historical  |
|  `1985-2014`  |  era5-x0.25 Historical  |
|  `1986-2005`  |  era5-x0.25 Historical  |
|  `1991-2020`  |  era5-x0.25 Historical  |
|  `1995-2014`  |  era5-x0.25 Historical  |
|  `1995-2014`  |  pop-x0.25 Historical  |
|  `2000-2000`  |  pop-x0.25 Historical  |
|  `2010-2100`  |  pop-x0.25 Projection  |
|  `2020-2039`  |  pop-x0.25 Projection  |
|  `2040-2059`  |  pop-x0.25 Projection  |
|  `2060-2079`  |  pop-x0.25 Projection  |
|  `2080-2099`  |  pop-x0.25 Projection  |

**Percentile**

|  **Code**  |  **Label**  |
| --- | --- |
|  `mean`  |  Mean  |
|  `median`  |  Median or 50th Percentile of the Multi-Model Ensemble  |
|  `p10`  |  10th Percentile of the Multi-Model Ensemble  |
|  `p90`  |  90th Percentile of the Multi-Model Ensemble  |

**Type**

|  **Code**  |  **Label**  |  **Notes**  |
| --- | --- | --- |
|  `climatology`  |  Mean  |  |
|  `heatplot`  |  Heat plot  | Only applied to Collection = `cru-x0.5` |
|  `timeseries`  |  Timeseries  |  |
|  `timeseries-smooth`  |  Timeseries Smooth  |  |

**Statistics**

|  **Code**  |  **Label**  |  **Notes**  |
| --- | --- | --- |
|  `mean`  |  Mean  |  |
|  `max`  |  Maximum  | Only applied to Variables = `rxmonth`  |

**Naming Convention and Example Files**

In the S3 bucket {`Collection`}/{`Variables`}: `cmip6-x0.25/cdd`, you will find file with name:

`climatology-cdd-annual-mean_cmip6-x0.25_ensemble-all-historical_climatology_median_1995-2014.nc`

From the filename, we can see the structure: 

<font color='#A8D08D'>product</font>-<font color='#ED7D31'>variable</font>-<font color='#B4C6E7'>aggregationperiod</font>-<font color='#4472C4'>statistic</font>\_<font color='#FF0000'>collection</font>\_<font color='#FFC000'>model-scenario</font>\_<font color='#538135'>type</font>\_<font color='#404040'>percentile</font>\_<font color='#AEAAAA'>timeperiod</font>.nc

and the explanation:

Historical Climatology of Consecutive Dry Days (CDD), calculated as the annual mean, using the median of all ensemble members from CMIP6 models at 0.25-degree resolution, for the period 1995-2014.

Or in {`Collection`}/{`Variables`}: `cmip6-x0.25/wsdi`, you will find file with name:

`conflictingsignal-wsdi-annual-mean_cmip6-x0.25_ensemble-all-ssp585_climatology_median_2080-2099.nc`

From the filename, we can see it's:

Conflicting Signal analysis for the Warm Spell Duration Index (WSDI), calculated as the annual mean, using the median of all ensemble members from CMIP6 models at 0.25-degree resolution, for the SSP5-8.5 scenario, representing the climatology for the period 2080-2099.

## References

1. https://climateknowledgeportal.worldbank.org/download-data#htab-1499
2. https://worldbank.github.io/climateknowledgeportal/README.html