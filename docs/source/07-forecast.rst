Forecast process
================

General process

Directories are first created using R. This refers to the entire series of folders that the script needs to read, store, and write files.

Then the configurations must be extracted from the database. This is explained in :ref:`Importing data`. These configurations contain files necessary for the forecasting process, such as: monthly historical data, daily historical data and crop configurations.

Once the configurations have been extracted from the database, we can start with the generation of the seasonal forecast. This process uses monthly data and sea level temperature data downloaded from online databases. Use the Climate Predictability Tool (CPT) model for predictions. As a result, the probability of precipitation for six months is obtained.

Having the probability of precipitation for six months and the daily historical data, the process of generating climate scenarios can be started. This process performs a re-sampling and results in 100 climate scenarios.

With the climatic scenarios and the configuration files per crop, the crop simulation starts. This process uses the DSSAT model for corn and wheat; and Oryza 3000 for rice. It outputs crop simulation statistics based on planting dates.

Finally having the probability of precipitation for six months, the climatic scenarios and simulation statistics of crops based on sowing dates, it is possible to proceed with the import of the data in the datastorage. This being the final step of the forecasting process

The following diagram explains the process described above:

.. image:: /_static/img/07-forecast/07_forecast.*
  :alt: Forecast process activity diagram
  :class: device-screen-vertical side-by-side

