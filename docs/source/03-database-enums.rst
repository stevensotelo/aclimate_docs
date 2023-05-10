Enums 
#####


.. _Measure Yield Definition:

Measure Yield
=============

The following Enums are used in the forecast crop model processing

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Mesuare
    - Long name
  
  * - yield_14
    - yield kg/ha to 14% humidity
  * - yield_0
    - yield kg/ha to 0% humidity
  * - d_har
    - days to harvest
  * - d_dry
    - days to start grain drying
  * - prec_acu
    - Cumulative precipitation for the crop cycle
  * - t_max_acu
    - cumulative maximum temperature
  * - t_min_acu
    - cumulative minimum temperature
  * - bio_acu
    - Total aboveground biomass accumulated
  * - et_acu
    - Cumulative Evapotranspiration
  * - land_pre_day
    - Land preparation day
  * - st_ger_boo_n
    - Nitrogen stress germination to booting
  * - st_boo_ant_n
    - Nitrogen stress booting to anthesis
  * - st_beg_end_gf_n
    - nitrogen stress beginning to end of grain filling
  * - st_ger_boo_w
    - Water stress germination to booting
  * - st_boo_ant_w
    - Water stress booting to anthesis
  * - st_beg_end_gf_w
    - water stress beginning to end of grain filling
  * - st_ger_ant_n
    - nitrogen stress germination to anthesis
  * - st_ger_ant_w
    - water stress germination to anthesis
  * - hs_hb_s_e
    - Hydrological balance between sowing and emergence
  * - hs_hb_t
    - Hydrological balance during tillering
  * - hs_hb_ei_b
    - Hydrological balance between  beginning of stem elongation period and end of booting
  * - hs_hb_bh_m
    - Hydrological balance between beginning of heading and full maturity
  * - hs_hb_s_m
    - Hydrological balance between sowing and full maturity
  * - hs_ra_s
    - Rainfall amount during pre-sowing period
  * - hs_ndr10_t
    - Number of rainy days with rain above 10 mm  during tillering
  * - hs_ndr40_t
    - Number of rainy days with rain above 40 mm  during tillering
  * - hs_ndr5_h_m
    - Number of days with rain above 5 mm between heading and full maturity
  * - hs_ndr40_bh_m
    - Number of days with rain above 40 mm between heading and full maturity
  * - hs_cdr5_h_f
    - Maximum number of consecutive days with rain above 5 mm between heading and flowering
  * - hs_cdr5_f_m
    - Maximum number of consecutive days with rain above 5 mm between flowering and full maturity
  * - hs_ndt2_b_f
    - Number of days with minimum daily temperature below 2 °C between booting and flowering
  * - hs_ndt28_b_f
    - Number of hot days with maximum daily temperature above 28 °C between beginning of stem elongation period and flowering


Forecast Model
==============

This enumeration represents the mode to execute climate forecast

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Variables
    - Description
  
  * - none
    - No execute forecast
  * - cpt
    - Use CPT traditional
  * - next_gen
    - Use next gen scripts


Measure Climatic
================

This Enum represents the different climatic variables available on the platform

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Variables
    - Description
  
  * - prec
    - Precipitation
  * - t_max
    - Maximum temperature
  * - t_min
    - minimum temperature
  * - rel_hum
    - Relative humidity
  * - sol_rad
    - Solar radiation
  * - prec_ter_1
    - Lower tertile of normality of precipitation
  * - prec_ter_2
    - Upper tertile of normality of precipitation



Measure Performance
===================

This enum represents the different metrics of climate models

.. list-table:: Enums
  :widths: 25
  :header-rows: 1

  * - Variables
  
  * - goodness
  * - kendall
  * - pearson
  * - canonica
  * - afc2
  * - groc
  * - ignorance
  * - rpss
  * - spearman



ModelsPyCpt
===========

These Enums are used in PyCPT modules.

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Module
    - Type
  
  * - CanSIPSv2
    - Seasonal
  * - COLA_RSMAS_CCSM4
    - Seasonal
  * - GFDL_CM2p5_FLOR_A06
    - Seasonal
  * - GFDL_CM2p5_FLOR_B01
    - Seasonal
  * - NASA_GEOSS2S
    - Seasonal
  * - NCEP_CFSv2
    - Seasonal
  * - EU_C3S_ECMWF_SEAS5
    - Seasonal
  * - EU_C3S_MeteoFrance_System7
    - Seasonal
  * - EU_C3S_UKMO_GloSea6GC2S600
    - Seasonal
  * - EU_C3S_DWD_GCFS2p1
    - Seasonal
  * - EU_C3S_CMCC_SPS3p5
    - Seasonal
  * - ECMWF
    - Subseasonal
  * - CFSv2_SubX
    - Subseasonal


.. _Quarter:


Quarter
=======

These Enums represent the quarters of the year

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Quarter
    - Definition

  * - djf
    - December January February
  * - jfm
    - January February March
  * - fma
    - February March April
  * - mam
    - March April May
  * - amj
    - April May June
  * - mjj
    - May June July
  * - jja
    - June July August
  * - jas
    - July August September
  * - aso
    - August September October
  * - son
    - September October November
  * - ond
    - October November December
  * - ndj
    - November December January



TypePyCPT
=========

This enumeration represents the type of configuration for PyCPT.

.. list-table:: Enum Definition
  :widths: 25
  :header-rows: 1

  * - Type

  * - seasonal
  * - subseasonal



ScenarioName
============

This enum represents the extreme scenarios of the application.

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Type
    - Definition

  * - max
    - maximum extreme scenario
  * - min
    - minimum extreme scenario
  * - avg
    - average scenario



LogEntity
=========

This enumeration represents the entities that are affected in the system

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Variables
    - Description
  
  * - lc_country
    - Countries' collection
  * - lc_state
    - States' collection
  * - lc_municipality
    - Municipalities' collection
  * - lc_weather_station
    - Weather stations' collection
  * - cp_setup
    - Setup collection
  * - cp_crop
    - Crops' collection
  * - cp_soil
    - Soils' collection
  * - cp_cultivar
    - Cultivars' collection
  * - cp_recommendation
    - Recommendation collection
  * - log_administrative
    - Administrative log collection
  * - log_service
    - Service log collection
  * - hs_climatology
    - Collection of climatology
  * - hs_historical_climatic
    - Climate History collection
  * - hs_historical_yield
    - Yield history collection
  * - fs_forecast
    - Forecast's collection
  * - fs_forecast_scenario
    - Forecast scenario collection
  * - fs_forecast_yield
    - Yield forecast collection
  * - fs_forecast_climate
    - Climate forecast collection
  * - fs_forecast_phen_phase
    - Phenological phase forecast collection
  * - users
    - Users collection
  * - roles
    - Roles collection
  * - ad_source
    - Source collection
  * - ad_user_permission
    - User permission collection




LogEvent
========

This enums represents the events that can be performed on the application.

.. list-table:: Enum Definition
  :widths: 25 25
  :header-rows: 1

  * - Event
    - Definition
  
  * - cre
    - Event to create a record
  * - rea
    - Event to search records
  * - upd
    - Event to update records
  * - del
    - Event to delete records
  * - lis
    - Event to list records
  * - err
    - Error in the application
  * - exc
    - Exception in the application



Obs
===

.. list-table:: Enum Definition
  :widths: 25
  :header-rows: 1

  * - Variable

  * - CPC_CMAP_URD
  * - CHIRPS
  * - TRMM
  * - CPC
  * - Chilestations
  * - ENACT



Mos
===

.. list-table:: Enum Definition
  :widths: 25
  :header-rows: 1

  * - Variable

  * - PCR
  * - CCA
  * - None


Predictand
==========

.. list-table:: Enum Definition
  :widths: 25
  :header-rows: 1

  * - Variable

  * - PRCP
  * - RFREQ


Predictors
==========

.. list-table:: Enum Definition
  :widths: 25
  :header-rows: 1

  * - Variable

  * - PRCP
  * - GCM
  * - VQ
  * - UQ
  * - T2M
