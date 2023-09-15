Installation with Docker
##########################

This chapter guides you through the installation and initial setup of a self-hosted 
instance of all platform from Docker container. You can find the Dockerfiles into
the Github repository: `<https://github.com/CIAT-DAPA/usaid_forecast_docker>`_.
You should start cloning the repository from Github:


Run the image
===============

Before running the image check the latest version at: https://hub.docker.com/r/stevensotelo/acclimate_process/tags
In this case, the latest version is 2.2.


.. tip::
  When launching the docker run command, the following flags can be added:

  - GEO_USER - Geoserver user. Used to import files to the geoserver from the image
  - GEO_PWD - Geoserver password. Used to import files to the geoserver from the image
  - N_CORES - Number of cores. It is used for parallelization processes
  
To run the image you can do the following:

.. code-block:: console
  :linenos:

  # Pull the image
  docker pull stevensotelo/aclimate_process:2.2
  # Run the image
  docker run --name aclimate2.2 -it --rm -v D:/folder_example/workdir:/forecast/workdir stevensotelo/aclimate_process:2.2 /bin/bash


This image contains all resources needed to execute the agroclimate forecast using the methodology of aclimate platform. The models which are inside of this image are:

  * CPT - Climate Predictable Tool (15.5.10, 15.5.3, 17.6.1 versions)
  * PyCPT - Climate Predictable Tool
  * DSSAT - Model version 4.8.1.006


Build the image
===============

If you need to build the image, you must download the repository as follows:

.. code-block:: console
    :linenos:

    git clone https://github.com/CIAT-DAPA/usaid_forecast_docker


This repository has the following structure:

.. image:: /_static/img/04-installation/04-usaid_docker_folders.*
  :alt: usaid_forecast_docker folders
  :class: device-screen-vertical side-by-side

The folder of interest is forecast_process. Inside this folder, you can copy some script folder from the version folder to start editing a new version. You can review the dockerfiles for each version to see the differences between the image versions.

Once the dockerfile has been edited, you must go, through the console, to the scripts folder where your dockerfile is and build the image with the following command:

.. code-block:: console
  :linenos:

  # Build the image
  docker build -t stevensotelo/aclimate_process:version_example .

After ":" you must put the version that will have this new image.