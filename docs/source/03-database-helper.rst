Helpers structures
##################

cp_crop
=======

This collection contains all crops with their respective settings, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - name
    - This parameter corresponds to the name of the crop
    - String
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object
  * - crop_conf
    - This parameter contains the different crop configurations, having the maximum and minimum values for each phenological phase.
    - Array


.. note::


    To know more about the parameters inside the **crop_conf** array: :ref:`Crop configuration`



.. image:: /_static/img/03-database-helper/cp_crop_model.*
    :alt: Model of the collection cp_crop
    :class: device-screen-vertical side-by-side




cp_cultivar
===========

This collection contains all Cultivars of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - name
    - This parameter corresponds to the name of the crop
    - String
  * - crop
    - This parameter corresponds to the Id of the crop to which the cultivar belongs.
    - ObjectId
  * - order
    - This parameter establishes the way to list these, the higher the number, the more will be listed first.
    - Integer
  * - rainfed
    - This parameter indicates whether the cultivar is rainfed or irrigated.
    - Bool
  * - national
    - This parameter indicates whether the material is national or imported.
    - Bool
  * - country
    - This parameter corresponds to the Id of the country to which the cultivar belongs.
    - ObjectId
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object
  * - threshold
    - This parameter corresponds to the different thresholds of the cultivar, with their respective name and value.
    - Array


.. image:: /_static/img/03-database-helper/cp_cultivar_model.*
    :alt: Model of the collection cp_cultivar
    :class: device-screen-vertical side-by-side


cp_recommendation
=================

This collection contains all Cultivars of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - country
    - This parameter corresponds to the Id of the country to which the recommendation belongs.
    - ObjectId
  * - type_enum
    - This parameter contains the type of enum to which the recommendation belongs.
    - String
  * - type_resp
    - This parameter contains the type of response to which the recommendation belongs.
    - String
  * - resp
    - This parameter contains the response to which the replacements of the variables will be made.
    - String


.. image:: /_static/img/03-database-helper/cp_recommendation_model.*
    :alt: Model of the collection cp_recommendation
    :class: device-screen-vertical side-by-side



cp_setup
========

This parameter contains the configurations of the crops and their respective soils and cultivars, for the execution of the crop model process, This collection contains the following parameters:

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
    - This parameter contains the Id of the weather station to which the configuration belongs.
    - ObjectId
  * - cultivar
    - This parameter contains the Id of the cultivar to which the configuration belongs.
    - ObjectId
  * - soil
    - This parameter contains the Id of the soil to which the configuration belongs.
    - ObjectId
  * - crop
    - This parameter contains the Id of the crop to which the configuration belongs.
    - ObjectId
  * - days
    - This parameter represents the number of days that are used when running the crop model.
    - Double
  * - config_files
    - This parameter contains each of the files that this configuration contains, with the name, the path from which the file should be copied, and the date of registration.
    - Array
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object


.. image:: /_static/img/03-database-helper/cp_setup_model.*
    :alt: Model of the collection cp_setup
    :class: device-screen-vertical side-by-side



cp_soil
=======

This collection contains all soils of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier.
    - ObjectId
  * - name
    - This parameter corresponds to the name of the soil.
    - String
  * - country
    - This parameter corresponds to the Id of the country to which the soil belongs.
    - ObjectId
  * - order
    - This parameter establishes the way to list these, the higher the number, the more will be listed first.
    - Integer
  * - crop
    - This parameter contains the Id of the crop to which the soil belongs.
    - ObjectId
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object
  * - threshold
    - This parameter corresponds to the different thresholds of the soil, with their respective name and value.
    - Array


.. image:: /_static/img/03-database-helper/cp_soil_model.*
    :alt: Model of the collection cp_soil
    :class: device-screen-vertical side-by-side


lc_country
==========

This collection contains all countries of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - name
    - This parameter corresponds to the name of the country.
    - String
  * - iso2
    - This parameter contains the Iso2 format of the corresponding country. To know the format of the countries, you can access the following link: http://www.nationsonline.org/oneworld/country_code_list.htm.
    - String
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object
  * - conf_pycpt
    - This parameter corresponds to the configuration for seasonal forecast using pypct.
    - Array
  * - subseasonal_pycpt
    - This parameter corresponds to the configuration for subseasonal forecast using pypct.
    - Array
  * - seasonal_mode
    - This parameter corresponds to the mode in which the country executes seasonal climate forecast.
    - Integer
  * - subseasonal_mode
    - This parameter corresponds to the mode in which the country executes subseasonal climate forecast.
    - Integer


.. image:: /_static/img/03-database-helper/lc_country_model.*
    :alt: Model of the collection lc_country
    :class: device-screen-vertical side-by-side



lc_municipality
===============

This collection contains all municipalities of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - state
    - This parameter corresponds to the Id of the state to which the municipality belongs.
    - ObjectId
  * - name
    - This parameter corresponds to the name of the municipality.
    - String
  * - visible
    - This parameter allows you to activate or deactivate the municipality within the different AClimate pages and also in the forecast process.
    - Bool
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object


.. image:: /_static/img/03-database-helper/lc_municipality_model.*
    :alt: Model of the collection lc_municipality
    :class: device-screen-vertical side-by-side



lc_state
========

This collection contains all states of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - country
    - This parameter corresponds to the Id of the country to which the state belongs.
    - ObjectId
  * - name
    - This parameter corresponds to the name of the state.
    - String
  * - conf
    - This parameter contains the configurations of each quarter for the execution of cpt.
    - Array
  * - conf_pycpt
    - This parameter corresponds to the configuration for seasonal forecast using pypct.
    - Array
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object


.. note::


    To know more about the parameters inside the **quarter**: :ref:`Quarter`



.. image:: /_static/img/03-database-helper/lc_state_model.*
    :alt: Model of the collection lc_state
    :class: device-screen-vertical side-by-side


lc_weather_station
==================

This collection contains all weather stations of the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - name
    - This parameter corresponds to the name of the weather station.
    - String
  * - ext_id
    - This parameter corresponds to the Id of the data source (external id)
    - String
  * - country
    - This parameter corresponds to the Id of the municipality to which the weather station belongs.
    - ObjectId
  * - origin
    - This parameter corresponds to the name of entity owns this weather station.
    - String
  * - latitude
    - This parameter corresponds to the decimal latitude of the location of the weather station.
    - Double
  * - longitude
    - This parameter corresponds to the decimal longitude of the location of the weather station.
    - Double
  * - elevation
    - This parameter corresponds to the elevation of the weather station.
    - Double
  * - conf_files
    - This parameter contains each of the files that this configuration contains, with the name, the path from which the file should be copied, and the date of registration.
    - Array
  * - visible
    - This parameter allows you to activate or deactivate the weather station within the different AClimate pages and also in the forecast process.
    - Bool
  * - ranges
    - This parameter contains array of yield ranges of the crops for the weather station. It contains the parameters of the crop to which it belongs, the name of the range and the upper and lower.
    - Array
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object


.. image:: /_static/img/03-database-helper/lc_weather_station_model.*
    :alt: Model of the collection lc_weather_station
    :class: device-screen-vertical side-by-side