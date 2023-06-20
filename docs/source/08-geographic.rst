Geographic
##########

.. _Geographic Country:

Country
=======


Through this endpoint you can obtain a list with all the countries registered in the system. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Geographic/Country/** (https://webapi.aclimate.org/api/Geographic/Country/)
* This endpoint needs one parameter: 

    - **format:** to learn more about format parameter click here :ref:`format`.

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/Country/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/Country/json 
    - https://webapi.aclimate.org/api/Geographic/Country/csv 



.. _Country Parameters:

.. list-table:: Country Parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Corresponds to the Id of the country.
    - ObjectId
  * - **iso2**
    - Corresponds to the international ISO code that is assigned to each country. A list of ISO 2 codes for each country is available at http://www.nationsonline.org/oneworld/country_code_list.htm.
    - String
  * - **name**
    - Corresponds to the name of the country.
    - String



JSON format example:

.. image:: /_static/img/08-geographic/country_example_1.*
    :alt: country_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-geographic/country_example_2.*
    :alt: country_example_2 csv view
    :class: device-screen-vertical side-by-side


.. _Geographic IdCountry:

Geographic
==========


Through this endpoint you can obtain a list of the states of the selected country with each of their municipalities and weather stations and for each weather station their ranges for each crop. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Geographic/** (https://webapi.aclimate.org/api/Geographic/)
* This endpoint needs two parameters: 

    - **countryId:** Represents the id of the country from which you want to obtain the information.

    - **format:** to learn more about format parameter click here :ref:`format`.



The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/(countryId)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/61e59d829d5d2486e18d2ea8/json 
    - https://webapi.aclimate.org/api/Geographic/62a739250dd05810f0e2938d/csv 


.. _Weather station ranges:

.. list-table:: Weather station ranges
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **crop_id**
    - Corresponds to the id of the crop to which the range belongs.
    - ObjectId
  * - **crop_name**
    - Corresponds to the name of the crop to which the range belongs.
    - String
  * - **label**
    - Range name.
    - String
  * - **lower**
    - Minimum limit
    - Double
  * - **upper**
    - Maximum limit.
    - Double


.. _Weather stations parameters:

.. list-table:: Weather stations parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Unique identifier
    - ObjectId
  * - **name**
    - This parameter corresponds to the name of the weather station.
    - String
  * - **ext_id**
    - This parameter corresponds to the Id of the data source (external id)
    - String
  * - **ranges**
    - To learn more click here :ref:`Weather station ranges`.
    - Array of ranges
  * - **origin**
    - This parameter corresponds to the name of entity owns this weather station.
    - String
  * - **latitude**
    - This parameter corresponds to the decimal latitude of the location of the weather station.
    - Double
  * - **longitude**
    - This parameter corresponds to the decimal longitude of the location of the weather station.
    - Double


.. _Municipalities parameters:

.. list-table:: Municipalities parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Corresponds to the Id of the municipality.
    - ObjectId
  * - **name**
    - Corresponds to the name of the municipality.
    - String
  * - **weather_stations**
    - To learn more click here :ref:`Weather stations parameters`.
    - Arrays of weather stations


.. _State parameters:

.. list-table:: State parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Corresponds to the Id of state.
    - ObjectId
  * - **name**
    - Corresponds to the name of state.
    - String
  * - **country**
    - To learn more click here :ref:`Country Parameters`.
    - Country
  * - **municipalities**
    - To learn more click here :ref:`Municipalities parameters`.
    - Array of municipalities


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

    - **format:** to learn more about format parameter click here :ref:`format`.

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Geographic/Crop/(countryId)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Geographic/Crop/61e59d829d5d2486e18d2ea8/json 
    - https://webapi.aclimate.org/api/Geographic/Crop/62a739250dd05810f0e2938d/csv 



.. list-table:: Crop
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **id**
    - Corresponds to the id of the crop.
    - ObjectId
  * - **name**
    - Corresponds to the name of the crop.
    - String
  * - **states**
    - To learn more click here :ref:`State parameters`.
    - Array of states



JSON format example:

.. image:: /_static/img/08-geographic/country_crop_example_1.*
    :alt: country_crop_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-geographic/country_crop_example_2.*
    :alt: country_crop_example_2 csv view
    :class: device-screen-vertical side-by-side