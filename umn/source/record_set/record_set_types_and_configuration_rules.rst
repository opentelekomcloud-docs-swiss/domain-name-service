:original_name: dns_usermanual_0601.html

.. _dns_usermanual_0601:

Record Set Types and Configuration Rules
========================================

Type
----

:ref:`Table 1 <dns_usermanual_0601__table8568111315618>` describes the record set types.

.. _dns_usermanual_0601__table8568111315618:

.. table:: **Table 1** Record set types

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | Type                              | Description                                                                                                                                |
   +===================================+============================================================================================================================================+
   | A                                 | Maps domains to IPv4 addresses.                                                                                                            |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | CNAME                             | Maps one domain name to another or multiple domain names to one domain name.                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | MX                                | Maps domain names to email servers.                                                                                                        |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | AAAA                              | Maps domain names to IPv6 addresses.                                                                                                       |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | TXT                               | Specifies text records. It is usually used in the following scenarios:                                                                     |
   |                                   |                                                                                                                                            |
   |                                   | -  To record DKIM public keys to prevent email fraud.                                                                                      |
   |                                   | -  To record the identity of domain name owners to facilitate domain name retrieval.                                                       |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | SRV                               | Records servers providing specific services.                                                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | NS                                | Delegates subdomains to other name servers. This type of record set is created by default and cannot be added manually.                    |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | SOA                               | Specifies the master authoritative DNS server for a domain name. The SOA record set is created by the system and cannot be added manually. |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+
   | PTR                               | Maps IP addresses to domain names.                                                                                                         |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------+

Record Set Configuration
------------------------

:ref:`Table 2 <dns_usermanual_0601__table936244914119>` lists the value requirements for different types of record sets.

.. _dns_usermanual_0601__table936244914119:

.. table:: **Table 2** Requirements for record set values

   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | Record Set Type       | Value                                                                                                                                         | Example                                          |
   +=======================+===============================================================================================================================================+==================================================+
   | A                     | IPv4 addresses mapped to the domain name                                                                                                      | 192.168.12.2                                     |
   |                       |                                                                                                                                               |                                                  |
   |                       | You can enter a maximum of 50 record values, each on a separate line.                                                                         | 192.168.12.3                                     |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | CNAME                 | Domain name alias. You can enter only one domain name.                                                                                        | www.example.com                                  |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | MX                    | Email server address                                                                                                                          | 10 mailserver.example.com.                       |
   |                       |                                                                                                                                               |                                                  |
   |                       | You can enter a maximum of 50 record values, each on a separate line.                                                                         | 20 mailserver2.example.com.                      |
   |                       |                                                                                                                                               |                                                  |
   |                       | The format is **[priority][mail server host name]**.                                                                                          |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | Configuration rules:                                                                                                                          |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  **priority**: priority for an email server to receive emails. A smaller value indicates a higher priority.                                 |                                                  |
   |                       | -  **mail server host name**: domain name provided by the email service provider                                                              |                                                  |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | AAAA                  | IPv6 addresses mapped to the domain name                                                                                                      | ff03:0db8:85a3:0:0:8a2e:0370:7334                |
   |                       |                                                                                                                                               |                                                  |
   |                       | You can enter a maximum of 50 record values, each on a separate line.                                                                         |                                                  |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | TXT                   | Text content                                                                                                                                  | -  Single text record:                           |
   |                       |                                                                                                                                               |                                                  |
   |                       | Configuration rules:                                                                                                                          |    "aaa"                                         |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  Text record values must be enclosed in double quotation marks.                                                                             | -  Multiple text records:                        |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  One or more text record values are supported, each on a separate line.                                                                     |    "bbb"                                         |
   |                       |                                                                                                                                               |                                                  |
   |                       |    A maximum of 50 text record values can be entered.                                                                                         |    "ccc"                                         |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  A single text record value can contain multiple character strings, each of which is double quoted and separated from others using a space. | -  A text record that contains multiple strings: |
   |                       |                                                                                                                                               |                                                  |
   |                       |    One character string cannot exceed 255 characters.                                                                                         |    "ddd" "eee" "fff"                             |
   |                       |                                                                                                                                               |                                                  |
   |                       |    A value must not exceed 4096 characters.                                                                                                   |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  The value cannot be left blank.                                                                                                            |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  The text cannot contain a backslash (\\).                                                                                                  |                                                  |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | SRV                   | Server address                                                                                                                                | 2 1 2355 example_server.test.com                 |
   |                       |                                                                                                                                               |                                                  |
   |                       | You can enter a maximum of 50 record values, each on a separate line.                                                                         |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | The value format is **[priority] [weight] [port number] [server address]**.                                                                   |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | Configuration rules:                                                                                                                          |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  The priority, weight, and port number range from 0 to 65535.                                                                               |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  A smaller priority value indicates a higher priority.                                                                                      |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  A larger weight value indicates a larger weight.                                                                                           |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | -  The server address is the domain name of the target server.                                                                                |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       |    Ensure that the domain name can be resolved.                                                                                               |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       | .. note::                                                                                                                                     |                                                  |
   |                       |                                                                                                                                               |                                                  |
   |                       |    The system checks the priority values first. If the priority values are the same, the system will check the weight values.                 |                                                  |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
   | PTR                   | Private domain name mapped to the private IP address. You can enter only one domain name.                                                     | www.example.com.                                 |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------+
