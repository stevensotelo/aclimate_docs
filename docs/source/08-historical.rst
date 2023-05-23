Historical
##########



Climatology
===========


Through this endpoint you can obtain the weather history of the selected weather station. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Historical/Climatology/** (https://webapi.aclimate.org/api/Historical/Climatology/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain climatology for different stations, you must separate each Id by ",". 

    - **format:** The format in which you want to obtain the information. 



 

There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Historical/Climatology/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Historical/Climatology/5e91e1c214daf81260ebba59/json 
    - https://webapi.aclimate.org/api/Historical/Climatology/60a114538141a31200f3e5dc/csv 



JSON format example:

.. image:: /_static/img/08-historical/climatology_example_1.*
    :alt: climatology_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-historical/climatology_example_2.*
    :alt: climatology_example_2 csv view
    :class: device-screen-vertical side-by-side






HistoricalClimatic
==================


Through this endpoint you can obtain the historical climatic data of the selected weather station. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Historical/HistoricalClimatic/** (https://webapi.aclimate.org/api/Historical/HistoricalClimatic/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain historical climatic for different stations, you must separate each Id by ",". 

    - **format:** The format in which you want to obtain the information. 



 

There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Historical/HistoricalClimatic/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Historical/HistoricalClimatic/5e91e1c214daf81260ebba59/json 
    - https://webapi.aclimate.org/api/Historical/HistoricalClimatic/60a114538141a31200f3e5dc/csv 



JSON format example:

.. image:: /_static/img/08-historical/historical_climatic_example_1.*
    :alt: historical_climatic_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-historical/historical_climatic_example_2.*
    :alt: historical_climatic_example_2 csv view
    :class: device-screen-vertical side-by-side




HistoricalYieldYears
====================


Through this endpoint you can obtain the years that contain historical climatic data of the selected weather station. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Historical/HistoricalYieldYears/** (https://webapi.aclimate.org/api/Historical/HistoricalYieldYears/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain historical yield data for different stations, you must separate each Id by ",". 

    - **format:** The format in which you want to obtain the information. 



 

There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Historical/HistoricalYieldYears/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Historical/HistoricalYieldYears/58504f6a006cb93ed40eec8c/json 
    - https://webapi.aclimate.org/api/Historical/HistoricalYieldYears/58504f6a006cb93ed40eec8c/csv 



JSON format example:

.. image:: /_static/img/08-historical/historical_yield_year_example_1.*
    :alt: historical_yield_year_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-historical/historical_yield_year_example_3.*
    :alt: historical_yield_year_example_2 csv view
    :class: device-screen-vertical side-by-side




HistoricalYield
===============


Through this endpoint you can obtain the historical yield data per year of the selected weather station. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Historical/HistoricalYield/** (https://webapi.aclimate.org/api/Historical/HistoricalYield/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain historical yield data for different stations, you must separate each Id by ",". 

    - **format:** The format in which you want to obtain the information. 

    - **years:** You must enter the year from which you want to get the information, if you want to obtain historical yield data for different years, you must separate each year by ",".

 

There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Historical/HistoricalYield/(weather_stations)/(years)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Historical/HistoricalYield/58504f6a006cb93ed40eec8c/2004/json 
    - https://webapi.aclimate.org/api/Historical/HistoricalYield/58504f6a006cb93ed40eec8c/2004,2007/csv 



JSON format example:

.. image:: /_static/img/08-historical/historical_yield_example_1.*
    :alt: historical_yield_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-historical/historical_yield_example_2.*
    :alt: historical_yield_example_2 csv view
    :class: device-screen-vertical side-by-side