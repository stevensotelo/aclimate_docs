.. _Recommendation endpoints:

Recommendation
##############



Through this endpoint you can obtain It provides a list of recommendations depending on whether you are in in-season or pre-season. This endpoint is used through the Http GET method.

Pre-season:

    * Recommendation of the best date to prepare the land.
    * Recommendation to know the best cultivar.
    * Recommendation to know the best planting date.

In season:

    * Recommendation regarding nitrogen and water stresses in the phenological phase in which the crop is located.
    * recommendations regarding extreme events linked to phenological phases.


To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Recommendation/RecommendationYield/** (https://webapi.aclimate.org/api/Recommendation/RecommendationYield/)
* This endpoint needs two parameters: 

    - **weather_stations:** You must enter the id of the weather station from which you want to get the information, if you want to obtain recommendations for different stations, you must separate each Id by ",".

    - **language:** It is the ISO 639-2 of each of the languages, it is used to filter the language of the recommendation. (By default in case of not passing the parameter it is **eng**)

    - **format:** to learn more about format parameter click here :ref:`format`.


The endpoint must follow the following format **https://webapi.aclimate.org/api/Recommendation/RecommendationYield/{weather_stations}/{language}/{format}** 

Examples: 

    - https://webapi.aclimate.org/api/Recommendation/RecommendationYield/5a7e22af57d7f316c8bc4ac6/eng/json 
    - https://webapi.aclimate.org/api/Recommendation/RecommendationYield/5a7e22af57d7f316c8bc4ac6/eng/csv 



.. _Recommendation key parameters:

.. list-table:: Recommendation key parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **tag**
    - key identifier.
    - String
  * - **id**
    - key identifier id.
    - ObjectId
  * - **value**
    - Id identifier value.
    - String



.. list-table:: Recommendation parameters
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Description
    - Type
  
  * - **ws_id**
    - This parameter indicates the ID of the weather station to which the recommendation belongs.
    - ObjectId
  * - **ws_name**
    - This parameter indicates the name of the weather station to which the recommendation belongs.
    - Double
  * - **type**
    - Indicates the type of recommendation to be displayed.
    - String
  * - **keys**
    - To learn more click here :ref:`Recommendation key parameters`.
    - Array of keys
  * - **content**
    - Corresponds to the recommendation that is being provided.
    - String



JSON format example:

.. image:: /_static/img/08-recommendation/recommendation_example_1.*
    :alt: recommendation_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-recommendation/recommendation_example_2.*
    :alt: recommendation_example_2 csv view
    :class: device-screen-vertical side-by-side




For the algorithm to decide if it is in in-season or pre-season, the forecast simulation start date is taken and if it is between the start and end date, in-season is taken, otherwise it's pre-season.

Pre-season
**********

In pre-season 3 recommendations are provided, recommendation of the best cultivar for each soil, recommendation of the best date to plant by soil and the recommendation of the range of dates to prepare the soils, for each one respectively the avg is taken to know the best scenery.
These data are taken from the outputs of the monthly forecast process.

In-season
*********

In-season, 2 recommendations are provided, a recommendation for the phenological phase and its respective level of stress, and a recommendation for extreme events.

For the recommendation of the phenological phase, the search for the current phase in which the crop is located is carried out, through the outputs obtained in the forecast with respect to the dates of each of the phenological phases, once the phenological phase has been obtained. The stress level is evaluated to provide the recommendation.

For the recommendation of extreme events, the dates of each indicator of extreme events are used to obtain the extreme event in which it is found to thus provide the recommendation.


For each of the recommendations, the language, the type of recommendation and the type of response are taken to perform the search for the recommendations stored in the database through WebAdmin and then the added variables are replaced in the recommendation text.