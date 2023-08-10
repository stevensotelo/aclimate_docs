.. _Forecast information endpoints:


Forecast
########


Climate
=======


Through this endpoint you can obtain the information obtained through the forecast process, the probabilities and the climatic scenarios. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/Climate/** (https://webapi.aclimate.org/api/Forecast/Climate/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain forecast information for different stations, you must separate each Id by ",". 

    - **probabilities:** If this parameter is true it will show the information of the probabilities if it is false it will show the information of the climatic scenarios in the csv format.

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Climate/{weather_stations}/{probabilities}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Climate/5a7e22af57d7f316c8bc4ac6/true/json 
    - https://webapi.aclimate.org/api/Forecast/Climate/5a7e22af57d7f316c8bc4ac6/false/csv 


.. _Data - Climate:

.. list-table:: Data - Climate
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **year**
    - It represents the year to which the probabilities correspond.
    - Integer
  * - **month**
    - It represents the month to which the probabilities correspond.
    - Integer
  * - **probabilities**
    - To learn more click here :ref:`probability`.
    - Array of probabilities


.. _Performance:

.. list-table:: Performance
  :widths: 25 25 25
  :header-rows: 1

  * - **year**
    - It represents the year to which the perfomance correspond.
    - Integer
  * - **month**
    - It represents the month to which the perfomance correspond.
    - Integer
  * - **name**
    - It represents the name to which the perfomance correspond.
    - String
  * - **value**
    - It represents the value of the performance.
    - Double


.. _Climate:

.. list-table:: Climate
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **weather_station**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - **performance**
    - To learn more click here :ref:`Performance`.
    - Array of performance
  * - **data**
    - To learn more click here :ref:`Data - Climate`.
    - Array of data


.. _monthly_data:

.. list-table:: monthly_data
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type

  * - **month**
    - Represents the month
    - Integer
  * - **data**
    - Contains each variable with its respective value
    - Array of data
  * - **data.measure**
    - Variable name
    - String
  * - **data.value**
    - Variable value
    - Double


.. _Scenario:

.. list-table:: Scenario
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **weather_station**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - **name**
    - This parameter indicates the ID of the forecast to which the forecast data belongs.
    - String
  * - **year**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - Integer
  * - **monthly_data**
    - To learn more click here :ref:`monthly_data`.
    - Array of monthly data



.. list-table:: Forecast Climate
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs.
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **climate**
    - To learn more click here :ref:`Climate`.
    - Array of climates.
  * - **scenario**
    - To learn more click here :ref:`Scenario`.
    - Array of scenarios.



JSON format example:

.. image:: /_static/img/08-forecast/climate_example_1.*
    :alt: climate_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example when probabilities is true:

.. image:: /_static/img/08-forecast/climate_example_2.*
    :alt: climate_example_2 csv view
    :class: device-screen-vertical side-by-side


CSV format example when probabilities is false:

.. image:: /_static/img/08-forecast/climate_example_3.*
    :alt: climate_example_3 csv view
    :class: device-screen-vertical side-by-side



Yield
=====


Through this endpoint you can obtain the information obtained through the crop model process, yield data. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/Yield/** (https://webapi.aclimate.org/api/Forecast/Yield/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain yield data obtained from the crop model for different stations, you must separate each Id by ",". 

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Yield/{weather_stations}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Yield/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/Yield/5a7e22af57d7f316c8bc4ac6/csv 


.. _Yield Crop:

.. list-table:: Yield Crop
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **cultivar**
    - It is the cultivar id of the cultivar to which the yield data belongs.
    - ObjectId
  * - **soil**
    - It is the soil id of the soil to which the yield data belongs.
    - ObjectId
  * - **start**
    - Corresponds to the simulation start date.
    - Date
  * - **end**
    - Corresponds to the simulation end date.
    - Date
  * - **data**
    - To learn more click here :ref:`yield_data`.
    - Array of yield data


.. _Yield:

.. list-table:: Yield
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **weather_station**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - **yield**
    - To learn more click here :ref:`Yield Crop`.
    - Array of yield crop


.. list-table:: Forecast Yield
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs.
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **yield**
    - To learn more click here :ref:`Yield`.
    - Array of yield.


JSON format example:

.. image:: /_static/img/08-forecast/yield_example_1.*
    :alt: yield_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/yield_example_2.*
    :alt: yield_example_2 csv view
    :class: device-screen-vertical side-by-side




YieldExceedance
===============


Through this endpoint you can obtain the information obtained through of all forecast in the crop model process, yield data. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/YieldExceedance/** (https://webapi.aclimate.org/api/Forecast/YieldExceedance/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain yield data obtained from the forecast for different stations, you must separate each Id by ",". 

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/YieldExceedance/{weather_stations}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/YieldExceedance/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/YieldExceedance/5a7e22af57d7f316c8bc4ac6/csv 




.. list-table:: Forecast Yield Exceedance
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs. Contains multiple forecast Ids separated by ",".
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **yield**
    - To learn more click here :ref:`Yield`.
    - Array of yield.


JSON format example:

.. image:: /_static/img/08-forecast/yield_exceedance_example_1.*
    :alt: yield_exceedance_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/yield_exceedance_example_2.*
    :alt: yield_exceedance_example_2 csv view
    :class: device-screen-vertical side-by-side




SubseasonalWS
=============


Through this endpoint you can obtain the information obtained through the forecast process for subseasonal, the probabilities and the climatic scenarios. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/SubseasonalWS/** (https://webapi.aclimate.org/api/Forecast/SubseasonalWS/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain forecast information for different stations, you must separate each Id by ",".  

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/SubseasonalWS/{weather_stations}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/SubseasonalWS/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/SubseasonalWS/5a7e22af57d7f316c8bc4ac6/csv 



.. _Subseasonal Data - Climate:

.. list-table:: Subseasonal Data - Climate
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **year**
    - It represents the year to which the probabilities correspond.
    - Integer
  * - **month**
    - It represents the month to which the probabilities correspond.
    - Integer
  * - **week**
    - It represents the week to which the probabilities correspond.
    - Integer
  * - **probabilities**
    - To learn more click here :ref:`probability`.
    - Array of probabilities


.. _Climate Subseasonal:

.. list-table:: Climate Subseasonal
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **weather_station**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - **data**
    - To learn more click here :ref:`Subseasonal Data - Climate`.
    - Array of data


.. list-table:: Forecast SubseasonalWS
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs.
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **climate**
    - To learn more click here :ref:`Climate Subseasonal`.
    - Array of climates.


JSON format example:

.. image:: /_static/img/08-forecast/subseasonal_example_1.*
    :alt: subseasonal_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/subseasonal_example_2.*
    :alt: subseasonal_example_2 csv view
    :class: device-screen-vertical side-by-side




Historical
==========


Through this endpoint you can obtains the forecast information for a specific year indicated in the parameters. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/Log/** (https://webapi.aclimate.org/api/Forecast/Log/)
* This endpoint needs two parameters: 

    - **year:** The year from which the forecast information will be obtained.

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Log/{year}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Log/2018/json 
    - https://webapi.aclimate.org/api/Forecast/Log/2020/csv 




.. list-table:: Forecast Historical
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Indicates the id of the forecast.
    - ObjectId
  * - **start**
    - Corresponds to the start date of the forecast.
    - Date
  * - **end**
    - Corresponds to the end date of the forecast.
    - Date
  * - **confindece**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double.


JSON format example:

.. image:: /_static/img/08-forecast/historical_example_1.*
    :alt: historical_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/historical_example_2.*
    :alt: historical_example_2 csv view
    :class: device-screen-vertical side-by-side





YieldPrevious
=============


Through this endpoint you can obtains the forecast information for a specific forecast indicated in the parameters. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/YieldPrevious/** (https://webapi.aclimate.org/api/Forecast/YieldPrevious/)
* This endpoint needs two parameters: 

    - **forecast:** Represents the id of the forecast from which the information is desired.

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain forecast information for different stations, you must separate each Id by ",".  

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/YieldPrevious/{forecast}/{weather_stations}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/YieldPrevious/6435c8429a5fca102dde5666/5a7e22af57d7f316c8bc4ac6/json
    - https://webapi.aclimate.org/api/Forecast/YieldPrevious/6435c8429a5fca102dde5666/5a7e22af57d7f316c8bc4ac6/csv 


.. list-table:: Forecast YieldPrevious
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs.
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **yield**
    - To learn more click here :ref:`Yield`.
    - Array of yield.


JSON format example:

.. image:: /_static/img/08-forecast/yieldprevious_example_1.*
    :alt: yieldprevious_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/yieldprevious_example_2.*
    :alt: yieldprevious_example_2 csv view
    :class: device-screen-vertical side-by-side





Climate Previous
================


Through this endpoint you can obtain the information obtained through the forecast process that is desired by means of the Id, the seasonal and subseasonal probabilities and the climatic scenarios. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/ClimatePrevious/** (https://webapi.aclimate.org/api/Forecast/ClimatePrevious/)
* This endpoint needs two parameters: 

    - **forecast:** Represents the id of the forecast from which the information is desired.

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain forecast information for different stations, you must separate each Id by ",". 

    - **probabilities:** If this parameter is true it will show the information of the probabilities if it is false it will show the information of the climatic scenarios in the csv format.

    - **format:** to learn more about format parameter click here :ref:`format`.


 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/ClimatePrevious/{forecast}/{weather_stations}/{probabilities}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/ClimatePrevious/648202f6a0488e3540a59e4e/60a114538141a31200f3e678/true/json 
    - https://webapi.aclimate.org/api/Forecast/ClimatePrevious/648202f6a0488e3540a59e4e/60a114538141a31200f3e678/false/csv 



.. _Climate Previous:

.. list-table:: Climate Previous
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **weather_station**
    - This parameter indicates the ID of the weather station to which the forecast data belongs.
    - ObjectId
  * - **performance**
    - To learn more click here :ref:`Performance`.
    - Array of performance
  * - **data**
    - To learn more click here :ref:`Data - Climate`.
    - Array of data
  * - **subseasonal_data**
    - To learn more click here :ref:`Subseasonal Data - Climate`.
    - Array of data



.. list-table:: Forecast Climate
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **forecast**
    - Indicates the id of the forecast to which the data belongs.
    - ObjectId
  * - **confidence**
    - This parameter indicates the confidence value for the intervals confidence.
    - Double
  * - **climate**
    - To learn more click here :ref:`Climate Previous`.
    - Array of climates.
  * - **scenario**
    - To learn more click here :ref:`Scenario`.
    - Array of scenarios.



JSON format example:

.. image:: /_static/img/08-forecast/climateprevious_example_1.*
    :alt: climateprevious_example_1 json view
    :class: device-screen-vertical side-by-side


JSON format example 2:

.. image:: /_static/img/08-forecast/climateprevious_example_1-2.*
    :alt: climateprevious_example_1-2 csv view
    :class: device-screen-vertical side-by-side


CSV format example when probabilities is false:

.. image:: /_static/img/08-forecast/climateprevious_example_2.*
    :alt: climateprevious_example_2 csv view
    :class: device-screen-vertical side-by-side

