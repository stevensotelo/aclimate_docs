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
            **North Western Tigray,5eb75aadeadbca178471af17,"Very low:0-1525,Low:1526-1852,High:1853-2268,Very high:2269-3004"**


    The following is an example of what the file would look like in the excel viewer

        .. image:: /_static/img/06-import-crop-setups/import_ranges_example_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/06-import-crop-setups/import_ranges_example_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side


.. _Crop configurations:

Crop configurations
===================

The Crop configuration is the option of the crop module that allows the configuration of crops for the generation of agro-climatic forecasts. Before making a configuration for any crop, it is necessary to have previously registered the climatic season, the cultivar and the soil.


#. To start the import you must create a folder with the folders containing the files with each configuration you want to import.

        .. image:: /_static/img/06-import-crop-setups/import_crop_1.*
            :alt: Guide how to import Crop configuration 1
            :class: device-screen-vertical side-by-side

    Example of files required for DSSAT configuration
        
        .. image:: /_static/img/06-import-crop-setups/import_crop_2.*
            :alt: Guide how to import Crop configuration 2
            :class: device-screen-vertical side-by-side

    .. note::

        The folder containing the configuration files must have the following format in its name\: **weather station id _ cultivar id _ soil id _ days**. 
        
        Example: **5e91e1c214daf81260eb_60a16e2826e98d13b8db_6334a6d230243c12cc1f_3**

        The **Days** is used to represent the date interval in which the agro-climatic forecast can be made between sowing dates. If you want to see the variation that can occur day by day in each of the sowing dates, the value that should go there is 1; but if, on the contrary, what you want is to observe the variation that occurs weekly, the value that should go there is 7.


#. To import daily data you must access the path where ForecastApp is located through the console, either Linux or Windows.

        .. image:: /_static/img/06-import-crop-setups/import_2.*
            :alt: Guide how to import ranges configuration 2
            :class: device-screen-vertical side-by-side

    .. note::

        If you are using Windows it is recommended to use CMD.

#. To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

#. To execute the import of the ranges configuration you must use the following command **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -in -cc -p "path to the folder with the folders containing the files to be imported" -wd value -stm value -edm value -sd value**.

        .. image:: /_static/img/06-import-crop-setups/import_crop_3.*
            :alt: Guide how to import ranges configuration 3
            :class: device-screen-vertical side-by-side

    .. note::

        The command consists of the following parts:

            * **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** = This is the first mandatory part for all ForecastApp commands, it must be complemented with the command you want to perform.
            * **-in** = As this is an import process, the -in parameter must be used to indicate that a data import will be performed.
            * **-cc** = This parameter indicates that an import process of range configuration will be performed, it is mandatory if you want to perform this process.
            * **-p "ranges configuration file path"** = The -p parameter indicates the path where the file to be imported are located, this parameter is followed by the path where this file is located, example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\data.csv"**
                
                - In case you use a Linux operating system the path must be separated by **/** and in Windows you must use **\\**.
                - Linux example: **-p "/Users/Downloads/Daily-20221214T155614Z-001/Daily/Csv/Import/"**
                - Windows example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\"**

            * **-wd value** 
            * **-stm value** 
            * **-edm value**
            * **-sd value**

#. Once the command is prepared with all the parameters, copy the command in the console and press Enter, the process will perform the import of all data and once finished it will display the message **Import process has finished**.



Oryza configuration files
=========================

For the configuration of the Oryza files it is necessary to have 4 files that configure the run for the region, these files are:

    - coordinates.csv (File with coordinates for the region)
    - .crp (Crop data file for rice growth model)
    - .sol (Soil information file)
    - \*.exp (Experimental data file)


.. note::

    Any error in each of these files will result in a failed run, i.e. the agro-climatic forecast for that region will not be generated.


The file "coordinates.csv" (it should always be saved with this name) should be constructed as follows (comma separated file):

.. image:: /_static/img/06-import-crop-setups/oryza_example.*
                :alt: Oryza example 1
                :class: device-screen-vertical side-by-side

.. note::

    - lat = latitud
    - long = longitud
    - elev = elevación


    Decimal separators in this case are given by **'.'** (period).


    The **"*.crp"** file should contain the crop growth parameters once calibrated (remember that this file is the process of the researcher's hard work). By recommendation the file name can be the name of the variety (e.g. F2000.crp).

    The file **"*.sol"** soil data, for the soil water balance model. The name to pay tribute to the textural characteristic of the soil (e.g., loam_loam_clay.sol).

    Finally, the experimental file **"*.exp"** which contains all the crop management. Since forecast runs are made, irrigation options should not be included. The file name can refer to the zone or region where the run is being configured (e.g. LOCO.exp). It should be noted that the run configuration should be done in experimental mode and not evaluation as is conventionally done for calibration, i.e., LOCO.exp:


            .. image:: /_static/img/06-import-crop-setups/oryza_example_2.*
                :alt: Oryza example 2
                :class: device-screen-vertical side-by-side

    Example of the required files.

            .. image:: /_static/img/06-import-crop-setups/oryza_example_3.*
                :alt: Oryza example 2
                :class: device-screen-vertical side-by-side

    Without the files shown above it is impossible to perform an agroclimatic forecast run. The climatic information does not need to be added in this step since the module automatically takes the climatic forecast loaded in the previous module.


DSSAT configuration files
=========================


The DSSAT configuration files must respect certain patterns both the name of the files and the configuration within them. The following is a description of the files needed to configure a run for a region. For this case it is necessary to have the following 5 files:


    - MZCER048.CUL
    - MZCER048.ECO
    - MZCER048.SPE
    - SOIL.SOL
    - planting_details.csv


The following is an example of each of the files, primarily as they should be configured for the correct specification of the model run. Any error in each of these files will result in a failed run, i.e. the agroclimatic forecast for that region will not be generated.

The file that defines the cultivar parameters, it is necessary that it is always saved as "MZCER048.CUL" and the name inside the file is a generic name given as "CROP00", otherwise the platform will not generate the agroclimatic forecast. That is to say:

.. image:: /_static/img/06-import-crop-setups/dssat_example_1.*
                :alt: DSSAT example 1
                :class: device-screen-vertical side-by-side

The name of the ecotype must match the file "MZCER048.ECO"

.. image:: /_static/img/06-import-crop-setups/dssat_example_2.*
                :alt: DSSAT example 2
                :class: device-screen-vertical side-by-side

On the left side of the graph is shown the .cul file and on the left side the .eco file, showing where the names must match for the correct specification of the crop model run. The .spe file should not be medicated (leave the standard default that comes with the DSSAT installation).

The .sol file, should always be named "SOIL.SOL" and within its configuration it should be created as:

.. image:: /_static/img/06-import-crop-setups/dssat_example_3.*
                :alt: DSSAT example 3
                :class: device-screen-vertical side-by-side


It is important that within the SOIL.SOL file it is accessed as "\*USAID00001" since it is a generic name created for the correct operation of the platform.

Finally, to configure the run for the region it is essential to have this information inside the file "planting_details.csv" a file separated by commas and decimals by '.' (period). Below is an example of the crop management for a particular region.


.. image:: /_static/img/06-import-crop-setups/dssat_example_4.*
                :alt: DSSAT example 4
                :class: device-screen-vertical side-by-side


.. note::

    The above parameters must be configured by the expert for the region, since any error will cause the agroclimatic forecast not to be generated.
