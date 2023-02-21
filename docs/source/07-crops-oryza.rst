Oryza
=====

Oryza is a model that simulates the growth and development of rice. Its inputs are the climatic scenarios of the resampling process and the configuration files of each scenario to be simulated. The latter are the ones that contain information about the soil, the rice cultivar and the geographical location.
 
A configuration is a set of files (soil, cultivar, geographic information) linked to a set of climatic scenarios (station/location). For each configuration, a number n of days is simulated. In the case of rice for Colombia it is 45 days with a frequency of one. That is, 45 simulations will be made for a configuration.
 
The process begins by loading the entries. That is, the climatic scenarios and the geographical, soil and rice cultivar information. The simulation days and the frequency (every how many days the simulation will be done) are defined. The climatic scenarios are transformed so that the model understands them and copies them to the execution route (one for each day to be simulated). The configuration files of the scenario to be simulated are also copied to this path. Once all the files are ready, each day's simulation is run. This is done for each configuration.
 
Finally, the simulation data for each simulated day is extracted and written to a csv file as crop simulation statistics based on planting dates. So there will be a csv file for each configuration.

The following diagram describes the process mentioned above:

.. image:: /_static/img/07/07_oryza.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side