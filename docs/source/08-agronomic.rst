Agronomy
########


Through this endpoint you can obtain It provides a list of each soil and cultivar that each of the crops has. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Agronomy/** (https://webapi.aclimate.org/api/Agronomy/)
* This endpoint needs two parameters: 

    - **cultivar:** Boolean giving additional information if true such as cultivar rainfed and cultivar national.

    - **format:** The format in which you want to obtain the information. 


There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Agronomy/(cultivar)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Agronomy/true/json 
    - https://webapi.aclimate.org/api/Agronomy/false/csv 



JSON format example:

.. image:: /_static/img/08-agronomic/agronomic_example_1.*
    :alt: agronomic_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-agronomic/agronomic_example_2.*
    :alt: agronomic_example_2 csv view
    :class: device-screen-vertical side-by-side

