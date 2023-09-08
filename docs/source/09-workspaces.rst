Workspaces
##########

On the platform there are different workspaces for different data purposes. The different categories and structure of each workspace are presented below:

Forecast data
=============

aclimate_{country_iso}
  * **description:** seasonal and subseasonal layers for a country
  * **data type:** raster files (.tif) image mosaic
  * **keywords relevant to layer search:**  seasonal, subseasonal, above, normal, below 
layer name structure: 
  * {seasonal|subseasonal}_country_{country_iso}_probabilistic_{scenario}
  * {seasonal|subseasonal}_country_{country_iso}_deterministic 
  * {seasonal|subseasonal}_country_{country_iso}_dominant 

**example:** subseasonal_country_et_probabilistic_above, seasonal_country_gt_probabilistic_normal, seasonal_country_et_probabilistic_below

-------------------------------------------------------------------

Agroclimatic data
==================

agroclimate_indices_{country_iso}
  * **description:** agroclimate indices for a country
  * **data type:** raster files (.tif) image mosaic
  * **keywords relevant to layer search:** coffee, dry_bean, maize, soybean, dry_spells, heat_waves, spei, etc.
layer name structure: 
  * {crop}_{index}

**example:** coffe_max_heat_wave_duration, dry_bean_number_dry_days

-------------------------------------------------------------------

Climate indices
===============

climate_indices_{country_iso}
  * **description:** climate indices for a contry 
  * **data type:** raster files (.tif) image mosaic
  * **keywords relevant to layer search:** total_rainfall, r1_mm, r10_mm, r1mm_periods, t_30, t30_periods, etc.
layer name structure: 
  * {indicator_id}

**example:** freq_rh80_t_20_25, t30_periods, total_rainfall

-------------------------------------------------------------------

Administrative
===============

administrative
  * **description:** administrative levels for country
  * **data type:** shapefiles (.shp)
  * **keywords relevant to layer search:** ao, et, adm1, adm2, adm3, adm4.
layer name structure: 
  * {country_iso}_adm1/adm2/adm3/adm4
shapefiles fields:
  * **{country_iso}_adm1**: *fid*, name_adm1, id_adm1
  * **{country_iso}_adm2**: *fid*, id_adm1, name_adm1, id_adm2, name_adm2

**remark:** *fid* is another field, but Geoserver automatically adds it when uploading the shapefile. Therefore, the shapefile must be **without** that field when uploading.
