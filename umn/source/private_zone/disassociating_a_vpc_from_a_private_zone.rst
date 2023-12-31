:original_name: dns_usermanual_0004.html

.. _dns_usermanual_0004:

Disassociating a VPC from a Private Zone
========================================

**Scenarios**
-------------

Disassociate a VPC from a private zone if you do not want the private domain name to be resolved in this VPC. If a private zone has only one VPC associated, you cannot disassociate the VPC.

.. note::

   If you do not intend to use private domain names, delete the private zone configured for it.

**Procedure**
-------------

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

#. In the navigation pane, choose **Private Zones**.

   The **Private Zones** page is displayed.

#. Click |image1| in the upper left corner and select the desired region and project.

5. Locate the private zone from which a VPC is to be disassociated, select the VPC to be disassociated under **Associated VPC**, and click |image2| on the right of the VPC.
6. In the **Disassociate VPC** dialog box, click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0148391090.png
.. |image2| image:: /_static/images/en-us_image_0210876854.png
