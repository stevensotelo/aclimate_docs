Historical climate
##################


State historical
================



#. To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

#. To execute the export of the state historical you must use the following command **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -out -s "measure" -p "path where the file is exported" -start value -end value -c "country_id"**.

        .. image:: /_static/img/06-export-historical-climate/export_state_1.*
            :alt: Guide how to export state historical 1
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        The command consists of the following parts:

            * **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** = This is the first mandatory part for all ForecastApp commands, it must be complemented with the command you want to perform.
            * **-out** = As this is an export process, the -out parameter must be used to indicate that a data export will be performed.
            * **-s** = Export the climate historical data of all states. Every state is exported in a file with its name. You should add the parameter "-start" and "-end".
            * **-p "path where the file is exported"** = The -p parameter indicates the path where the file to be exported, this parameter is followed by the path, example: **-p "C:\\Users\\Csv\\Export\\"**
                
                - In case you use a Linux operating system the path must be separated by **/** and in Windows you must use **\\**.
                - Linux example: **-p "/Users/Csv/Export/"**
                - Windows example: **-p "C:\\Users\\Csv\\Export\\"**

            * **-start value**  = This parameter indicates the start year to export data. It is integer value.
            * **-end value**  = This parameter indicates the end year to export data. It is integer value.
            * **-c value**  = Mandatory parameter. It is the ObjectId of Country to export data for only country indicated in the parameter.

#. Once the command is prepared with all the parameters, copy the command in the console and press Enter, the process will perform the export of all data and once finished it will display the message **Export process has finished**.

At the end of the export, the folder **estacionesMensuales** is generated, which will contain a folder for each state of the selected country, within the folder of each state there will be one file.

**stations.csv**

.. list-table:: CSV columns
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning
  
  * - **year**
    - Corresponds to the year of the data
  * - **month**
    - corresponds to the month of the data
  * - **weather station id**
    - It is the id of the weather station to which the data belongs

.. note::

    The file must be in the following format in order to correctly import:

      * The data it contains are: **year**, **month**, **weather station id**.
      
      * The first row of the file is the header and should be in the following format:

            **year,month,62a74f9bea81f11fe450cbc2,63868afd5371672adc12c1fc**

      * The following lines should contains the information to perform the importing of the ranges. Example:

            **1981,1,191.4,178.706862208**


    The following is an example of what the file would look like in the excel viewer

        .. image:: /_static/img/06-export-historical-climate/export_state_example_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/06-export-historical-climate/export_state_example_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side

