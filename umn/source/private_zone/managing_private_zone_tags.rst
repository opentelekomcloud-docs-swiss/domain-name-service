:original_name: dns_usermanual_05044.html

.. _dns_usermanual_05044:

Managing Private Zone Tags
==========================

Scenarios
---------

A tag is the identifier of a private zone. Adding tags to private zones helps you identify and manage your private zones. You can add tags when creating a private zone or add tags to existing private zones. Up to 10 tags can be added to a private zone.

A tag consists of a key and value pair. :ref:`Table 1 <dns_usermanual_05044__ted9687ca14074ef785241145365a6175>` lists the tag key and value requirements.

.. _dns_usermanual_05044__ted9687ca14074ef785241145365a6175:

.. table:: **Table 1** Tag key and value requirements

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

Procedure
---------

**In the private zone list, search for the private zone by tag key or value.**

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. On the **Dashboard** page, click **Private Zones** under **My Resources**.
4. Click |image1| in the upper left corner and select the desired region and project.
5. In the upper right corner of the private zone list, click **Search by Tag**.

6. Enter the tag key and value of the private zones you want to query.

   Both the tag key and value must be specified. The system automatically displays the private zones you are looking for if both the tag key and value are matched.

7. Click **+** to add more tag keys and values.

   You can add multiple tag keys and values to refine your search results. If you add more than one tag to search for private zones, the private zones containing all specified tags will be displayed.

8. Click **Search**.

   The system searches for private zones by tag key and value.

**In the private zone details area, add, delete, modify, and query tags.**

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. On the **Dashboard** page, click **Private Zones** under **My Resources**.
4. Click |image2| in the upper left corner and select the desired region and project.

5. On the **Private Zones** page, click |image3| to view details about the private zone.

   The details of the private zone are displayed.


   .. figure:: /_static/images/en-us_image_0000001257030905.png
      :alt: **Figure 1** Private zone details

      **Figure 1** Private zone details

6. In the **Tags** area, query, add, modify, or delete tags.

   -  Query tags.

      In the **Tags** area, view details about tags, including the number of tags and the key and value of each tag.

   -  Add a tag.

      Click **Add Tag** in the upper left corner. In the displayed **Add Tag** dialog box, enter the tag key and value, and click **OK**.

   -  Modify a tag.

      Locate the row that contains the tag you want to edit and click **Edit** in the **Operation** column. In the **Edit Tag** dialog box, change the tag value and click **OK**.

   -  Delete a tag.

      Locate the row that contains the tag to be deleted and click **Delete** in the **Operation** column. In the displayed **Delete Tag** dialog box, click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0148391090.png
.. |image2| image:: /_static/images/en-us_image_0148391090.png
.. |image3| image:: /_static/images/en-us_image_0000001256963621.png
