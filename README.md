# Modelling Time-Series Data

This repository contains the time-series data used in a study by [Ullmark et al. (2023)](https://dx.doi.org/10.2139/ssrn.4681508) with a focus on Northern Europe. The dataset is built upon ERA5 reanalysis data and utilizes the [GlobalEnergyGIS](https://github.com/niclasmattsson/GlobalEnergyGIS) repository for its generation. To convert from .mat files to .inc files, scripts available in [another repository](https://github.com/jonull93/PhD) have been used.

This image illustrates the geographical coverage of the region (nordic_L) focused on in this study.

<picture>
  <img alt="Geographical Scope of the Study" src="Ullmark 2023 (nordic_L)/nordic_L.png" width="400">
</picture>


## Repository Structure

The main folder of interest is "Ullmark 2023 (nordic_L)". Within this folder, you'll find:

### Folders:

* **electricity demand**: Contains `.inc` files with hourly data for each profile year representing electricity demand.
* **heating demand**: Contains `.inc` files with hourly data for each profile year representing heating demand.
* **variable renewables**: Contains `.inc` files with hourly data for each profile year representing the normalized electricity output of wind or solar generating capacity at various sites.
* **GlobalEnergyGIS case files**: Contains project-specific files necessary to recreate the profiles.

The `.inc` files contain hourly data and are text-readable. The profile years may correspond to calendar years or could span from `h4344` of one year to `h4343` of the next, labeled `1980-1981` for example.

### Files:

* **commands to generate electricity demand.txt**: Julia commands used to generate electricity demand profiles.
* **commands to generate heat demand.txt**: Julia commands used to generate heating demand profiles.
* **commands to generate solar PV profiles.txt**: Julia commands used to generate solar PV profiles.
* **commands to generate wind profiles.txt**: Julia commands used to generate wind profiles.


## Background

The VRE and demand profiles here are rooted in ERA5 reanalysis data and were generated using scripts available in the [GlobalEnergyGIS repository](https://github.com/niclasmattsson/GlobalEnergyGIS) developed for a study by Mattsson et al. The methodology employed harnesses machine learning to enable the generation of demand profiles for times and areas where concrete electricity demand data is lacking but temperature, wind, and solar irradiation data are accessible.

For the present work:

* Electricity demand training was done on demand profiles for 44 regions during the year 2015.
* Heating demand training was based on profiles from 28 regions spanning the years 2008-2015.


## Usage & Instructions

Before attempting to execute the provided Julia commands to recreate profiles, users are strongly advised to:

1.  Visit the [GlobalEnergyGIS repository](https://github.com/niclasmattsson/GlobalEnergyGIS).
2.  Follow the setup and usage instructions there.

## Credits

A special thank you to the [GlobalEnergyGIS project](https://github.com/niclasmattsson/GlobalEnergyGIS) by Niclas Mattsson for making this work possible. Please ensure you reference the project appropriately if you utilize or adapt the data and scripts from this repository.
