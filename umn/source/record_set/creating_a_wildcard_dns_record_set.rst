:original_name: dns_usermanual_0036.html

.. _dns_usermanual_0036:

Creating a Wildcard DNS Record Set
==================================

**Scenarios**
-------------

A wildcard record set with its name set to an asterisk (``*``) can map all subdomains of the domain name to the same value. During domain name resolution, fuzzy matching is used.

.. note::

   Exact matching has a higher priority than fuzzy matching.

Constraints
-----------

Wildcard DNS resolution does not support NS and SOA record sets.

**Procedure**
-------------

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. In the navigation pane, choose **Private Zones**.

   The zone list is displayed.

4. Click |image1| in the upper left corner and select the desired region and project.

5. Click the name of the zone to which you want to add a wildcard DNS record set.

6. Click **Add Record Set**.

7. Configure the parameters based on :ref:`Table 1 <dns_usermanual_0036__ta6b1707711b04a89b824b97109ef7db2>`.

   .. _dns_usermanual_0036__ta6b1707711b04a89b824b97109ef7db2:

   .. table:: **Table 1** Parameters for adding a wildcard DNS record set

      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | Parameter             | Description                                                                                                                                           | Example Value                                                                                            |
      +=======================+=======================================================================================================================================================+==========================================================================================================+
      | Name                  | Private domain name                                                                                                                                   | \*.abc                                                                                                   |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | Enter an asterisk (``*``) as the leftmost label of the domain name, for example, **\*.example.com**.                                                  |                                                                                                          |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | .. note::                                                                                                                                             |                                                                                                          |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       |    Only the leftmost asterisk is considered as a wildcard character. Other asterisks in the domain name are common text characters.                   |                                                                                                          |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | Type                  | Record set type                                                                                                                                       | A - Map domains to IPv4 addresses                                                                        |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | Wildcard DNS resolution does not support NS and SOA record sets.                                                                                      |                                                                                                          |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | TTL (s)               | Cache duration of the record set on a local DNS server, in seconds.                                                                                   | The default value is 300s, which is, 5 minutes.                                                          |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | The value ranges from **300** to **2147483647**, and the default is **300**.                                                                          |                                                                                                          |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | If your service address changes frequently, set TTL to a smaller value.                                                                               |                                                                                                          |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | Value                 | Record set value                                                                                                                                      | Take an A record set for example, **Value** is set to IPv4 addresses mapped to the domain name. Example: |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       |                                                                                                                                                       | 192.168.12.2                                                                                             |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       |                                                                                                                                                       | 192.168.12.3                                                                                             |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | Tag                   | (Optional) Identifier of the record set.                                                                                                              | example_key1                                                                                             |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | Each tag contains a key and a value. You can add a maximum of 10 tags to a record set. This parameter is displayed when you expand **More Settings**. | example_value1                                                                                           |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | For details about tag key and value requirements, see :ref:`Table 2 <dns_usermanual_0036__table865604093219>`.                                        |                                                                                                          |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+
      | Description           | (Optional) Supplementary information about the record set.                                                                                            | This is a wildcard DNS record set.                                                                       |
      |                       |                                                                                                                                                       |                                                                                                          |
      |                       | You can enter a maximum of 255 characters.                                                                                                            |                                                                                                          |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------+

   .. _dns_usermanual_0036__table865604093219:

   .. table:: **Table 2** Tag key and value requirements

      +-----------------------+--------------------------------------------------------------------------------------+-----------------------+
      | Parameter             | Requirements                                                                         | Example Value         |
      +=======================+======================================================================================+=======================+
      | Key                   | -  Cannot be left blank.                                                             | example_key1          |
      |                       | -  Must be unique for each resource.                                                 |                       |
      |                       | -  Can contain a maximum of 36 characters.                                           |                       |
      |                       | -  Can contain only letters, digits, hyphens (-), at signs (@), and underscores (_). |                       |
      +-----------------------+--------------------------------------------------------------------------------------+-----------------------+
      | Value                 | -  Cannot be left blank.                                                             | example_value1        |
      |                       | -  Can contain a maximum of 43 characters.                                           |                       |
      |                       | -  Can contain only letters, digits, hyphens (-), at signs (@), and underscores (_). |                       |
      +-----------------------+--------------------------------------------------------------------------------------+-----------------------+

8. Click **OK**.

9. Switch back to the **Record Sets** page.

   View the created wildcard DNS record set in the record set list of the domain name, and ensure that the status of the record set is **Normal**.

.. |image1| image:: /_static/images/en-us_image_0148391090.png
