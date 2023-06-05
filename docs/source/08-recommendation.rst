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

    - **weather_stations**: You must enter the id of the weather station from which you want to get the information, if you want to obtain recommendations for different stations, you must separate each Id by ",".

    - **format:** The format in which you want to obtain the information. 


There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format **https://webapi.aclimate.org/api/Recommendation/RecommendationYield/(weather_stations)/(format)** 

Examples: 

    - https://webapi.aclimate.org/api/Recommendation/RecommendationYield/5a7e22af57d7f316c8bc4ac6/json 
    - https://webapi.aclimate.org/api/Recommendation/RecommendationYield/5a7e22af57d7f316c8bc4ac6/csv 



JSON format example:

.. image:: /_static/img/08-recommendation/recommendation_example_1.*
    :alt: recommendation_example_1 json view
    :class: device-screen-vertical side-by-side


CSV format example:

.. image:: /_static/img/08-recommendation/recommendation_example_2.*
    :alt: recommendation_example_2 csv view
    :class: device-screen-vertical side-by-side

