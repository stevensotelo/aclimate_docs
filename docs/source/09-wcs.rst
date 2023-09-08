WCS
============

WCS is a service that allows downloading of layers. To use this service, the following URL will be used as a base:

* https://geo.aclimate.org/geoserver/workspace_name/ows?service=WCS&request=GetCoverage&version=2.0.1&coverageId=layer_name&format=format&time=date

Parameters:

- workspace_name e.g. agroclimate_indices_ao
- layer_name e.g. coffee_number_dry_spells
- format e.g. image/geotiff
- time e.g. 1979-0

Change the parameters according to your needs. In the example layer the final URL would be the following:

https://geo.aclimate.org/geoserver/agroclimate_indices_ao/ows?service=WCS&request=GetCoverage&version=2.0.1&coverageId=coffee_number_dry_spells&format=image/geotiff&time=1979-0