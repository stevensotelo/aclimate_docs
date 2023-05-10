Historical collections
######################

hs_climatology
==============

This collection contains the historical climatic data by month of each of the weather stations, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the historical climate data belongs.
    - ObjectId
  * - monthly_data
    - This parameter is an array that contains each of the months with its variable.
    - Array
  * - monthly_data.month
    - This parameter is an integer that represents the number of the month to which the data belongs.
    - Integer
  * - monthly_data.data
    - This parameter is an array that contains each of the mesaures (t_max, t_min, sol_rad and prec).
    - Array



.. image:: /_static/img/03-database-historical/hs_climatology_model.*
    :alt: Model of the table hs_climatology
    :class: device-screen-vertical side-by-side


hs_historical_climatic
======================

This collection contains the historical data of each year of each weather station, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the historical data belongs.
    - ObjectId
  * - year
    - This parameter represents the year to which the historical data belongs.
    - Integer
  * - monthly_data
    - This parameter is an array that contains each of the months with its variable.
    - Array
  * - monthly_data.month
    - This parameter is an integer that represents the number of the month to which the data belongs.
    - Integer
  * - monthly_data.data
    - This parameter is an array that contains each of the mesaures (t_max, t_min, sol_rad and prec).
    - Array



.. image:: /_static/img/03-database-historical/hs_historical_climatic_model.*
    :alt: Model of the table hs_historical_climatic
    :class: device-screen-vertical side-by-side



hs_historical_yield
===================

This collection contains the historical data of the yield data, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - source
    - This parameter corresponds to the Id of the source to which the historical yield data belongs.
    - ObjectId
  * - weather_station
    - This parameter indicates the ID of the weather station to which the historical yield data belongs.
    - ObjectId
  * - soil
    - This parameter indicates the ID of the soil to which the historical yield data belongs.
    - ObjectId
  * - cultivar
    - This parameter indicates the ID of the cultivar to which the historical yield data belongs.
    - ObjectId
  * - yield
    - This parameter contains the data, variables and values of the yield historical data.
    - ObjectId
  * - date
    - This parameter represents the date the record was saved.
    - Date


.. note::


    To learn more about the parameters inside the **yield** array: :ref:`Yield data`


.. image:: /_static/img/03-database-historical/hs_historical_yield_model.*
    :alt: Model of the table hs_historical_yield
    :class: device-screen-vertical side-by-side