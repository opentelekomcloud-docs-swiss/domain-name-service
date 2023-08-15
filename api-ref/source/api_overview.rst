:original_name: en-us_topic_0132421999.html

.. _en-us_topic_0132421999:

API Overview
============

The DNS service provides RESTful APIs.

By calling these APIs, you can use all DNS functions, including creating, querying, modifying, and deleting private zones, and record sets.

:ref:`Table 1 <en-us_topic_0132421999__table138131522381>` provides an overview of the DNS APIs.

.. _en-us_topic_0132421999__table138131522381:

.. table:: **Table 1** API overview

   +-------------------------+---------------------------------------------------------------------+
   | Category                | Description                                                         |
   +=========================+=====================================================================+
   | Version Management      | Query version information of all DNS APIs or a specified API.       |
   +-------------------------+---------------------------------------------------------------------+
   | Private Zone Management | Create, delete, modify, and query private zones.                    |
   +-------------------------+---------------------------------------------------------------------+
   | Record Set Management   | Create, delete, modify, and query record sets in private zones.     |
   +-------------------------+---------------------------------------------------------------------+
   | Tag Management          | Create, delete, modify, and query tags for specified DNS resources. |
   +-------------------------+---------------------------------------------------------------------+

Version Management
------------------

Query DNS API versions.

.. table:: **Table 2** Version management APIs

   +-----------------------------------------------------+---------------------------------------------+
   | API                                                 | Description                                 |
   +=====================================================+=============================================+
   | :ref:`Listing All DNS API Versions <dns_api_61001>` | Query the versions of all DNS APIs.         |
   +-----------------------------------------------------+---------------------------------------------+
   | :ref:`Querying the DNS API Version <dns_api_61002>` | Queries the version of a specified DNS API. |
   +-----------------------------------------------------+---------------------------------------------+

Private Zone Management
-----------------------

Create, query, delete, and modify private zones.

.. table:: **Table 3** Private zone management APIs

   +-----------------------------------------------------------------+-----------------------------------------+
   | API                                                             | Description                             |
   +=================================================================+=========================================+
   | :ref:`Creating a Private Zone <dns_api_63002>`                  | Query a private zone.                   |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Associating a Private Zone with a VPC <dns_api_63003>`    | Associate a private zone with a VPC.    |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Disassociating a VPC from a Private Zone <dns_api_63004>` | Disassociate a VPC from a private zone. |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Querying a Private Zone <dns_api_63005>`                  | Query a private zone.                   |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Querying Private Zones <dns_api_63006>`                   | Query private zones.                    |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Querying Name Servers in a Private Zone <dns_api_63007>`  | Query name servers in a private zone.   |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Deleting a Private Zone <dns_api_63008>`                  | Delete a private zone.                  |
   +-----------------------------------------------------------------+-----------------------------------------+
   | :ref:`Modifying a Private Zone <dns_api_63009>`                 | Modify a private zone.                  |
   +-----------------------------------------------------------------+-----------------------------------------+

Record Set Management
---------------------

Create, query, delete, and modify record sets.

.. table:: **Table 4** Record set management APIs

   +-------------------------------------------------------+----------------------------------------+
   | API                                                   | Description                            |
   +=======================================================+========================================+
   | :ref:`Creating a Record Set <dns_api_64001>`          | Create a record set.                   |
   +-------------------------------------------------------+----------------------------------------+
   | :ref:`Querying a Record Set <dns_api_64002>`          | Query a record set.                    |
   +-------------------------------------------------------+----------------------------------------+
   | :ref:`Querying All Record Sets <dns_api_64003>`       | Query record sets.                     |
   +-------------------------------------------------------+----------------------------------------+
   | :ref:`Querying Record Sets in a Zone <dns_api_64004>` | Query record sets in a specified zone. |
   +-------------------------------------------------------+----------------------------------------+
   | :ref:`Deleting a Record Set <dns_api_64005>`          | Delete a record set.                   |
   +-------------------------------------------------------+----------------------------------------+
   | :ref:`Modifying a Record Set <dns_api_64006>`         | Modify a record set.                   |
   +-------------------------------------------------------+----------------------------------------+

Tag Management
--------------

Add, delete, and query resource tags.

.. table:: **Table 5** Tag management APIs

   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | API                                                                | Description                                                                            |
   +====================================================================+========================================================================================+
   | :ref:`Adding Resource Tags <dns_api_67001>`                        | Add tags to a specified resource. You can add a maximum of 10 tags to a resource.      |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | :ref:`Deleting a Resource Tag <dns_api_67002>`                     | Delete a resource tag.                                                                 |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | :ref:`Adding or Deleting Resource Tags in Batches <dns_api_67003>` | Add or delete tags for a specified resource in batches.                                |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | :ref:`Querying Tags of a Resource <dns_api_67004>`                 | Query tags of a specified resource.                                                    |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | :ref:`Querying Tags of a Specified Resource Type <dns_api_67005>`  | Query all tags of a resource type.                                                     |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
   | :ref:`Querying Resources by Tag <dns_api_67006>`                   | Query DNS resources by tag. Resources are sorted by creation time in descending order. |
   +--------------------------------------------------------------------+----------------------------------------------------------------------------------------+
