Stores
##########

A store connects to a data source that contains raster or vector data. A data source can be a file or group of files, a table in a database, a single raster file, or a directory. The stores are linked to a workspace.

To upload a layer to the Geoserver you must do the following:

1. Specify layer name
=====================

This value acts like an internal identifier and will not be visible publicly 

* use underscores and lower case letters only 
* e.g. total_rainfall 


.. image:: /_static/img/09-geoserver/geoserver-layer-creation.*
  :alt: GeoServer layer creation
  :class: device-screen-vertical side-by-side

2. Add title 
=====================

Enable i18n for Title and add languages accordingly. Set a descriptive title for each language that the user will understand

- en
- es
- pt (if necessary)
- e.g. Total rainfall in mm 


.. image:: /_static/img/09-geoserver/geoserver-layer-creation-i18n.*
  :alt: GeoServer layer enable i18n
  :class: device-screen-vertical side-by-side

3. Add description
=====================

Enable i18n for abstract and fill in for each language an easy to understand description for the layer. Be specific what the user will see:

- e.g. This layer shows the total rainfall in millimeters in Perú for the selected time period. The darker the color, the more rainfall is present


.. image:: /_static/img/09-geoserver/geoserver-layer-creation-descript.*
  :alt: GeoServer layer description
  :class: device-screen-vertical side-by-side

4. Specify keywords
=====================

Add the following relevant keywords for the layer:

- crop (e.g. maize, coffee, etc)
- group (e.g. dry_spells, heat_waves, spei, etc)
- units (e.g. days, mm, etc)
- acronym
- period (e.g. [02-03,04-07,10-12])

If a layer does not have a certain keyword, add the id anyways with value =NA (not available). Add the keywords like this:

- crop=maize
- group=dry_spells
- units=days
- acronym=NDS
- period=[02-03,04-07,10-12] (use array of month values/monthly periods, if annual, set to NA)


.. image:: /_static/img/09-geoserver/geoserver-layer-creation-keywords.*
  :alt: GeoServer layer keywords
  :class: device-screen-vertical side-by-side

5. Add style
=====================
Go to styles and create/copy one for the layer. Adjust values and colors to represent the layer accordingly. This should enable the creation of an automatic legend.  

.. image:: /_static/img/09-geoserver/geoserver-layer-creation-styles.*
  :alt: GeoServer layer styles
  :class: device-screen-vertical side-by-side