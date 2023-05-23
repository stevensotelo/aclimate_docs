Geographic
##########


Country
=======


Through this endpoint you can obtain a list with all the countries registered in the system. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Geographic/Country/** (https://webapi.aclimate.org/api/Geographic/Country/)
* This endpoint needs two parameters: 

    - **format:** The format in which you want to obtain the information. 


There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/Country/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/Country/json 
    - https://webapi.aclimate.org/api/Geographic/Country/csv 



JSON format example:

.. image:: /_static/img/08-geographic/country_example_1.*
    :alt: country_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-geographic/country_example_2.*
    :alt: country_example_2 csv view
    :class: device-screen-vertical side-by-side




countryId
=========


Through this endpoint you can obtain a list of the states of the selected country with each of their municipalities and weather stations and for each weather station their ranges for each crop. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Geographic/** (https://webapi.aclimate.org/api/Geographic/)
* This endpoint needs two parameters: 

    - **countryId:** Represents the id of the country from which you want to obtain the information.

    - **format:** The format in which you want to obtain the information. 


There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/(countryId)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/61e59d829d5d2486e18d2ea8/json 
    - https://webapi.aclimate.org/api/Geographic/62a739250dd05810f0e2938d/csv 



JSON format example:

.. image:: /_static/img/08-geographic/country_id_example_1.*
    :alt: country_id_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-geographic/country_id_example_2.*
    :alt: country_id_example_2 csv view
    :class: device-screen-vertical side-by-side




Crop
====


Through this endpoint you can obtain a list of the states of the selected country with each of their municipalities and weather stations and for each weather station their ranges for each crop grouped by each crop. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Geographic/Crop/** (https://webapi.aclimate.org/api/Geographic/Crop/)
* This endpoint needs two parameters: 

    - **countryId:** Represents the id of the country from which you want to obtain the information.

    - **format:** The format in which you want to obtain the information. 


There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/Crop/(countryId)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/Crop/61e59d829d5d2486e18d2ea8/json 
    - https://webapi.aclimate.org/api/Geographic/Crop/62a739250dd05810f0e2938d/csv 



JSON format example:

.. image:: /_static/img/08-geographic/country_crop_example_1.*
    :alt: country_crop_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-geographic/country_crop_example_2.*
    :alt: country_crop_example_2 csv view
    :class: device-screen-vertical side-by-side