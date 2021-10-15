# TerraClimate

[TerraClimate](http://www.climatologylab.org/terraclimate.html) is a dataset of monthly climate and climatic water balance for global terrestrial surfaces from 1958-2020. These data provide important inputs for ecological and hydrological studies at global scales that require high spatial resolution and time-varying data. All data have monthly temporal resolution and a 4-km (1/24th degree) spatial resolution. 

## Datasets

**Primary Climate Variables:** Maximum temperature, minimum temperature, vapor pressure, precipitation accumulation, downward surface shortwave radiation, wind-speed

**Derived variables:** Reference evapotranspiration (ASCE Penman-Montieth), Runoff, Actual Evapotranspiration, Climate Water Deficit, Soil Moisture, Snow Water Equivalent, Palmer Drought Severity Index, Vapor pressure deficit

aet (Actual Evapotranspiration, monthly total), units = mm
def (Climate Water Deficit, monthly total), units = mm
pet (Potential evapotranspiration, monthly total), units = mm
ppt (Precipitation, monthly total), units = mm
q (Runoff, monthly total), units = mm
soil (Soil Moisture, total column - at end of month), units = mm
srad (Downward surface shortwave radiation), units = W/m2
swe (Snow water equivalent - at end of month), units = mm
tmax (Max Temperature, average for month), units = C
tmin (Min Temperature, average for month), units = C
vap (Vapor pressure, average for month), units  = kPa
ws (Wind speed, average for month), units = m/s
vpd (Vapor Pressure Deficit, average for month), units = kpa
PDSI (Palmer Drought Severity Index, at end of month), units = unitless

## Repo

This repo provide links for individual data that extracted and categorized from http://thredds.northwestknowledge.net:8080/thredds/catalog/TERRACLIMATE_ALL/catalog.html

## How to use?

Make sure you already have `wget` in your machine. Download the `*.sh` files, in your Terminal type and run `sh data_precipitation.sh`

If you are in Windows, download `wget` from [http://gnuwin32.sourceforge.net/packages/wget.htm](http://gnuwin32.sourceforge.net/packages/wget.htm) and `git` for Windows from [https://gitforwindows.org](https://gitforwindows.org).
