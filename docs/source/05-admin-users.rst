Users
#####

Within the administration module is the **User administration**, which allows the creation of accounts which will have access to the system.

What does this module allow you to do?
**************************************

The User module allow you to add, edit and list available users in the administration web portal. 

.. image:: /_static/img/05-admin-users/user_module.*
  :alt: User module image
  :class: device-screen-vertical side-by-side

.. note::

    Users cannot be deleted from the database, if you want to disable access to the system for a user, this must be disabled in the database.


How to access to the user administration module?
************************************************

To access the user administration module, you must go to the top menu and select the **Administration** option and in the submenu that is displayed you must select **Users**.

.. image:: /_static/img/05-admin-users/how_to_access.*
  :alt: Guide how to access to the module
  :class: device-screen-vertical side-by-side

Functionalities
***************


Create users
============

#. To create users you must select below the title Users, the option **New**.

            .. image:: /_static/img/05-admin-users/create_user_1.*
                :alt: Guide how to create user 1
                :class: device-screen-vertical side-by-side

#. You must complete all the fields

            .. image:: /_static/img/05-admin-users/create_user_2.*
                :alt: Guide how to create user 2
                :class: device-screen-vertical side-by-side

#. To finish you must press the **Register** button

Required fields
===============

.. list-table:: Required fields
  :widths: 25 25
  :header-rows: 1

  * - Field
    - Description
  
  * - **Email**
    - is an active email account, with the following pattern example@example.example
  * - **Roles**
    - define the user's profile and to which sites they have access.
  * - **Password**
    - is the user's key to enter the platform, password must contain at least 8 characters and maximun 100
  * - **Confirmar password**
    - this field helps to verify that you typed the password correctly, it must be exactly the same as the **Password** field (It is case sensitive)


.. note::

  **Roles**
    
    The Roles define the set of actions that can or cannot be performed in the application. Users need to have one or more roles associated to be able to access the different modules. The Roles are predefined by the application and there is no option to edit them. 
    
    The Roles are those available in the application:

        - **ADMIN:** Allows access to all modules of the application.
        - **CLIMATOLOGIST:** Allows access to the geographic modules and the configuration of climate forecasts.
        - **IMPROVER:** Allows access to the crop modules and the configuration of agro-climatic forecasts.
        - **TECH:** Allows access to user administration.

Edit users
==========

#. To edit users you must select in the last column, the option **Edit**.

          .. image:: /_static/img/05-admin-users/edit_user_1.*
            :alt: Guide how to edit user 1
            :class: device-screen-vertical side-by-side

#. A new view will be displayed, where you can select the countries which this user can view in the modules.

          .. image:: /_static/img/05-admin-users/edit_user_2.*
            :alt: Guide how to edit user 2
            :class: device-screen-vertical side-by-side

#. To finish you must press the **Edit** button