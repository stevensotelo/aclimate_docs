Historical climate
##################

The Forecast app allows the import of monthly and daily data, these processes can also be performed through **WebAdmin**, but it is recommended to use **Forecast app** for imports containing a lot of data or many weather stations, as it allows to perform the processes much faster and with a lower consumption of resources.


.. _Import Daily Data:

Importing daily data
====================

Daily historical data files are required for the resampling process during the generation of the climate forecast.


#. To start the import you must create a folder with the files containing the daily data of each weather station you want to import.

        .. image:: /_static/img/06-import-historical-climate/import_daily_data_1.*
            :alt: Guide how to import daily data 1
            :class: device-screen-vertical side-by-side


    .. note::

        The name of each file should have either the Id of the weather station or the external Id, followed by **_daily** and the format, which must be csv (comma separated flat file).

            * **(Id or extId)_daily.csv**

        All files to be imported must have the same type, external Id or Id, it cannot vary between files of the same import.

#. To import daily data you must access the path where ForecastApp is located through the console, either Linux or Windows.

        .. image:: /_static/img/06-import-historical-climate/import_daily_data_2.*
            :alt: Guide how to import daily data 2
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        If you are using Windows it is recommended to use CMD.

#. To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

#. To execute the import of the daily data you must use the following command **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -in -fcfg -p "daily data path" -tyd value**.

        .. image:: /_static/img/06-import-historical-climate/import_daily_data_3.*
            :alt: Guide how to import daily data stations 3
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        The command consists of the following parts:

            * **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** = This is the first mandatory part for all ForecastApp commands, it must be complemented with the command you want to perform.
            * **-in** = As this is an import process, the -in parameter must be used to indicate that a data import will be performed.
            * **-fcfg** = This parameter indicates that a daily data import process will be performed, it is mandatory if you want to perform this process.
            * **-p "daily data path"** = The -p parameter indicates the path where the files to be imported are located, this parameter is followed by the path where these files are located, example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\"**
                
                - In case you use a Linux operating system the path must be separated by **/** and in Windows you must use **\\**.
                - Linux example: **-p "/Users/Downloads/Daily-20221214T155614Z-001/Daily/Csv/Import/"**
                - Windows example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\"**

            * **-tyd value** = This parameter tells the system whether to use the file names as external ID or weather station Id, this parameter must be followed by the number representing the type of file name to be read. example: **-tyd 1**.

                - **1** for weather station Id.
                - **2** for external Id.

#. Once the command is prepared with all the parameters, copy the command in the console and press Enter, the process will perform the import of all the files and once finished it will display the message **Import process has finished**.

        .. image:: /_static/img/06-import-historical-climate/import_daily_data_4.*
            :alt: Guide how to import daily data stations 4
            :class: device-screen-vertical side-by-side

    .. note::

        The process will create a folder called **tmp** inside the path used in the command, in this folder will be moved the files that were successfully imported, in case the process finishes and some file has not been moved to the **tmp** folder is because some error occurred while importing that file.


.. list-table:: CSV columns
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning
  
  * - day
    - day of the month - number type
  * - month
    - month of the year - number type
  * - year
    - year - number type
  * - t_max
    - maximum temperature °C - double type
  * - t_min
    - minimum temperature °C - double type
  * - prec
    - precipitation mm - double type
  * - sol_rad
    - solar radiation MJ/m²d - double type


.. note::

  The file must be in the following format in order to correctly generate the resampling:

    * This file should contain information on at least 30 years of historical data.

    * The data it contains are: **day**, **month**, **year**, maximum temperature (**t_max**), minimum temperature (**t_min**), precipitation (**prec**) and solar radiation (**sol_rad**).
    
    * The first row of the file is the header and should be in the following format:

        - **day,month,year,t_max,t_min,prec,sol_rad**

    * The following lines should contain the information for this station. Example:

        - **1,1,1980,30.67449154,22.67449154,0,16.37537505**
    
    * The units of measurement for each variable are: 
    
        - **t_max** = °C 
        - **t_min** = °C 
        - **prec** = mm
        - **sol_rad** = MJ/m²d


  The following is an example of what the file would look like in the excel viewer

      .. image:: /_static/img/06-import-historical-climate/import_example_1.*
        :alt: How looks the import csv file 1
        :class: device-screen-vertical side-by-side

  
  The following is an example of what the file would look like in text viewer

      .. image:: /_static/img/06-import-historical-climate/import_example_2.*
        :alt: How looks the import csv file 2
        :class: device-screen-vertical side-by-side
    

  The files imported into the system are stored within the administration website in the Data/Configurations folder, the name of the files consists of the date (format yyyyMMddHHmmss), an antenna name (-wsconf-), the weather station id, an antenna name (-) and ends with the name of the file itself that was uploaded.


.. warning::

    Make sure that the values of the year, month and day columns are of numeric type and the data of each measurement variable are of double type.

.. _Import Monthly Data:

Importing monthly data
======================

Monthly data is very important for the platform, this data is used for the process of climate prediction generation and information visualization. These data are used in the probabilistic prediction component


#. To start the import you must create a folder with the file containing the monthly data of each weather station you want to import.

        .. image:: /_static/img/06-import-historical-climate/import_monthly_data_1.*
            :alt: Guide how to import monthly data 1
            :class: device-screen-vertical side-by-side

    The name of each column should have either the name of the weather station or the external Id.


#. To import monthly data you must access the path where ForecastApp is located through the console, either Linux or Windows.

        .. image:: /_static/img/06-import-historical-climate/import_daily_data_2.*
            :alt: Guide how to import monthly data 2
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        If you are using Windows it is recommended to use CMD.

#. To execute any ForecastApp command you must use the following line of code **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** this will execute the file that will start the ForecastApp process, this command must be followed by the action you want to do.

#. To execute the import of the monthly data you must use the following command **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll -in -hs -s "measure" -type value -p "monthly data path"**.

        .. image:: /_static/img/06-import-historical-climate/import_monthly_data_3.*
            :alt: Guide how to import monthly data 3
            :height: 50
            :class: device-screen-vertical side-by-side

    .. note::

        The command consists of the following parts:

            * **dotnet CIAT.DAPA.USAID.Forecast.ForecastApp.dll** = This is the first mandatory part for all ForecastApp commands, it must be complemented with the command you want to perform.
            * **-in** = As this is an import process, the -in parameter must be used to indicate that a data import will be performed.
            * **-hs** = This parameter indicates that a monthly data import process will be performed, it is mandatory if you want to perform this process.
            * **-s "measure"** = The -s parameter indicates the measurement variable to be imported, this parameter is followed by the name of the variable to be imported. Example: **-s "sol_rad"**

                - **prec** = precipitation.
                - **sol_rad** = Solar radiation.
                - **t_max** = Maximum temperature.
                - **t_min** = Minimum temperature

            * **-p "monthly data path"** = The -p parameter indicates the path where the file to be imported are located, this parameter is followed by the path where this file is located, example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\data.csv"**
                
                - In case you use a Linux operating system the path must be separated by **/** and in Windows you must use **\\**.
                - Linux example: **-p "/Users/Downloads/Daily-20221214T155614Z-001/Daily/Csv/Import/data.csv"**
                - Windows example: **-p "C:\\Users\\Downloads\\Daily-20221214T155614Z-001\\Daily\\Csv\\Import\\data.csv"**

            * **-type value** = This parameter tells the system whether to use the column names of the file as external ID or name of the weather station, this parameter must be followed by the number representing the type of file name to be read. Example: **-type 1**.

                - **1** for external Id.
                - **2** for the name of the weather station.

#. Once the command is prepared with all the parameters, copy the command in the console and press Enter, the process will perform the import of all data and once finished it will display the message **Import process has finished**.

        .. image:: /_static/img/06-import-historical-climate/import_monthly_data_4.*
            :alt: Guide how to import daily data stations 4
            :class: device-screen-vertical side-by-side


.. list-table:: CSV columns
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning
  
  * - year
    - year - number type
  * - month
    - month of the year - number type
  * - name of the point
    - It can be a id, string or extension id

.. note::

    The file must have the following format:

        - Line 1 must start with the headers year and month, then the search parameter of the stations as chosen. Each station must be separated by comma. The following example is parameterized by external codes:

            * **year,month,26055070,26060020,26070110**

        - The following lines contain the information by year, month and the values for each station. Example:

            * **1981,1,75.1,38,10**
        
    The following is an example of what the file would look like in the excel viewer

        .. image:: /_static/img/06-import-historical-climate/import_example_m_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/06-import-historical-climate/import_example_m_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side

.. warning::

    Make sure that the values of the year and month columns are of numeric type and the data of each station are of double type.