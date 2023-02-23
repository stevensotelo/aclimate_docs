Crop setups
###########

The Forecast app allows the import of crop configurations, ranges configuration (Yield ranges) and soil data.

* Soil data

.. _Ranges configuration:

Ranges configuration
====================

The production ranges allow managing the production levels of the different crops that have been historically presented in the climatic seasons. This serves to give the users a vision of the production thresholds that occur in the locality of the different crops. There can be several levels per crop per season, however it is recommended to have 5 levels for each crop.


#. To start the import you must create a folder with the file containing the ranges configuration of each weather station you want to import.

        .. image:: /_static/img/06-import-crop-setups/import_ranges_1.*
            :alt: Guide how to import ranges configuration 1
            :class: device-screen-vertical side-by-side

#. To import daily data you must access the path where ForecastApp is located through the console, either Linux or Windows.

        .. image:: /_static/img/06-import-crop-setups/import_2.*
            :alt: Guide how to import ranges configuration 2
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        If you are using Windows it is recommended to use CMD.

#. To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

#. To execute the import of the ranges configuration you must use the following command **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -in -wr -p "ranges configuration file path"**.

        .. image:: /_static/img/06-import-crop-setups/import_ranges_3.*
            :alt: Guide how to import ranges configuration 3
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        The command consists of the following parts:

            * **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** = This is the first mandatory part for all ForecastApp commands, it must be complemented with the command you want to perform.
            * **-in** = As this is an import process, the -in parameter must be used to indicate that a data import will be performed.
            * **-wr** = This parameter indicates that an import process of range configuration will be performed, it is mandatory if you want to perform this process.
            * **-p "ranges configuration file path"** = The -p parameter indicates the path where the file to be imported are located, this parameter is followed by the path where this file is located, example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\data.csv"**
                
                - In case you use a Linux operating system the path must be separated by **/** and in Windows you must use **\\**.
                - Linux example: **-p "/Users/Downloads/Daily-20221214T155614Z-001/Daily/Csv/Import/"**
                - Windows example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\"**

#. Once the command is prepared with all the parameters, copy the command in the console and press Enter, the process will perform the import of all data and once finished it will display the message **Import process has finished**.


.. note::

    The file must be in the following format in order to correctly import:

      * The data it contains are: **country_name**, **country_iso2**, **state_id**, **state_name**, **municipality_id**, **municipality_name**, **crop_id**, **ranges**.
      
      * The first row of the file is the header and should be in the following format:

            **country_name,country_iso2,state_id,**
            **state_name,municipality_id,municipality_name,crop_id,ranges**

            - **country_name** = Name of the country where the weather station is located.
            - **country_iso2** = Corresponds to the international ISO code that is assigned to each country. A list of ISO 2 codes for each country is available at http://www.nationsonline.org/oneworld/country_code_list.htm.
            - **state_id** = Id of the state to which the weather station belongs.
            - **state_name** = Name of the state to which the weather station belongs.
            - **municipality_id** = Id of the municipality to which the weather station belongs.
            - **municipality_name** = Name of the municipality to which the weather station belongs.
            - **crop_id** = Id of the crop to which the configurations will be associated.
            - **ranges** = Ranges which will be imported to each weather station. Each range is made up as follows **Label\:min_value-max_value**. Example: **Very low:0-1525** and you can be grouped to import more than one range for each station, separating each range by a **","**. **"Very low:0-1525,Low:1526-1852,High:1853-2268,Very high:2269-3004"**.

      * The following lines should contains the information to perform the importing of the ranges. Example:

            **Ethiopia,ET,5e91dfaf14daf81260ebba2d,Tigray,5e91dfcb14daf81260ebba31,**
            **North Western Tigray,5eb75aadeadbca178471af17,"Very low:0-1525,Low:1526-1852,High:1853-2268,Very high:2269-3004**


    The following is an example of what the file would look like in the excel viewer

        .. image:: /_static/img/06-import-crop-setups/import_ranges_example_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/06-import-crop-setups/import_ranges_example_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side


Crop configurations
===================