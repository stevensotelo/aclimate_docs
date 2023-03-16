Historical climate
##################


Within the import module is the **Historical climate**, which allows to import historical climate by means of flat files.


Historical data is very important for the platform, this data is used for the process of climate prediction generation and information visualization. These data are used in the probabilistic prediction component.

.. note::
    
    This option is available for users who have the roles of ADMIN, CLIMATOLOGIST, IMPROVER.


What does this module allow you to do?
**************************************

The Historical climate module allows you to upload flat files with monthly weather history data. Each file contain information from one or several weather stations at a time. The data must be specific to each station. The climate variables that can be imported are: precipitation **prec**, maximum temperature **t_max**, minimum temperature **t_min** and solar radiation **sol_rad**.

.. note::

    Only one variable can be imported per file. 
     
    When importing, it must be specified whether the weather stations are to be searched by name or by external code.


.. image:: /_static/img/05-import-historical-climatic/historical_module.*
  :alt: Historical climate module image
  :class: device-screen-vertical side-by-side


How to access to the historical climate module?
***********************************************

To access to the historical climate module, you must go to the top menu and select the **Import** option and in the submenu that is displayed you must select **Historical climate**.

.. image:: /_static/img/05-import-historical-climatic/how_to_access.*
  :alt: Guide how to access to the module
  :class: device-screen-vertical side-by-side


Import historical climate
*************************

For more details on how to import historical climate and the format of the file to import, please click here :ref:`Import Monthly Data`

#. To perform the import, a flat file must be prepared with the information for each weather station. This file must be in CSV format. Select the file from your device.

        .. image:: /_static/img/05-import-historical-climatic/import.*
            :alt: Guide how to import historical climate
            :class: device-screen-vertical side-by-side


#. The type of search must be selected, you can choose between **external ID** or the **name** of the station.

        .. image:: /_static/img/05-import-historical-climatic/import_1.*
            :alt: Guide how to import historical climate 1
            :class: device-screen-vertical side-by-side


#. Then choose the climatic variable (**measurement**) to be imported. Then select the file to be imported.

        .. image:: /_static/img/05-import-historical-climatic/import_2.*
            :alt: Guide how to import historical climate 2
            :class: device-screen-vertical side-by-side


#. Finally, click on the Import button.

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

        .. image:: /_static/img/05-import-historical-climatic/import_example_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/05-import-historical-climatic/import_example_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side

.. warning::

    Make sure that the values of the year and month columns are of numeric type and the data of each station are of double type.