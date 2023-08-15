:original_name: dns_usermanual_06055.html

.. _dns_usermanual_06055:

Managing Record Set Tags
========================

Scenarios
---------

A tag is the identifier of a record set. Adding tags to record sets helps you identify and manage your record sets. You can add tags when adding a record set or add tags to an existing record set. Up to 10 tags can be added to a record set.

A tag consists of a key and value pair. :ref:`Table 1 <dns_usermanual_06055__ted9687ca14074ef785241145365a6175>` lists the tag key and value requirements.

.. _dns_usermanual_06055__ted9687ca14074ef785241145365a6175:

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

**In the record set list, search for record sets by tag key or value.**

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. On the **Dashboard** page, click **Private Zones** under **My Resources**.

4. Click |image1| in the upper left corner and select the desired region and project.

5. Click the private zone.

   The **Record Sets** page is displayed.

6. In the upper right corner of the record set list, click **Search by Tag**.

7. Enter the tag key and value of the record sets you want to query.

   Both the tag key and value must be specified. The system automatically displays the record sets you are looking for if both the tag key and value are matched.

8. Click **+** to add more tag keys and values.

   You can add multiple tag keys and values to refine your search results. If you add more than one tag to search for record sets, the record sets containing all specified tags will be displayed.

9. Click **Search**.

   The system searches for the record sets by tag key and value.

**In the record set details area, add, delete, modify, and query tags.**

#. Log in to the management console.

#. In the service list, choose **Network** > **Domain Name Service**.

   The DNS console is displayed.

3. On the **Dashboard** page, click **Private Zones** under **My Resources**.
4. Click |image2| in the upper left corner and select the desired region and project.

5. Click the private zone.

   The **Record Sets** page is displayed.

6. On the **Record Sets** page, click |image3| to view its details.

   The details of the record set are displayed.


   .. figure:: /_static/images/en-us_image_0000001212191716.png
      :alt: **Figure 1** Record set details

      **Figure 1** Record set details

7. In the **Tags** area, query, add, modify, or delete tags.

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
.. |image3| image:: /_static/images/en-us_image_0000001256763621.png
