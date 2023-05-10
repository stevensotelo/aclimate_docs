Admin collections
#################


ad_source
=========

This collection contains the different system sources used to identify the historical production data, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - name
    - This string corresponds to the name of the source.
    - String
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object



.. image:: /_static/img/03-database-admin/ad_source_model.*
    :alt: Model of the table ad_source
    :class: device-screen-vertical side-by-side



ad_user_permission
==================

This collection contains the records of the permissions of each one of the users to the different countries, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - user
    - This parameter corresponds to the user to which the permissions are linked.
    - String
  * - countries
    - Arrangement of countries to which the user has access to their respective data.
    - Array
  * - track
    - This object contains the registration data, if it is active within the system, date of registration in the system and date of updates.
    - Object


.. image:: /_static/img/03-database-admin/ad_user_permission_model.*
    :alt: Model of the table ad_user_permission
    :class: device-screen-vertical side-by-side



Users
=====

This collection contains the users who have access to the system, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - UserName
    - This parameter contains the user name with which the user accesses.
    - String
  * - NormalizedUserName
    - This parameter contains the normalized user name with which the user accesses.
    - String
  * - Email
    - This parameter contains the email with which the user accesses.
    - String
  * - NormalizedEmail
    - This parameter contains the normalized email with which the user accesses.
    - String
  * - EmailConfirmed
    - This parameter shows if the user has completed the email confirmation process.
    - Bool
  * - PasswordHash
    - This parameter contains the user's password in Hash format to protect the user's data.
    - String
  * - Roles
    - This parameter contains each of the Ids of the roles that the user has.
    - Array


Roles
=====

This collection contains each of the system roles, This collection contains the following parameters:

.. list-table:: Data base collection
  :widths: 25 25 25
  :header-rows: 1

  * - Parameter
    - Definition
    - Type
  
  * - _id
    - Unique identifier
    - ObjectId
  * - Name
    - This parameter contains the name of the Role.
    - String
  * - NormalizedName
    - This parameter contains the normalized name of the Role.
    - Array
  * - ConcurrencyStamp
    - A stamp that is used to identify the current version of the data. If you change it.
    - String



