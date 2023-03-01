.. _Importing data:

Importing data
##############

This section describes how import data with Forecast App in batch mode

To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

To perform import processes the command must contain the following **-in** parameter to indicate to the system that an import process will be performed.

**dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -in + (import proccess)**

.. toctree::
  :hidden:
  :maxdepth: 1
  :caption: Import

  06-import-historical-climate
  06-import-crop-setups
  06-import-forecast