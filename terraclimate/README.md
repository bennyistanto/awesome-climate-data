# TerraClimate

[TerraClimate](http://www.climatologylab.org/terraclimate.html) is a dataset of monthly climate and climatic water balance for global terrestrial surfaces from 1958-2020. These data provide important inputs for ecological and hydrological studies at global scales that require high spatial resolution and time-varying data. All data have monthly temporal resolution and a 4-km (1/24th degree) spatial resolution. 

## Datasets

**Primary Climate Variables:** Maximum temperature, minimum temperature, vapor pressure, precipitation accumulation, downward surface shortwave radiation, wind-speed

**Derived variables:** Reference evapotranspiration (ASCE Penman-Montieth), Runoff, Actual Evapotranspiration, Climate Water Deficit, Soil Moisture, Snow Water Equivalent, Palmer Drought Severity Index, Vapor pressure deficit

aet (Actual Evapotranspiration, monthly total), units = mm<br>
def (Climate Water Deficit, monthly total), units = mm<br>
pet (Potential evapotranspiration, monthly total), units = mm<br>
ppt (Precipitation, monthly total), units = mm<br>
q (Runoff, monthly total), units = mm<br>
soil (Soil Moisture, total column - at end of month), units = mm<br>
srad (Downward surface shortwave radiation), units = W/m2<br>
swe (Snow water equivalent - at end of month), units = mm<br>
tmax (Max Temperature, average for month), units = C<br>
tmin (Min Temperature, average for month), units = C<br>
vap (Vapor pressure, average for month), units  = kPa<br>
ws (Wind speed, average for month), units = m/s<br>
vpd (Vapor Pressure Deficit, average for month), units = kpa<br>
PDSI (Palmer Drought Severity Index, at end of month), units = unitless<br>

## Repo

This repo provide links for individual data that extracted and categorized from http://thredds.northwestknowledge.net:8080/thredds/catalog/TERRACLIMATE_ALL/catalog.html

## How to use?

Make sure you already have `wget` in your machine. Download the `*.txt` files, in your Terminal type and run `wget -c -i data_precipitation.txt`

If you are in Windows, download `wget` from [http://gnuwin32.sourceforge.net/packages/wget.htm](http://gnuwin32.sourceforge.net/packages/wget.htm) and `git` for Windows from [https://gitforwindows.org](https://gitforwindows.org).
