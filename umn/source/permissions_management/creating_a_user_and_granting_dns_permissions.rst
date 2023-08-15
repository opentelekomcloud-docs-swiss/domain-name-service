:original_name: dns_usermanual_0027.html

.. _dns_usermanual_0027:

Creating a User and Granting DNS Permissions
============================================

This chapter describes how to use IAM to implement fine-grained permissions control for your DNS resources. With IAM, you can:

-  Create IAM users for employees based on your enterprise's organizational structure. Each IAM user will have their own security credentials for accessing DNS resources.
-  Grant only the permissions required for users to perform a specific task.
-  Entrust another account or cloud service to perform efficient O&M on your DNS resources.

Skip this part if your account does not need individual IAM users.

The following describes the procedure for granting permissions (see :ref:`Figure 1 <dns_usermanual_0027__en-us_topic_0172268189_fig12481104618719>`).

**Prerequisites**
-----------------

Learn about the permissions.

Process Flow
------------

.. _dns_usermanual_0027__en-us_topic_0172268189_fig12481104618719:

.. figure:: /_static/images/en-us_image_0000001089067433.png
   :alt: **Figure 1** Process for granting permissions

   **Figure 1** Process for granting permissions

#. .. _dns_usermanual_0027__en-us_topic_0172268189_li10269636890:

   Create a user group and grant permissions.

   Create a user group on the IAM console and attach the DNS ReadOnlyAccess policy to the group, which grants users read-only permissions to DNS resources.

#. Create an IAM user.

   Create a user on the IAM console and add the user to the group created in step :ref:`1 <dns_usermanual_0027__en-us_topic_0172268189_li10269636890>`.

#. Log in and verify permissions.

   Log in to the DNS console by using the created user, and verify that the user only has read permissions for DNS.

   -  Choose **Service List** > **Domain Name Service**. On the DNS console, choose **Dashboard** > **Private Zones**. On the displayed page, click **Create Private Zone**. If the private zone cannot be created, the **DNS ReadOnlyAccess** policy has already taken effect.
   -  Choose any other service in **Service List**. If a message appears indicating that you have insufficient permissions to access the service, the **DNS ReadOnlyAccess** policy has already taken effect.
