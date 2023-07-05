Spatial data
============

GeoServer is an open source server for sharing geospatial data. The GeoServer used by Aclimate is https://geo.aclimate.org/.
On the platform there are different workspaces, the ones used by aclimate have the following structure:

- aclimate_(country_id)
- aclimate_(region_id)

Example: aclimate_et

To search and view the different layers, on the home page you can click on the left area, on layer preview data. 

.. image:: /_static/img/09-geoserver/geoserver-home.*
  :alt: GeoServer home page
  :class: device-screen-vertical side-by-side

Once here, all the layers will be listed for viewing. You can filter in the search bar (where there is a magnifying glass) either by name of the workspace, example aclimate_et or by name or title of the layer.

.. image:: /_static/img/09-geoserver/geoserver-layer-preview.*
  :alt: GeoServer layer preview
  :class: device-screen-vertical side-by-side

The names of the layers related to Aclimate have the following structure:

Seasonal

country level

- seasonal_country_{country_id}_probabilistic_normal
- seasonal_country_{country_id}_probabilistic_below
- seasonal_country_{country_id}_probabilistic_above
- seasonal_country_{country_id}_deterministic
- seasonal_country_{country_id}_dominant

At the region level

- seasonal_region_{region_id}_probabilistic_normal
- seasonal_region_{region_id}_probabilistic_below
- seasonal_region_{region_id}_probabilistic_above
- seasonal_region_{region_id}_deterministic

Subseasonal

country level

- subseasonal_country_{country_id}_probabilistic_normal
- subseasonal_country_{country_id}_probabilistic_below
- subseasonal_country_{country_id}_probabilistic_above
- subseasonal_country_{country_id}_deterministic
- subseasonal_country_{country_id}_dominant

At the region level

- subseasonal_region_{region_id}_probabilistic_normal
- subseasonal_region_{region_id}_probabilistic_below
- subseasonal_region_{region_id}_probabilistic_above
- subseasonal_region_{region_id}_deterministic

The following keywords are relevant to layer search:

- crop (e.g. maize, coffee, etc) 
- group (e.g. dry_spells, heat_waves, spei, etc) 
- units (e.g. days, mm, etc) 
- acronym 
- period (e.g. [02-03,04-07,10-12]) 

Once you have searched for the layer of interest, clicking on OpenLayers will open a new page displaying the layer:

.. image:: /_static/img/09-geoserver/geoserver-layer-visualization.*
  :alt: GeoServer layer preview OpenLayers
  :class: device-screen-vertical side-by-side

If you want to change the time parameter of the layer to display it on different dates, you can do it as follows:

.. image:: /_static/img/09-geoserver/geoserver-layer-visualization-time.*
  :alt: GeoServer layer preview OpenLayers
  :class: device-screen-vertical side-by-side
