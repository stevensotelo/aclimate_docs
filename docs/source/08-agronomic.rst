Agronomy
########


Through this endpoint you can obtain a list of each soil and cultivar that each of the crops has. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Agronomic/** (https://webapi.aclimate.org/api/Agronomic/)
* This endpoint needs two parameters: 

    - **cultivar:** Boolean giving additional information if true such as cultivar rainfed and cultivar national.

    - **format:** to learn more about format parameter click here :ref:`format`.

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Agronomic/{cultivar}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Agronomic/true/json 
    - https://webapi.aclimate.org/api/Agronomic/false/csv 


.. list-table:: Agronomic - Output
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **cp_id**
    - It is the id of the crop.
    - ObjectId
  * - **cp_name**
    - It is the name of the crop.
    - String
  * - **soils**
    - It is a list of the crop soils, to learn more click here :ref:`Soil`.
    - Array of Soils
  * - **cultivars**
    - It is a list of the crop cultivars, to learn more click here :ref:`Cultivar`.
    - Array of Cultivars


.. _Soil:

.. list-table:: Soil
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - It is the Id of the soil.
    - ObjectId
  * - **name**
    - It is the name of the soil.
    - String
  * - **country_id**
    - It is the country id of the country to which the soil belongs.
    - ObjectId


.. _Cultivar:

.. list-table:: Cultivar
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - It is the Id of the cultivar.
    - ObjectId
  * - **name**
    - It is the name of the cultivar.
    - String
  * - **rainfed**
    - indicates whether the cultivar is rainfed or irrigated.
    - Bool
  * - **national**
    - indicates whether the material is national or imported.
    - Bool
  * - **country_id**
    - It is the country id of the country to which the cultivar belongs.
    - ObjectId


JSON format example:

.. image:: /_static/img/08-agronomic/agronomic_example_1.*
    :alt: agronomic_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-agronomic/agronomic_example_2.*
    :alt: agronomic_example_2 csv view
    :class: device-screen-vertical side-by-side

