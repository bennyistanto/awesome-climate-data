# The WBG Climate Change Knowledge Portal

The Climate Change Knowledge Portal ([CCKP](https://climateknowledgeportal.worldbank.org/)) is the hub for climate-related information, data, and tools for the World Bank Group. The Portal provides an online platform from which access and analyze comprehensive data related to climate change and development.

## Datasets

Historical ([CRU](https://crudata.uea.ac.uk/cru/data/hrg/)) and projection ([CMIP5](https://pcmdi.llnl.gov/mips/cmip5/) and [CMIP6](https://pcmdi.llnl.gov/CMIP6/)) of climate data. 
Spatial data is provided as a global NetCDF file. For complete list of the data, please check the portal.

The GOST team has downloaded some of the data and it accessible via DEC S3 bucket: `s3://wbgdecinternal-ntl/climate/data/cckp/cmip6/`

## Repo

This repo provide link for individual data that extracted and categorized from https://climatedata.worldbank.org/thredds/catalog/CRM/catalog.html

## How to use?

Make sure you have `wget` in your machine. Download the `*.sh` files, in your Terminal type and run `sh file.sh`

If you are in Windows, download `wget` from [http://gnuwin32.sourceforge.net/packages/wget.htm](http://gnuwin32.sourceforge.net/packages/wget.htm) and `git` for Windows from [https://gitforwindows.org](https://gitforwindows.org).

## Naming Convention

CCKP used excellent folder structure and naming convention to organized the data in their THREDDS server, but sometimes it's hard to guess what the data is if we only see the file name which consist of several acronyms.

The list below is expected to help understand the difficulties above.

### CMIP6 (Extremes)

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

**Example Files**

In the S3 bucket `extremes`, you will find file with name:

`returnlevel5yr-rx1day-period-mean_cmip6_period_all-regridded-bct-historical-climatology_median_1985-2014.nc`

From the filename, we can see it's: Historical Largest 1-Day Precipitation with 5 year Return Level for the period 1985-2014.

Or

`faep5yr-rx1day-period-mean_cmip6_period_all-regridded-bct-ssp119-climatology_median_2010-2039.nc`

From the filename, we can see it's: Future Projections of Largest 1-Day Precipitation with 5 year Changes in Annual Exceedance Probability and median percentile for the period 2010-2039 using SSP1-1.9 scenario.

### CMIP6 (Mean Projections)

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
| Temperature: Cold Spell Duration Index | `cdsi` |
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




