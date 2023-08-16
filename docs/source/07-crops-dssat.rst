DSSAT
=====

The Decision Support System for Agrotechnology Transfer (DSSAT) is a software application program that comprises dynamic crop growth simulation models for more than 42 crops. In Aclimate, DSSAT is used to simulate corn and wheat crops. Like the Oryza component, its inputs are the climatic scenarios of the resampling process and the configuration files of each scenario to be simulated. These configurations are imported (explained in :ref:`Importing data`).
 
A configuration is a set of files (soil, cultivar, geographic information) linked to a set of climatic scenarios (station/location). For each configuration, a number n of days is simulated. In the case of wheat and maize for Ethiopia, 25 days are simulated at a frequency of 3. That is, 9 days in total are simulated per configuration.
 
The process begins by loading the identifiers of the station/location, cultivar, soil and the frequency of the simulations. It defines the input directories of the station/location weather settings and scenarios, as well as the output directories. Load the coordinates of the location/station and translate the climate scenarios into the format that the DSSAT models understand. Proceed to copy the configuration files with the climate scenarios and run the simulations. Once the simulations for all days are complete, the final simulation files are used to calculate the risk of water stress and land preparation days. The latter are indicators that have recently been added to the DSSAT crops module.
 
Finally, the simulation data for each simulated day is extracted and written to a csv file as crop simulation statistics based on planting dates. So there will be a csv file for each configuration.

The following diagram describes the process mentioned above:

.. image:: /_static/img/07-forecast/07_dssat.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side


The csv file mentioned has the following columns:

.. list-table:: CSV columns
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning
  
  * - weather_station
    - station/location id
  * - soil
    - soil id
  * - cultivar
    - cultivar id
  * - start
    - simulation start date
  * - end
    - simulation end date

For the 'measure' column, the following values are available:

.. list-table:: Measure column
  :widths: 25 25
  :header-rows: 1

  * - Measure
    - Meaning

  * - yield_0
    - yield
  * - d_dry
    - dry days
  * - prec_acu
    - accumulated precipitation
  * - bio_acu
    - accumulated biomass
  * - t_max_acu
    - accumulated maximum temperature
  * - t_min_acu
    - accumulated minimum temperature
  * - st_ger_boo_w
    - water stress germination to booting
  * - st_boo_ant_w
    - water stress booting to anthesis
  * - st_beg_end_gf_w
    - water stress beginning to end of grain filling
  * - st_ger_boo_n
    - nitrogen stress germination to booting
  * - st_boo_ant_n
    - nitrogen stress booting to anthesis
  * - st_beg_end_gf_n
    - nitrogen stress beginning to end of grain filling
  * - land_pre_day
    - land preparation days

For each measure the next colums are calculated:

.. list-table:: CSV columns statistics
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning

  * - avg
    - average
  * - median
    - median
  * - min
    - minimum value
  * - max
    - maximum value
  * - quar_1
    - quartile 1
  * - quar_2
    - quartile 2
  * - quar_3
    - quartile 3
  * - conf_lower
    - lower confidence interval limit
  * - conf_upper
    - upper confidence interval limit
  * - sd
    - standard deviation
  * - perc_5
    - 5th percentile
  * - perc_95
    - 95th percentile
  * - coef_var
    - coefficient of variation

Below is an example of what the CSV looks like in Excel:

.. image:: /_static/img/07-forecast/07_dssat_csv_example.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side

Below is an example of what the CSV looks like in a plain text viewer:

.. image:: /_static/img/07-forecast/07_dssat_csv_example_2.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side