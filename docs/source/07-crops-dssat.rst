DSSAT
=====

The Decision Support System for Agrotechnology Transfer (DSSAT) is a software application program that comprises dynamic crop growth simulation models for more than 42 crops. In Aclimate, DSSAT is used to simulate corn and wheat crops. Like the Oryza component, its inputs are the climatic scenarios of the resampling process and the configuration files of each scenario to be simulated.
 
A configuration is a set of files (soil, cultivar, geographic information) linked to a set of climatic scenarios (station/location). For each configuration, a number n of days is simulated. In the case of wheat and maize for Ethiopia, 25 days are simulated at a frequency of 3. That is, 9 days in total are simulated per configuration.
 
The process begins by loading the identifiers of the station/location, cultivar, soil and the frequency of the simulations. It defines the input directories of the station/location weather settings and scenarios, as well as the output directories. Load the coordinates of the location/station and translate the climate scenarios into the format that the DSSAT models understand. Proceed to copy the configuration files with the climate scenarios and run the simulations. Once the simulations for all days are complete, the final simulation files are used to calculate the risk of water stress and land preparation days. The latter are indicators that have recently been added to the DSSAT crops module.
 
Finally, the simulation data of each simulated day is extracted, the indicators calculated and written to a csv file as crop simulation statistics based on planting dates. So there will be a csv file for each configuration.

The following diagram describes the process mentioned above:

.. image:: /_static/img/07/07_dssat.*
  :alt: Resampling process activity diagram
  :class: device-screen-vertical side-by-side