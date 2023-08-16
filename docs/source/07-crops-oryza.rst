Oryza
=====

Oryza is a model that simulates the growth and development of rice. Its inputs are the climatic scenarios of the resampling process and the configuration files of each scenario to be simulated. The latter are the ones that contain information about the soil, the rice cultivar and the geographical location. These configurations are imported (explained in :ref:`Importing data`).
 
A configuration is a set of files (soil, cultivar, geographic information) linked to a set of climatic scenarios (station/location). For each configuration, a number n of days is simulated. In the case of rice for Colombia it is 45 days with a frequency of one. That is, 45 simulations will be made for a configuration.
 
The process begins by loading the entries. That is, the climatic scenarios and the geographical, soil and rice cultivar information. The simulation days and the frequency (every how many days the simulation will be done) are defined. The climatic scenarios are transformed so that the model understands them and copies them to the execution route (one for each day to be simulated). The configuration files of the scenario to be simulated are also copied to this path. Once all the files are ready, each day's simulation is run. This is done for each configuration.

Finally, the simulation data for each simulated day is extracted and written to a csv file as crop simulation statistics based on planting dates. So there will be a csv file for each configuration.

The following diagram describes the process mentioned above:

.. image:: /_static/img/07-forecast/07_oryza.*
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

  * - yield_14
    - yield
  * - prec_acu
    - accumulated precipitation
  * - t_max_acu
    - accumulated maximum temperature
  * - t_min_acu
    - accumulated minimum temperature
  * - bio_acu
    - accumulated biomass
  * - d_har
    - harvest days

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

.. image:: /_static/img/07-forecast/07_oryza_csv_example.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side

Below is an example of what the CSV looks like in a plain text viewer:

.. image:: /_static/img/07-forecast/07_oryza_csv_example_2.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side