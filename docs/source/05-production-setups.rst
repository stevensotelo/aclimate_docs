Setups
######


Within the Production module is the **Setups**, The setup is the option of the crop module that allows the configuration of crops for the generation of agro-climatic forecasts. Before making a configuration for any crop, it is necessary to have previously registered the climatic season, the cultivar and the soil.

For more details on how to import Crop configurations and the format of the files to import, please click here :ref:`Crop configurations`

What does this module allow you to do?
**************************************

The Setups module allows you to create new setups, edit, view details and delete.

.. image:: /_static/img/05-production-setups/setup_module.*
  :alt: Setup module image
  :class: device-screen-vertical side-by-side


.. note::

    To delete data in this module it must be logical deletion. 
    (Logical deletions are those where the result is never actually deleted)


How to access to the setups module?
***********************************

To access to the setups module, you must go to the top menu and select the **Production** option and in the submenu that is displayed you must select **Setup**.

.. image:: /_static/img/05-production-setups/how_to_access.*
  :alt: Guide how to access to the module
  :class: device-screen-vertical side-by-side



Functionalities
***************


Create setups
=============

#. To create setups you must select below the title Setups, the option **New record**.

            .. image:: /_static/img/05-production-setups/create_setup_1.*
                :alt: Guide how to create setups 1
                :class: device-screen-vertical side-by-side

#. You must complete all the fields

            .. image:: /_static/img/05-production-setups/create_setup_2.*
                :alt: Guide how to create setups 2
                :class: device-screen-vertical side-by-side


#. To add configuration files you must click on **Add file**.

#. You must select the file saved on your device and name the file depending on the configuration file to be uploaded to the system.

      .. image:: /_static/img/05-production-setups/create_setup_3.*
        :alt: Guide how to create setups 3
        :class: device-screen-vertical side-by-side


#. To finish you must press the **Save** button


Required fields
===============

.. list-table:: Required fields
  :widths: 25 25
  :header-rows: 1

  * - Field
    - Description
  
  * - **Crop**
    - you must select the crop to which the setup will be associated.
  * - **Weather station**
    - you must select the weather station to which the setup will be associated.
  * - **Cultivar**
    - you must select the cultivar to which the setup will be associated.
  * - **Soil**
    - you must select the soil to which the setup will be associated.
  * - **Days**
    - is used to represent the date interval in which the agro-climatic forecast can be made between sowing dates. If you want to see the variation that can occur day by day in each of the sowing dates, the value that should go there is 1; but if, on the contrary, what you want is to observe the variation that occurs weekly, the value that should go there is 7.
  * - **Configurations files**
    - Files to upload


.. note::

    This option is available for users who have the roles of **ADMIN** and **IMPROVER**.


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

.. image:: /_static/img/05-production-setups/oryza_example.*
                :alt: Oryza example 1
                :class: device-screen-vertical side-by-side

.. list-table:: Abbreviations
  :widths: 25 25
  :header-rows: 1

  * - Abbreviation
    - Meaning
  
  * - lat
    - latitud
  * - long
    - longitud
  * - elev
    - elevation

.. note::


    Decimal separators in this case are given by **'.'** (period).


    The **"*.crp"** file should contain the crop growth parameters once calibrated (remember that this file is the process of the researcher's hard work). By recommendation the file name can be the name of the variety (e.g. F2000.crp).

    The file **"*.sol"** soil data, for the soil water balance model. The name to pay tribute to the textural characteristic of the soil (e.g., loam_loam_clay.sol).

    Finally, the experimental file **"*.exp"** which contains all the crop management. Since forecast runs are made, irrigation options should not be included. The file name can refer to the zone or region where the run is being configured (e.g. LOCO.exp). It should be noted that the run configuration should be done in experimental mode and not evaluation as is conventionally done for calibration, i.e., LOCO.exp:


            .. image:: /_static/img/05-production-setups/oryza_example_2.*
                :alt: Oryza example 2
                :class: device-screen-vertical side-by-side

    Example of the required files.

            .. image:: /_static/img/05-production-setups/oryza_example_3.*
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

.. image:: /_static/img/05-production-setups/dssat_example_1.*
                :alt: DSSAT example 1
                :class: device-screen-vertical side-by-side

The name of the ecotype must match the file "MZCER048.ECO"

.. image:: /_static/img/05-production-setups/dssat_example_2.*
                :alt: DSSAT example 2
                :class: device-screen-vertical side-by-side

On the left side of the graph is shown the .cul file and on the left side the .eco file, showing where the names must match for the correct specification of the crop model run. The .spe file should not be medicated (leave the standard default that comes with the DSSAT installation).

The .sol file, should always be named "SOIL.SOL" and within its configuration it should be created as:

.. image:: /_static/img/05-production-setups/dssat_example_3.*
                :alt: DSSAT example 3
                :class: device-screen-vertical side-by-side


It is important that within the SOIL.SOL file it is accessed as "\*USAID00001" since it is a generic name created for the correct operation of the platform.

Finally, to configure the run for the region it is essential to have this information inside the file "planting_details.csv" a file separated by commas and decimals by '.' (period). Below is an example of the crop management for a particular region.


.. image:: /_static/img/05-production-setups/dssat_example_4.*
                :alt: DSSAT example 4
                :class: device-screen-vertical side-by-side


.. note::

    The above parameters must be configured by the expert for the region, since any error will cause the agroclimatic forecast not to be generated.

Edit setups
===========

#. To edit setups you must select in the last column, the option **Edit**.

          .. image:: /_static/img/05-production-setups/edit_setup_1.*
            :alt: Guide how to edit setups 1
            :class: device-screen-vertical side-by-side

#. A new view will be displayed, where you can edit the setup fields.

          .. image:: /_static/img/05-production-setups/edit_setup_2.*
            :alt: Guide how to edit setups 2
            :class: device-screen-vertical side-by-side

#. If you want to delete a file, you can do it by means of the trash can icon, or you can add more files clicking on the **Add file** button.

          .. image:: /_static/img/05-production-setups/edit_setup_3.*
            :alt: Guide how to edit setups 3
            :class: device-screen-vertical side-by-side

#. To finish you must press the **Save** button.


Setup details
=============

#. To view setup details you must select in the last column, the option **Details**.

      .. image:: /_static/img/05-production-setups/details_setup_1.*
        :alt: Guide how to view setup details 1
        :class: device-screen-vertical side-by-side

#. A new view will appear, in which you can view the setup details.

      .. image:: /_static/img/05-production-setups/details_setup_2.*
        :alt: Guide how to view setup details 2
        :class: device-screen-vertical side-by-side


Delete setups
=============

#. To delete one setup you must select in the last column, the option **Delete**.

      .. image:: /_static/img/05-production-setups/delete_setup_1.*
        :alt: Guide how to delete setups 1
        :class: device-screen-vertical side-by-side

#. A new view will appear, in which you can delete the setup.

      .. image:: /_static/img/05-production-setups/delete_setup_2.*
        :alt: Guide how to delete setups 2
        :class: device-screen-vertical side-by-side

#. To finish you must press the **Delete** button



.. note::

    You can use the pager below to see all available setups.


              .. image:: /_static/img/05-production-setups/pager.*
                :alt: pager
                :class: device-screen-vertical side-by-side  