Forecast collections
####################


fs_forecast
===========

This collection contains each of the forecasts that are made month by month, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Forecast unique identifier
    - ObjectId
  * - start
    - Simulation start date.
    - Date
  * - end
    - Simulation end date.
    - Date
  * - confidence
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - track
    - This parameter contains other parameters that are used for deletion logic and other settings.
    - Object
  * - track.enable
    - The enable parameter indicates whether the forecast is enabled to be taken into account by the system or not.
    - Bool
  * - track.register
    - This parameter indicates the date the forecast was registered in the system.
    - Date
  * - track.updated
    - This parameter indicates the date of the last update of some forecast parameter.
    - Date
  * - climate_conf
    - Forecast unique identifier
    - Array


.. note::


    To learn more about the parameters inside the **climate_conf** array: :ref:`Forecast Meanings`


.. image:: /_static/img/03-database-forecast/fs_forecast_model.*
    :alt: Model of the table forecast
    :class: device-screen-vertical side-by-side


fs_forecast_climate
===================

This collection contains each of the forecasts that are made month by month, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - forecast
    - This parameter indicates the ID of the forecast to which the forecast data belongs.
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - data
    - This parameter contains the probabilities divided by year and month.
    - Array
  * - data.year
    - It represents the year to which the probabilities correspond.
    - Integer
  * - data.month
    - It represents the month to which the probabilities correspond.
    - Integer
  * - data.probabilities
    - This parameter contains the probabilities divided by year and month.
    - Array
  * - data.probabilities.measure
    - Corresponds to the variable which has the probabilities
    - String
  * - data.probabilities.lower
    - It corresponds to the probability of being below normal.
    - Double
  * - data.probabilities.normal
    - It corresponds to the probability of being in the normal.
    - Double
  * - data.probabilities.upper
    - It corresponds to the probability of being above normal.
    - Double
  * - performance
    - This parameter contains other parameters that are used for deletion logic and other settings.
    - Array
  * - performance.year
    - It represents the year to which the perfomance correspond.
    - Integer
  * - performance.month
    - It represents the month to which the perfomance correspond.
    - Integer
  * - performance.name
    - It represents the name to which the perfomance correspond.
    - String
  * - performance.value
    - It represents the value of the performance.
    - Double
  * - subseasonal
    - It represents the value of the performance.
    - Double
  * - subseasonal.week
    - It represents the week to which the probabilities correspond.
    - Double


.. note::


    The subseasonal parameter has the same parameters as the **data** parameter, it only has the additional **week** parameter.


.. image:: /_static/img/03-database-forecast/fs_forecast_climate_model.*
    :alt: Model of the table forecast_climate
    :class: device-screen-vertical side-by-side



fs_forecast_scenario
====================

This collection contains each of the forecasts that are made month by month, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - forecast
    - This parameter indicates the ID of the forecast to which the forecast data belongs.
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - name
    - This parameter indicates the ID of the forecast to which the forecast data belongs.
    - String
  * - year
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - Integer
  * - monthly_data
    - Contains the data of each variable divided by month
    - Array
  * - monthly_data.month
    - Represents the month
    - Integer
  * - monthly_data.data
    - Contains each variable with its respective value
    - Array


.. note::


    To learn more about the parameters inside the **climate_conf** array: :ref:`Forecast Meanings`


.. image:: /_static/img/03-database-forecast/fs_forecast_scenarios_model.*
    :alt: Model of the table forecast_scenarios
    :class: device-screen-vertical side-by-side



List and description of all collections of forecast


fs_forecast_yield
=================

This collection contains the variables obtained by executing the crop model process during the forecast, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - forecast
    - This parameter indicates the ID of the forecast to which the forecast yield data belongs.
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the forecast yield data belongs.
    - ObjectId
  * - soil
    - This parameter indicates the ID of the soil to which the forecast yield data belongs.
    - ObjectId
  * - cultivar
    - This parameter indicates the ID of the cultivar to which the forecast yield data belongs.
    - ObjectId
  * - yield
    - It represents the month to which the probabilities correspond.
    - Array


.. note::


    To learn more about the parameters inside the **yield** array: :ref:`Yield data`


    To learn more about the mesaure yields inside the **yield_data** array: :ref:`Measure Yield Definition`

.. image:: /_static/img/03-database-forecast/fs_forecast_yield_model.*
    :alt: Model of the table forecast_yield
    :class: device-screen-vertical side-by-side



fs_forecast_phen_phase
======================

This collection contains the dates generated by each forecast of each of the phenological phases, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - forecast
    - This parameter corresponds to the Id of the forecast to which this record of the phenological phases belongs.
    - ObjectId
  * - ws
    - This parameter corresponds to the Id of the weather station to which this record of the phenological phases belongs.
    - ObjectId
  * - soil
    - This parameter corresponds to the Id of the soil to which this record of the phenological phases belongs.
    - ObjectId
  * - cultivar
    - This parameter corresponds to the Id of the cultivar to which this record of the phenological phases belongs.
    - ObjectId
  * - phases_crop
    - This parameter contains both the start and end date of the simulation and within this contains each of the phenological phases with their date ranges.
    - Array



.. image:: /_static/img/03-database-forecast/fs_forecast_phases_model.*
    :alt: Model of the table forecast_phases
    :class: device-screen-vertical side-by-side
