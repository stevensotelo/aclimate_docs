Helpers structures
##################


.. _yield_data:

yield_data
==========

This entity represents the data of crop yield for different variables, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - measure
    - Name of the measured variable
    - MeasureYield
  * - avg
    - average
    - Double
  * - median
    - median
    - Double
  * - min
    - minimum value
    - Double
  * - max
    - maximum value
    - Double
  * - quar_1
    - quartile 1
    - Double
  * - quar_2
    - quartile 2
    - Double
  * - quar_3
    - quartile 3
    - Double
  * - conf_lower
    - lower confidence interval limit
    - Double
  * - conf_upper
    - upper confidence interval limit
    - Double
  * - sd
    - standard deviation
    - Double
  * - perc_5
    - 5th percentile
    - Double
  * - perc_95
    - 95th percentile
    - Double
  * - coef_var
    - coefficient of variation
    - Double



.. image:: /_static/img/03-database-helper/yield_data_model.*
    :alt: Model of the collection yield_data_model
    :class: device-screen-vertical side-by-side




yield_crop
==========

This entity represents the yield of a cultivar, a soil for a weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - start
    - Start date of the result of prediction
    - Date
  * - end
    - End date of the result of prediction
    - Date
  * - data
    - List of variables results yield forecasts
    - Array of YieldData




.. image:: /_static/img/03-database-helper/yield_crop_model.*
    :alt: Model of the collection yield_crop_model
    :class: device-screen-vertical side-by-side


.. _probability:

probability
===========

This entity represents the probabilities of the variables of climate prediction, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - measure
    - Variable's name
    - MeasureClimatic
  * - lower
    - Probability that is below normal
    - Double
  * - normal
    - Probability that is normal
    - Double
  * - upper
    - Normal probability that is above
    - Double



.. image:: /_static/img/03-database-helper/probability_model.*
    :alt: Model of the collection probability_model
    :class: device-screen-vertical side-by-side



performance_metric
==================

This entity represents an indicator of behavior prediction models, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - year
    - Year forecast
    - Integer
  * - month
    - Month forecast
    - Integer
  * - name
    - Metric name
    - MeasurePerformance
  * - value
    - Metric value
    - Double



.. image:: /_static/img/03-database-helper/performance_metric_model.*
    :alt: Model of the collection performance_metric_model
    :class: device-screen-vertical side-by-side




probability_climate
===================

This entity represents the probabilities of the variables of values of the prediction of every weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - year
    - Year forecast
    - Integer
  * - month
    - Month forecast
    - Integer
  * - probabilities
    - List of variables forecast for the month
    - Array of Probability



.. image:: /_static/img/03-database-helper/probability_climate_model.*
    :alt: Model of the collection probability_climate_model
    :class: device-screen-vertical side-by-side




probability_subseasonal
=======================

This entity represents the probabilities of the variables of values of the prediction of every weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - year
    - Year forecast
    - Integer
  * - month
    - Month forecast
    - Integer
  * - week
    - Week forecast
    - Integer
  * - probabilities
    - List of variables forecast for the month
    - Array of Probability



.. image:: /_static/img/03-database-helper/probability_subseasonal_model.*
    :alt: Model of the collection probability_subseasonal_model
    :class: device-screen-vertical side-by-side




threshold
=========

This entity represents the threshold of the soil or the cultivar, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - label
    - Label of the threshold
    - String
  * - value
    - percentage of the soil
    - Double



.. image:: /_static/img/03-database-helper/threshold_model.*
    :alt: Model of the collection threshold_model
    :class: device-screen-vertical side-by-side




crop_config
===========

This entity represents the crop config with the limit and upper of the variable, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - label
    - Label for the range
    - String
  * - min
    - Lower limit
    - Double
  * - max
    - Upper limit
    - Double
  * - type
    - percentage of the soil
    - String



.. image:: /_static/img/03-database-helper/crop_config_model.*
    :alt: Model of the collection crop_config_model
    :class: device-screen-vertical side-by-side




climate_configuration
=====================

This entity represents the cpt configurations by state taken into account at the time of the climatic forecast, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - state
    - ID's state
    - ObjectId
  * - conf
    - Contains the configurations of each quarter for the execution of cpt
    - Array of the ConfigurationCPT




.. image:: /_static/img/03-database-helper/climate_configuration_model.*
    :alt: Model of the collection climate_configuration_model
    :class: device-screen-vertical side-by-side




track
=====

This entity represents the history that an entity has had, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - enable
    - It indicates whether the entity is active or not. True is active, it is not false
    - Bool
  * - register
    - Date on which was register the entity to the database
    - Date
  * - updated
    - Date on which the last update of the entity was carried out in the database
    - Date




.. image:: /_static/img/03-database-helper/track_model.*
    :alt: Model of the collection track_model
    :class: device-screen-vertical side-by-side





monthly_data_station
====================

This entity represents the monthly climatological data from a weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - month
    - Month of the year
    - Integer
  * - data
    - Climatic data
    - Array of ClimaticData




.. image:: /_static/img/03-database-helper/monthly_data_station_model.*
    :alt: Model of the collection monthly_data_station_model
    :class: device-screen-vertical side-by-side


daily_readings
==============

This entity represents the daily climatic data from a weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - day
    - Day of the month
    - Integer
  * - data
    - Climatic data
    - Array of ClimaticData




.. image:: /_static/img/03-database-helper/daily_readings_model.*
    :alt: Model of the collection daily_readings_model
    :class: device-screen-vertical side-by-side



climatic_data
=============

This entity represents climatic data, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - measure
    - Variable's name
    - MeasureClimatic
  * - value
    - Variable's value
    - Double




.. image:: /_static/img/03-database-helper/climatic_data_model.*
    :alt: Model of the collection climatic_data_model
    :class: device-screen-vertical side-by-side





climatic_data
=============

This entity represents climatic data, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - measure
    - Variable's name
    - MeasureClimatic
  * - value
    - Variable's value
    - Double




.. image:: /_static/img/03-database-helper/climatic_data_model.*
    :alt: Model of the collection climatic_data_model
    :class: device-screen-vertical side-by-side



log
===

This entity has the activities record over platform, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - date
    - Date event
    - Date
  * - user
    - User that executed the event
    - String
  * - type_event
    - Event's name
    - LogEvent
  * - entities
    - List of entities affected in the event
    - Array of LogEntity
  * - content
    - Description's event
    - String




.. image:: /_static/img/03-database-helper/log_model.*
    :alt: Model of the collection log_model
    :class: device-screen-vertical side-by-side



yield_range
===========

This entity represents the yield ranges of the crops in the weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - crop
    - ID's crop
    - ObjectId
  * - label
    - Label of the range
    - String
  * - lower
    - Lower limit
    - Double
  * - upper
    - Upper limit
    - Double




.. image:: /_static/img/03-database-helper/yield_range_model.*
    :alt: Model of the collection yield_range_model
    :class: device-screen-vertical side-by-side




configuration_file
==================

This entity has the information about configurations files, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - name
    - Configuration's name
    - String
  * - path
    - Absolut path where the configuration file is located
    - String
  * - date
    - Date of file creation in the system
    - Date



.. image:: /_static/img/03-database-helper/configuration_file_model.*
    :alt: Model of the collection configuration_file_model
    :class: device-screen-vertical side-by-side




season
======

This entity represents the ranges of the planting window is active, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - start
    - Month when planting window start
    - String
  * - end
    - Month when planting window finish
    - String
  * - sowing_days
    - Sowing days it's a env equal to 45
    - Date



.. image:: /_static/img/03-database-helper/season_model.*
    :alt: Model of the collection season_model
    :class: device-screen-vertical side-by-side




configuration_cpt
=================

This entity represents the configuration that must be made at the time of generation of climate forecasts with cpt, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - trimester
    - Sets the quarter for which the forecast is made
    - Quarter
  * - regions
    - List of theoretical regions
    - Array of Region
  * - x_mode
    - Number of modes in x
    - Integer
  * - y_mode
    - Number of modes in y
    - Integer
  * - cca_mode
    - Number of modes in canonical correlation
    - Integer
  * - gamma
    - Sets if the gamma transformation is used
    - Bool
  * - track
    - Shows the trace of the changes that occurred in the entity
    - Track


.. image:: /_static/img/03-database-helper/configuration_cpt_model.*
    :alt: Model of the collection configuration_cpt_model
    :class: device-screen-vertical side-by-side




configuration_cpt
=================

This entity represents the configuration that must be made at the time of generation of climate forecasts with cpt, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - trimester
    - Sets the quarter for which the forecast is made
    - Quarter
  * - regions
    - List of theoretical regions
    - Array of Region
  * - x_mode
    - Number of modes in x
    - Integer
  * - y_mode
    - Number of modes in y
    - Integer
  * - cca_mode
    - Number of modes in canonical correlation
    - Integer
  * - gamma
    - Sets if the gamma transformation is used
    - Bool
  * - track
    - Shows the trace of the changes that occurred in the entity
    - Track


.. image:: /_static/img/03-database-helper/configuration_cpt_model.*
    :alt: Model of the collection configuration_cpt_model
    :class: device-screen-vertical side-by-side



region
======

This entity represents geographic regions in rectangular form, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - left_lower
    - Coordinates of the lower left corner of the theoretical area
    - Coords
  * - rigth_upper
    - Coordinates of the upper rigth corner of the theoretical area
    - Coords



.. image:: /_static/img/03-database-helper/region_model.*
    :alt: Model of the collection region_model
    :class: device-screen-vertical side-by-side



coords
======

This entity represents the geographic coordinates, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - lat
    - Decimal latitude of the location
    - Double
  * - lon
    - Decimal longitude of the location
    - Double



.. image:: /_static/img/03-database-helper/coords_model.*
    :alt: Model of the collection coords_model
    :class: device-screen-vertical side-by-side




configuration_pycpt
===================

This entity represents the configuration that must be made at the time of generation of climate forecasts with pycpt, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - spatial_predictors
    - Define the spatial region for predictors
    - Region
  * - spatial_predictands
    - Define the spatial region for predictands
    - Region
  * - models
    - List of models that will include in the forecast process
    - ModelsPyCpt
  * - obs
    - Type of observational data
    - Obs
  * - station
    - Define whether station
    - Bool
  * - mos
    - Define type of Mos
    - Mos
  * - predictand
    - Define the predictand
    - Predictand
  * - predictors
    - Define the predictors
    - Predictors
  * - month
    - Define the month of the year
    - Integer
  * - ranges_years
    - Define the ranges years
    - RangeParameter
  * - xmodes
    - Number of modes in x
    - RangeParameter
  * - ymodes
    - Number of modes in y
    - RangeParameter
  * - ccamodes
    - Number of modes in canonical correlation
    - RangeParameter
  * - force_download
    - Define whether force download
    - Bool
  * - single_models
    - Define whether single models
    - Bool
  * - forecast_anomaly
    - DDefine whether the forecast anomaly
    - Bool
  * - forecast_spi
    - Define whether the forecast spi
    - Bool
  * - confidence_level
    - Define the level of the confidence
    - Double
  * - track
    - Shows the trace of the changes that occurred in the entity
    - Track



.. image:: /_static/img/03-database-helper/configuration_pycpt_model.*
    :alt: Model of the collection configuration_pycpt_model
    :class: device-screen-vertical side-by-side





range_parameter
===============

This entity represents the ranges of the configs, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type


  * - min
    - Min value
    - Integer
  * - max
    - Max value
    - Integer



.. image:: /_static/img/03-database-helper/range_parameter_model.*
    :alt: Model of the collection range_parameter_model
    :class: device-screen-vertical side-by-side
