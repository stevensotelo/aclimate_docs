Database
========

This section contains all the collections found in the AClimate database, it is a non-relational database so the MongoDB manager is used.

The collections are divided into different categories:

* **Fs:** Collections related to the forecast process, forecast data, scenarios, etc. are stored.

* **Cp:** Collections related to the cultivation model process, contain data on soils, crops, cultivars, recommendations, etc.

* **Lc:** Collections related to localities, contains data from countries, states, municipalities, etc.

* **Hs:** Collections related to historical climatic data, climatology, daily monthly data, etc.

* **ad:** Collections related to system administration, contain user data, roles, etc.

* **log:** Collections with system event log data, errors etc.


.. toctree::
  :hidden:
  :maxdepth: 1

  03-database-admin
  03-database-enums
  03-database-forecast
  03-database-helper
  03-database-historical
  03-database-log