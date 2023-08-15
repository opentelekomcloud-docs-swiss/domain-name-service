:original_name: en-us_topic_0035467692.html

.. _en-us_topic_0035467692:

Record Set
==========

Overview
--------

A record set is a collection of resource records that belong to the same domain name. A record set defines DNS record types and values.

If you have created a zone on the DNS console, you can create record sets to expand the domain name or record its detailed information.

:ref:`Table 1 <en-us_topic_0035467692__table143828363174>` describes the record set types and their application scenarios.

.. _en-us_topic_0035467692__table143828363174:

.. table:: **Table 1** Record set usages

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | Type                              | Usage                                                                                                                                      |
   +===================================+============================================================================================================================================+
   | A                                 | Maps domains to IPv4 addresses.                                                                                                            |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | CNAME                             | Maps one domain name to another or multiple domain names to one domain name.                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | MX                                | Maps domain names to email servers.                                                                                                        |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | AAAA                              | Maps domain names to IPv6 addresses.                                                                                                       |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | TXT                               | Creates text records for domain names. TXT record sets are usually used in the following scenarios:                                        |
   |                                   |                                                                                                                                            |
   |                                   | -  To record DKIM public keys to prevent email fraud.                                                                                      |
   |                                   | -  To record the identity of domain name owners to facilitate domain name retrieval.                                                       |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | SRV                               | Records servers providing specific services.                                                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | NS                                | Delegates subdomains to other name servers.                                                                                                |
   |                                   |                                                                                                                                            |
   |                                   | This type of record set is created by default and cannot be added manually.                                                                |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | SOA                               | Specifies the master authoritative DNS server for a domain name. The SOA record set is created by the system and cannot be added manually. |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | PTR                               | Maps IP addresses to domain names.                                                                                                         |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+

Usage
-----

Record sets are used in following scenarios:

-  Private domain name resolution

   On a private network, A and AAAA record sets translate private domain names into private IP addresses.


   .. figure:: /_static/images/en-us_image_0201578061.png
      :alt: **Figure 1** Private domain name resolution

      **Figure 1** Private domain name resolution

-  Reverse resolution on a private network

   PTR records translate private IP addresses into private domain names.


   .. figure:: /_static/images/en-us_image_0000001194911334.png
      :alt: **Figure 2** Reverse resolution on a private network

      **Figure 2** Reverse resolution on a private network

Helpful Links
-------------

For details, see :ref:`Overview <dns_usermanual_0035>`.
