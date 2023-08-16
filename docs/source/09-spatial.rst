Spatial data
============

GeoServer is an open source server for sharing geospatial data. The GeoServer used by Aclimate is https://geo.aclimate.org/.
On the platform there are different workspaces:


aclimate_et
  * **description:** seasonal and subseasonal layers for Ethiopia
  * **data type:** raster files (.tif)
  * **keywords relevant to layer search:**  seasonal, subseasonal, above, normal, below 
layer name structure: 
  * seasonal/subseasonal_country_et_probabilistic_normal 
  * seasonal/subseasonal_country_et_probabilistic_below 
  * seasonal/subseasonal_country_et_probabilistic_above 
  * seasonal/subseasonal_country_et_deterministic 
  * seasonal/subseasonal_country_et_dominant 

-------------------------------------------------------------------

aclimate_gt
  * **description:** seasonal layers for Guatemala
  * **data type:** raster files (.tif)
  * **keywords relevant to layer search:** seasonal, above, normal, below 
layer name structure: 
  * seasonal_country_gt_probabilistic_normal 
  * seasonal_country_gt_probabilistic_below 
  * seasonal_country_gt_probabilistic_above 
  * seasonal_country_gt_dominant

-------------------------------------------------------------------

agroclimate_indices_ao
  * **description:** agroclimate indices for Angola
  * **data type:** raster files (.tif)
  * **keywords relevant to layer search:** coffee, dry_bean, maize, soybean, dry_spells, heat_waves, spei, etc.
layer name structure: 
  * {crop}_{indicator}_{unit} 

-------------------------------------------------------------------

climate_extreme_indices_et
  * **description:** climate extreme indices for Ethiopia 
  * **data type:** raster files (.tif)
  * **keywords relevant to layer search:** mm, day, spei, spi, tm, tn, etc.
layer name structure: 
  * {indice}

-------------------------------------------------------------------

climate_indices_pe
  * **description:** climate indices for Peru 
  * **data type:** raster files (.tif)
  * **keywords relevant to layer search:** total_rainfall, r1_mm, r10_mm, r1mm_periods, t_30, t30_periods, etc.
layer name structure: 
  * {indicator}
 	
-------------------------------------------------------------------

administrative
  * **description:** administrative levels for country
  * **data type:** shapefiles (.shp)
  * **keywords relevant to layer search:** ao, et, adm1, adm2, adm3, adm4.
layer name structure: 
  * {country_iso}_adm1/adm2/adm3/adm4
shapefiles fields:
  * **ao_adm1**: fid, name_adm1, id_adm1
  * **ao_adm2**: fid, id_adm1, name_adm1, id_adm2, name_adm2
  * **et_adm1**: fid, ADM1_EN, ADM1_PCODE
  * **et_adm2**: fid, ADM2_EN, ADM2_PCODE, ADM1_EN, ADM1_PCODE
  * **et_adm3**: fid, ADM3_EN, ADM3_PCODE, ADM2_EN, ADM2_PCODE, ADM1_EN, ADM1_PCODE
  * **et_adm4**: fid, id_adm1, id_adm2, id_adm3, id_adm4, name_adm1, name_adm2, name_adm3, name_adm4, ws_id


To search and view the different layers, on the home page you can click on the left area, on layer preview data. 

.. image:: /_static/img/09-geoserver/geoserver-home.*
  :alt: GeoServer home page
  :class: device-screen-vertical side-by-side

Once here, all the layers will be listed for viewing. You can filter in the search bar (where there is a magnifying glass) either by name of the workspace, example aclimate_et or by name or title of the layer.

.. image:: /_static/img/09-geoserver/geoserver-layer-preview.*
  :alt: GeoServer layer preview
  :class: device-screen-vertical side-by-side

**Click for** `search a layer <https://geo.aclimate.org/geoserver/web/wicket/bookmarkable/org.geoserver.web.demo.MapPreviewPage?1&filter=false>`_


To use the **WMS** service to download a layer, you can click All Formats and select the desired download format. 

.. image:: /_static/img/09-geoserver/geoserver-layer-download.*
  :alt: GeoServer layer download
  :class: device-screen-vertical side-by-side

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


