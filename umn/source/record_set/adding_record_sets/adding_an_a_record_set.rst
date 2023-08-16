:original_name: dns_usermanual_0007.html

.. _dns_usermanual_0007:

Adding an A Record Set
======================

**Scenarios**
-------------

If you want to use a private domain name to access ECSs configured with IPv4 addresses, you can add an A record set for the domain name.

For more information about the types of record sets, see :ref:`Record Set Types and Configuration Rules <dns_usermanual_0601>`.

Prerequisites
-------------

You have an ECS and obtained an IPv4 address.

**Procedure**
-------------

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. In the navigation pane, choose **Private Zones**.

   The zone list is displayed.

4. Click |image1| in the upper left corner and select the desired region and project.

5. Click the zone name.

6. Click **Add Record Set**.

   The **Add Record Set** dialog box is displayed.

7. Set required parameters based on :ref:`Table 1 <dns_usermanual_0007__table219785892310>`.

   .. _dns_usermanual_0007__table219785892310:

   .. table:: **Table 1** Parameters for adding an A record set

      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | Parameter             | Description                                                                                                                                           | Example Value                                   |
      +=======================+=======================================================================================================================================================+=================================================+
      | Name                  | Prefix of the domain name to be resolved.                                                                                                             | www                                             |
      |                       |                                                                                                                                                       |                                                 |
      |                       | For example, if the zone name is **example.com**, the domain name prefix can be as follows:                                                           |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | -  **www**: The domain name is www.example.com, which is usually used for a website.                                                                  |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | -  Left blank: The domain name is example.com.                                                                                                        |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       |    In some cases, you may need to set the record set name to the at sign (@). However, the at sign is not supported. Leave the **Name** blank.        |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | -  **abc**: The domain name is abc.example.com, a subdomain of example.com.                                                                           |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | -  **mail**: The domain name is mail.example.com, which is typically used for an email server.                                                        |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | -  **\***: The domain name is \*.example.com, which is a wildcard domain name, indicating all subdomains of example.com.                              |                                                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | Type                  | Type of the record set.                                                                                                                               | A - Map domains to IPv4 addresses               |
      |                       |                                                                                                                                                       |                                                 |
      |                       | If a message is displayed indicating that the record set you are trying to create exists, the record set conflicts with an existing record set.       |                                                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | TTL (s)               | Cache duration of the record set on a local DNS server, in seconds.                                                                                   | The default value is 300s, which is, 5 minutes. |
      |                       |                                                                                                                                                       |                                                 |
      |                       | The value ranges from **300** to **2147483647**, and the default is **300**.                                                                          |                                                 |
      |                       |                                                                                                                                                       |                                                 |
      |                       | If your service address changes frequently, set TTL to a smaller value.                                                                               |                                                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | Value                 | IPv4 addresses mapped to the domain name.                                                                                                             | 192.168.12.2                                    |
      |                       |                                                                                                                                                       |                                                 |
      |                       | You can enter a maximum of 50 record values, each on a separate line.                                                                                 | 192.168.12.3                                    |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | Tag                   | (Optional) Identifier of the record set.                                                                                                              | example_key1                                    |
      |                       |                                                                                                                                                       |                                                 |
      |                       | Each tag contains a key and a value. You can add a maximum of 10 tags to a record set. This parameter is displayed when you expand **More Settings**. | example_value1                                  |
      |                       |                                                                                                                                                       |                                                 |
      |                       | For details about tag key and value requirements, see :ref:`Table 2 <dns_usermanual_0007__table191971158112315>`.                                     |                                                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+
      | Description           | (Optional) Supplementary information about the record set.                                                                                            | ``-``                                           |
      |                       |                                                                                                                                                       |                                                 |
      |                       | You can enter a maximum of 255 characters.                                                                                                            |                                                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------+

   .. _dns_usermanual_0007__table191971158112315:

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

   View the added record set in the record set list of the zone and ensure that the status of the record set is **Normal**.

Related Operations
------------------

For details about how to configure A record sets, see :ref:`Routing Traffic Within VPCs <dns_qs_0006>`.

.. |image1| image:: /_static/images/en-us_image_0148391090.png
