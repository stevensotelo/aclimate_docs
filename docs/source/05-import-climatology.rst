Climatology
###########


Within the import module is the **Climatology**, which allows to import climatology by means of flat files.

This information is used for the visualization of climate information. These values allow establishing the historical average of each of the climate variables. The precipitation first tercile (**prec_ter_1**) and precipitation second tercile (**prec_ter_2**) variables define the precipitation normality interval.

.. note::
    
    This option is available for users who have the roles of ADMIN, CLIMATOLOGIST, IMPROVER.
    

What does this module allow you to do?
**************************************

The climatology module allows uploading flat files with information on historical monthly weather averages. Each file contain information from one or several weather stations at a time. The data must be specific to each station. The climate variables that can be imported are: precipitation (**prec**), maximum temperature (**t_max**), minimum temperature (**t_min**) and solar radiation (**sol_rad**), relative humidity (**rel_hum**), precipitation first tercile (**prec_ter_1**) and precipitation second tercile (**prec_ter_2**).

.. note::

    When importing, it must be specified whether the weather stations should be searched by name or by external ID.


.. image:: /_static/img/05-import-climatology/climatology_module.*
  :alt: Climatology module image
  :class: device-screen-vertical side-by-side


How to access to the climatology module?
****************************************

To access to the climatology module, you must go to the top menu and select the **Import** option and in the submenu that is displayed you must select **Climatology**.

.. image:: /_static/img/05-import-climatology/how_to_access.*
  :alt: Guide how to access to the module
  :class: device-screen-vertical side-by-side


Import Climatology
******************

#. To perform the import, a flat file must be prepared with the information for each weather station. This file must be in CSV format. Select the file from your device.

        .. image:: /_static/img/05-import-climatology/import.*
            :alt: Guide how to import historical climate
            :class: device-screen-vertical side-by-side


#. The type of search must be selected, you can choose between **external ID** or the **name** of the station.

        .. image:: /_static/img/05-import-climatology/import_1.*
            :alt: Guide how to import historical climate 1
            :class: device-screen-vertical side-by-side


#. Finally, click on the Import button.

.. list-table:: CSV columns
  :widths: 25 25
  :header-rows: 1

  * - Column
    - Meaning
  
  * - measure
    - name of the measure - string type
  * - month
    - month of the year - number type
  * - name of the point
    - It can be a id, string or extension id


.. note::

    The file must have the following format:

        - Line 1 should start with the headers measure and month, then the search parameter of the stations as chosen. Each station must be separated by a comma. The following example is parameterized by external codes:

            * **measure,month,21245040,26115040,13085010**

        - The following lines contain the information by measurement, month and the values for each station. Example:

            * **t_max,1,28.88639,31.21029,32.22629**
        
    The following is an example of what the file would look like in the excel viewer

        .. image:: /_static/img/05-import-climatology/import_example_1.*
          :alt: How looks the import csv file 1
          :class: device-screen-vertical side-by-side

    
    The following is an example of what the file would look like in text viewer

        .. image:: /_static/img/05-import-climatology/import_example_2.*
          :alt: How looks the import csv file 2
          :class: device-screen-vertical side-by-side

.. warning::

    Make sure that the values of the month columns are of numeric type and the data of each station are of double type.