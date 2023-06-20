Web API
=======


Through the AClimate API you can obtain historical information, information obtained through the forecast process or the crop model, this is done through the use of the Endpoint that represents each of the data that you want to obtain.


The base Endpoint is built as follows:

    - **base_URL + /api + /(controller)/(specific module)/(parameters)**

    - Example: https://webapi.aclimate.org/api/Forecast/Historical/2018/json


.. _format:

format
******

All API endpoints have the **format** parameter which has the following format:

There are two options for the **format** parameter. 

 

    - JSON: It will deliver the information in JSON format. 

    - csv: It will deliver the information in a plain text file separated by "," (csv). 



If you want to try the AClimate API you can enter the following link where you will have access to all the API methods: https://webapi.aclimate.org/swagger/index.html


.. image:: /_static/img/08-webapi/swagger_doc.*
    :alt: swagger_doc
    :class: device-screen-vertical side-by-side



The API consists of a flow which must be followed to obtain the necessary information to perform the different API queries, such as obtaining historical data or forecast information.


To make correct use of the API endpoints, the following flow must be followed:

    * The first endpoint to which the query must be made is the gregraphic module and the geographic/Country/ endpoint, since it contains the necessary information on the countries of the system to perform the following queries. To know how this endpoint works and how to make the query, click here :ref:`Geographic Country`.
    * Once the ID of the country to which you want to obtain the information is obtained, you can obtain the different administrative levels and their information (in the system they are divided into states, municipalities and climatic stations) and the crops. To obtain the information of the administrative levels you must use the following endpoint :ref:`Geographic IdCountry`.
    * With the information from the weather stations, you can make queries to obtain information on historical weather data or information obtained from the forecast process. 
        
        - To obtain the information of the historical data you can access the following link :ref:`Historical information endpoints`. 
        - To obtain the information of the forecast you can access the following link :ref:`Forecast information endpoints`. 
        - Through the Id of the climatic stations you can obtain pre-season and in-season recommendations regarding this, to learn more click here :ref:`Recommendation endpoints`.


.. image:: /_static/img/08-webapi/api_flow.*
    :alt: api_flow
    :class: device-screen-vertical side-by-side