Historical
##########



Climatology
===========


Through this endpoint you can obtain the weather history of the selected weather station. This endpoint is used through the Http GET method.

To make use of this endpoint you must follow the following steps:

* This endpoint is made up of the **base_URL + /api + /Historical/Climatology/** (https://webapi.aclimate.org/api/Historical/Climatology/)
* This endpoint needs two parameters: 





 

weather_stations: You must enter the id of the weather station from which you want to get the information, if you want to obtain recommendations for different stations, you must separate each Id by ",". 

format: The format in which you want to obtain the information. 

 

There are two options for the format parameter. 

 

JSON: It will deliver the information in JSON format. 

 

csv: It will deliver the information in a plain text file separated by "," (csv). 

 

The endpoint must follow the following format https://webapi.aclimate.org/api/Recommendation/RecommendationYield/(weather_stations)/(format)  
Examples: https://webapi.aclimate.org/api/Recommendation/RecommendationYield/(5e91e1c214daf81260ebba59/json 
https://webapi.aclimate.org/api/Recommendation/RecommendationYield/(60a114538141a31200f3e5dc/json 

Note: Not all stations have this information. 

 

 

 

 

 

At this time, you will be able to get recommendations depending on whether it is pre-season or in-season. 

 

Pre-season: 

 

Recommendation of the best date to prepare the land. 

Recommendation to know the best cultivar. 

Recommendation to know the best planting date. 

 

In season. 

 

Recommendation regarding nitrogen and water stresses in the phenological phase in which the crop is located. 

 

 

Consult the aclimate API https://webapi.aclimate.org/api/ (For more information and documentation of other queries that can be made, please access the following link https://webapi.aclimate.org/swagger/index.html). 