Forecast
########


Climate
=======


Through this endpoint you can obtain the information obtained through the forecast process, the probabilities and the climatic scenarios.. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Forecast/Climate/** (https://webapi.aclimate.org/api/Forecast/Climate/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain forecast information for different stations, you must separate each Id by ",". 

    - **probabilities:** If this parameter is true it will show the information of the probabilities if it is false it will show the information of the climatic scenarios in the csv format.

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Climate/(weather_stations)/(probabilities)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Climate/5a7e22af57d7f316c8bc4ac6/true/json 
    - https://webapi.aclimate.org/api/Forecast/Climate/5a7e22af57d7f316c8bc4ac6/false/csv 



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

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Yield/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Yield/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/Yield/5a7e22af57d7f316c8bc4ac6/csv 



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

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/YieldExceedance/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/YieldExceedance/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/YieldExceedance/5a7e22af57d7f316c8bc4ac6/csv 



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

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/SubseasonalWS/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/SubseasonalWS/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Forecast/SubseasonalWS/5a7e22af57d7f316c8bc4ac6/csv 



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

* This endpoint is made up of the **base_URL + /api + /Forecast/Historical/** (https://webapi.aclimate.org/api/Forecast/Historical/)
* This endpoint needs two parameters: 

    - **year:** The year from which the forecast information will be obtained.

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/Historical/(year)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/Historical/2018/json 
    - https://webapi.aclimate.org/api/Forecast/Historical/2020/csv 



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

    - **format:** The format in which you want to obtain the information. 



There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Forecast/YieldPrevious/(forecast)/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Forecast/YieldPrevious/6435c8429a5fca102dde5666/5a7e22af57d7f316c8bc4ac6/json
    - https://webapi.aclimate.org/api/Forecast/YieldPrevious/6435c8429a5fca102dde5666/5a7e22af57d7f316c8bc4ac6/csv 



JSON format example:

.. image:: /_static/img/08-forecast/yieldprevious_example_1.*
    :alt: yieldprevious_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-forecast/yieldprevious_example_2.*
    :alt: yieldprevious_example_2 csv view
    :class: device-screen-vertical side-by-side