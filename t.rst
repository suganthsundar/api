SPARES API
==========

Location
--------
Location Details
~~~~~~~~~~~~~~~~

::

    GET /api/location/${location_id}

Sites Served by the Depot/Depots supported by the Site
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    GET /api/location/${location_id}/sites

Part Counts (grouped by Status and Vendor, Part Type)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    GET /api/location/${location_id}/part-counts

Permissions
-----------

Add Power User
~~~~~~~~~~~~~~

::

    POST /api/permissions/power-users/${location_id}
    { "email" : "<User Email Id>" }

Add Admin
~~~~~~~~~

::

    POST /api/permissions/admins/${location_id}
    { "email" : "<User Email Id>" }

Delete Power User
~~~~~~~~~~~~~~~~~

::

    DELETE /api/permissions/power-users/${location_id}
    { "email" : "<User Email Id>" }

Delete Admin
~~~~~~~~~~~~

::

    DELETE /api/permissions/admins/${location_id}
    { "email" : "<User Email Id>" }

Part
----

Details about Part
~~~~~~~~~~~~~~~~~~

::

    GET /api/part/${part_id}

Adding Part
~~~~~~~~~~~

::

    POST  /api/part/add

Confirming Part
~~~~~~~~~~~~~~~

::

    POST  /api/part/confirm/${part_id}

Amend Part
~~~~~~~~~~

::

    POST  /api/part/deny/${part_id}

Transfer Part
~~~~~~~~~~~~~

::

    POST  /api/part/${part_id}/transfer

Editing Part
~~~~~~~~~~~~

::

    PUT /api/part/${part_id}

Deleting Part
~~~~~~~~~~~~~

::

    DELETE  /api/part/${part_id}
