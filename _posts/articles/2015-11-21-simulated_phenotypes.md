---
layout: post
title: "A Simulated Data Set"
modified: 2015-11-21T22:22:27-05:00
categories: articles
excerpt: "Draft of high frequency trait and yield data"
tags: [traits, yields, data]
image:
  feature: sorghum_simulation_20151121.png
  credit: "David LeBauer. Simulated growth of Sorghum genotypes; green is most productive and red line is least."
  creditlink: "https://github.com/terraref/terraref.github.io/blob/6cfb88a3b0e1d73dc539af5ae020baac2ac2bc9d/_drafts/simulated_sorghum_code.Rmd"

date: 2015-11-21T22:22:27-05:00
---

* Table of Contents
{:toc}

# A simulated dataset

We need feedback on data products that you will need access to.  To obtain feedback prior to the pipeline being in place, we have simulated data that a sensor might observe, along with data sets containing some of the underlying environmental drivers and physiological traits.

Note that these data sets contain numerical artifacts, quasi-principled error terms, and liberal re-application of core concepts for the purposes of developing these datasets. 

All of these simulated datasets are released with an unrestrive [copyright](https://creativecommons.org/publicdomain/zero/1.0/).  This means you can copy, modify, ans share the data.  Please keep in mind that the data sets are not production quality - they have been developed solely to receive feedback.

### A note on variable names

I have used the variable names currently used in BETYdb.org/variables, along with names inspired by the more standardized naming Climate Forecasting conventions. However, this is a very early pre-release, and we welcome comments on how such data should be formatted and accessed can be discussed in [issue #18](https://github.com/terraref/reference-data/issues/18).

# Design of Simulation Experiment


Sorghum lines grown at each of three sites along a N-S transect in Illinois over five years (2021-2025). 

## Time Span (2021-2025) 

These are historic data, but the years have been changed to emphasize the point that these are not real data. The years have been chosen to select climate extremes. Two years were dry, two were wet, and one was average.

| year | drought index |
|-----|-----|
| 2021 | wet |
| 2022 | dry |
| 2023 | normal |
| 2024 | wet |
| 2025 | dry |


### Sites

These are approximate locations used to query the meteorological and soil data used in the simulations. 
 
| site name | latitude | longitude | 
|-------|------|------|
| north | 42.0 | -88.5 |
| central | 40.0 | -88.5 |
| south | 37.0 | -88.5 |

Each site has four replicate fields: A, B, C, D. This simulated dataset assumes each field within a site has similar, but different meteorology (e.g., as if they were all in the same county). 

## Meteorology

| variable_id|name                           |standard_name       |units                          |description                                                                                                                                                                                                      |
|-----------:|:------------------------------|:---------------|:------------------------------|:----------------|
|            | Tmin                               | | C  |Daily max temperature |
|            | Tmax                               |  | C  |Daily min temperature |
|            | Tavg                               |  | C  |Daily mean temperature |
|            | precipitation                    | precipitation_flux | mm/d                        |Daily precipitation |


## Genotypes

Two-hundred and twenty-seven lines were grown at each site. Each line is identified by a unique integer in the range [9915:10141]

## Phenotypes

The phenotypes associated with each genotype is in the file `phenotypes.csv`. 

These 'phenotypes' are used as input parameters to the simulation model. We often refer to these as 'traits' (as opposed to biomass or growth rates, which are states and proceses). In this example, we assume that 'phenotypes' are time-invariant.


| variable_id|name                           |standard_name                                                 |units                          |Description                                                                                                                                                                                                      |
|-----------:|:------------------------------|:-------------------------------------------------------------|:------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          |genotype                 |                            |               |genetically and phenotypically distinct line |         
|          |Vmax                 |                            | umol m-2 s-1              | maximum carboxylation of Rubisco according to the Collatz model  |      
|          38|cuticular_cond                 |conductance_of_fully_closed_stomata                           |umol H2O m-2 s-1               |leaf conductance when stomata fully closed                                                                                                                                                                       |
|          15|SLA                            |specific_leaf_area                                            |m2 kg-1    |Specific Leaf Area|
|          39|quantum_efficiency             |mole_ratio_of_carbon_dioxide_to_irradiance_in_leaf  |fraction   |see Farqhuar model |
|          18|LAI                            |leaf_area_index          |m2 leaf m-2 ground |Leaf Area Index |
|          31|c2n_leaf |mass_ratio_of_carbon_to_nitrogen_in_leaf   |ratio  |C:N ratio in leaves|
|         493|growth_respiration_coefficient |respiration_coefficient_for_growth  |mol CO2 / mol net assimilation |amount of CO2 released due to growth per unit net photosynthesis  |
|           7|leaf_respiration_rate_m2       |respiration_rate_per_unit_area_in_leaf                        |umol CO2 m-2 s-1               |Not really ""dark respiration"" Often this is respiration that occurs in the light. Date and time fields ""should"" identify pre-dawn (nightime/dark) leaf resp vs the Rd that comes from a A-Ci or A-PPFD curve |
|           4|Vcmax                          |rubisco_carboxylation_rate_in_leaf_assuming_saturated_rubp    |umol CO2 m-2 s-1               |maximum rubisco carboxylation capacity  |
|         404|stomatal_slope.BB              |stomatal_slope_parameter_assuming_ball_berry_model            |ratio      |slope parameter for Ball-Berry Model of stomatal conductance |
|           5|Jmax   |electron_transport_flux_in_thylakoid_assuming_saturated_light |umol photons m-2 s-1   |maximum rate of electron transport  |
|         492|extinction_coefficient_diffuse |extinction_coefficient_for_diffuse_light_in_canopy            |                               |canopy extinction coefficient for diffuse light                                                                                                                                                                  |

## Simulated Sensor Data

This dataset includes what a sensor might observe, daily for five years during the growing season.

| variable_id|name                           |standard_name       |units                          |Description                                                                                                                                                                                                      |
|-----------:|:------------------------------|:---------------|:------------------------------|:----------------|
|            | sitename                     |                                                              |                        |  Name of site |
|            | plotid                               |                                                              |                        | experimental replicate plot |
|            |year                             |                                                              |                        | |
|            | date                           | | YYYY-MM-DD         | |
|            |  Stem                             |  stem_biomass_content  |                        | Mg / ha |
|            |  Leaf                             |  leaf_biomass_content  |                        | Mg / ha |
|            |  Root                             |  root_biomass_content  |                        | Mg / ha |
|            |  Rhizome                             |  rhizome_biomass_content  |                        | Mg / ha |
|          18|LAI                            |leaf_area_index   |ratio             |  Leaf Area Index is the ratio of leaf area to ground area |
|          |NDVI                            |normalized_difference_vegetation_index                                               |ratio             | commonly used vegetation index |
|            | Height                               |   canopy_height | m                        | |

# How to obtain data and give feedback:

Please provide feedback. Please provide feedback by leaving a comment below, commenting on the issue in our [GitHub repository](https://github.com/terraref/reference-data/issues/20), emailing me, [dlebauer@illinois.edu](mailto:dlebauer@illinois.edu), or visiting the [TerraRef Reference Data chatroom](https://gitter.im/terraref/reference-data).

* If you do something cool, please send comments and figures! 
* I also can provide similar data at hourly or higher frequency as well as other processes and environmental drivers, 
Data are located on Box: https://uofi.box.com/sorghum-simulation

## Data on BETYdb

These data have been uploaded to a [test instance of our database, BETYdb.](http://pecandev.igb.illinois.edu/terra-test/search?search=sorghum) and can be accessed in the following ways:

1. web interface: search + download terraref.ncsa.illinois.edu/betydb-test
2. via BETYdb API: 
  * json: http://terraref.ncsa.illinois.edu/betydb-test/search.json?genus=sorghum
  * csv: http://terraref.ncsa.illinois.edu/betydb-test/search.csv?genus=sorghum
  * To query additional metadata, see API Documentation: <--!please link here after it has been deployed-->

## csv files: [Data on Box](https://uofi.box.com/s/ups2b5hja4ul8bwi1c4jwiq19vdpwp7o)

* observations.csv: simulated observations including biomass, LAI, NDVI, height, (aka 'phenotypes')
* phenotypes.csv: physiological traits such as photosynthetic parameters, SLA, leaf angle, etc. associated w/ genotype (assumed time invariant)
* met.csv: daily temperature and precipitation summaries

 <iframe  src="https://app.box.com/embed_widget/s/ups2b5hja4ul8bwi1c4jwiq19vdpwp7o?view=list&sort=name&direction=ASC&theme=blue" width="500" height="400" frameborder="0" allowfullscreen webkitallowfullscreen msallowfullscreen></iframe>

