Spatial data
============

GeoServer is an open source server for sharing geospatial data. The GeoServer used by Aclimate is https://geo.aclimate.org/.
On the platform there are different workspaces:

- aclimate_et - seasonal and subseasonal layers for Ethiopia
- aclimate_gt - seasonal layers for Guatemala
- agroclimate_indices_ao - agroclimate indices for Angola
- climate_extreme_indices_et - climate extreme indices for Ethiopia 		
- climate_indices_pe - climate indices for Peru

To search and view the different layers, on the home page you can click on the left area, on layer preview data. 

.. image:: /_static/img/09-geoserver/geoserver-home.*
  :alt: GeoServer home page
  :class: device-screen-vertical side-by-side

Once here, all the layers will be listed for viewing. You can filter in the search bar (where there is a magnifying glass) either by name of the workspace, example aclimate_et or by name or title of the layer.

.. image:: /_static/img/09-geoserver/geoserver-layer-preview.*
  :alt: GeoServer layer preview
  :class: device-screen-vertical side-by-side

**Click for** `search a layer <https://geo.aclimate.org/geoserver/web/wicket/bookmarkable/org.geoserver.web.demo.MapPreviewPage?1&filter=false>`_

The following keywords are relevant to layer search:

- crop (e.g. maize, coffee, etc) 
- group (e.g. dry_spells, heat_waves, spei, etc) 
- units (e.g. days, mm, etc) 
- acronym 
- period (e.g. [02-03,04-07,10-12])
- season (e.g. seasonal, subseasonal) 
- scenario (e.g. above, normal, below)
- country iso (e.g. et, gt, ao, pe)
- workspaces (e.g. aclimate_et, aclimate_gt, agroclimate_indices_ao, climate_extreme_indices_et, climate_indices_pe)

Once you have searched for the layer of interest, clicking on OpenLayers will open a new page displaying the layer:

.. image:: /_static/img/09-geoserver/geoserver-layer-visualization.*
  :alt: GeoServer layer preview OpenLayers
  :class: device-screen-vertical side-by-side

If you want to change the time parameter of the layer to display it on different dates, you can do it by adding the follows:

.. image:: /_static/img/09-geoserver/geoserver-layer-visualization-time.*
  :alt: GeoServer layer preview OpenLayers
  :class: device-screen-vertical side-by-side

For **Peru's climate indices**, the corresponding years to El Nino y La Nina are 1977 and 1978.


