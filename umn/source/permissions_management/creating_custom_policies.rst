:original_name: dns_usermanual_0051.html

.. _dns_usermanual_0051:

Creating Custom Policies
========================

You can create custom policies to supplement system-defined policies and implement more refined access control.

You can create custom policies in either of the following two ways:

-  Visual editor: Select cloud services, actions, resources, and request conditions without the need to know policy syntax.
-  JSON: Edit JSON policies from scratch or based on an existing policy.

The following describes how to create a custom policy that allows users to modify DNS zones in the visual editor and JSON view.

Some examples of common custom DNS policies are provided.

Creating a Custom Policy in the Visual Editor
---------------------------------------------

#. Log in to the management console.

#. Choose **Management & Deployment** > **Identity and Access Management**.

   The **Identity and Access Management** page is displayed.

#. In the left navigation pane, choose Policies.

#. Click **Create Custom Policy**.

   The **Create Custom Policy** page is displayed.

#. Enter a policy name.

#. Select a scope in which the policy will take effect based on the type of services to be set in this policy.

   -  **Global services**: Select this option if the services to which the policy is related are available for all regions once deployed. When creating custom policies for globally deployed services, specify the scope as **Global services**. Custom policies of this scope must be attached to user groups in the Global service region.
   -  **Project-level services**: Select this option if the services to which the policy is related are deployed in specific regions. When creating custom policies for regionally deployed services, specify the scope as **Project-level services**. Custom policies of this scope must be attached to user groups in specific regions except the Global service region.

   Select **Project-level services** here.

   .. note::

      A custom policy can contain actions of multiple services that are all globally available or all deployed only in specific projects. To define permissions required for accessing both globally available and project-specific services, create two custom policies and specify the scope respectively as **Global services** and **Project-level services**.

#. Select **Visual editor**.

#. In the **Policy Content** area, configure a custom policy.

   a. Select **Allow** or **Deny**.

   b. Select **Cloud service**.

      .. note::

         Only one cloud service can be selected for each permission block. To configure permissions for multiple cloud services, click Add Permissions or switch to the :ref:`Creating a Custom Policy in the JSON View <dns_usermanual_0051__section1627013490104>`.

   c. Select actions.

   d. (Optional) Select a resource type. For example, if you select **Specific**, you can click **Specify resource path** to specify the resource to be authorized.

   e. (Optional) Add request conditions by specifying condition keys, operators, and values.

      .. table:: **Table 1** Criterion

         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Name                              | Description                                                                                                                                                           |
         +===================================+=======================================================================================================================================================================+
         | Condition Key                     | A key in the Condition element of a statement. There are global and service-level condition keys.                                                                     |
         |                                   |                                                                                                                                                                       |
         |                                   | -  Global-level condition key: The prefix is g:, which applies to all operations, as shown in :ref:`Table 2 <dns_usermanual_0051__table183017270387>`.                |
         |                                   | -  Project-level condition key: The prefix is the abbreviation of a service, for example, dns:. This key applies only to the operations of the corresponding service. |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Operator                          | Used together with a condition key to form a complete condition statement.                                                                                            |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Value                             | Used together with a condition key and an operator that requires a keyword, to form a complete condition statement.                                                   |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

      .. _dns_usermanual_0051__table183017270387:

      .. table:: **Table 2** Global request condition

         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | Global condition keys | Type    | Description                                                                                                         |
         +=======================+=========+=====================================================================================================================+
         | g:CurrentTime         | Time    | Time when an authentication request is received. The time is in ISO 8601 format, for example, 2012-11-11T23:59:59Z. |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:DomainName          | String  | Account name                                                                                                        |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:MFAPresent          | Boolean | Whether to use multi-factor authentication (MFA) to obtain a token                                                  |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:MFAAge              | Value   | Validity period of the token obtained through MFA. This condition must be used together with g:MFAPresent.          |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:ProjectName         | String  | Project name                                                                                                        |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:ServiceName         | String  | Service name                                                                                                        |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:UserId              | String  | IAM user ID                                                                                                         |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+
         | g:UserName            | String  | IAM username                                                                                                        |
         +-----------------------+---------+---------------------------------------------------------------------------------------------------------------------+

#. (Optional) Switch to the JSON view. Then you can modify the policy content in the JSON structure.

   .. note::

      If the JSON structure is wrong after modification, check the content, or click **Reset** to cancel the modification

#. (Optional) To add another permission block for the policy, click Add Permissions. Alternatively, click the plus (+) icon on the right of an existing permission block to clone its permissions.

#. (Optional) Describe the policy.

#. Click **OK**. The custom policy is created.

#. Assign the policy to a user group so that users in the group can inherit the permissions of the policy by referring to :ref:`Creating a User and Granting DNS Permissions <dns_usermanual_0027>`.

.. _dns_usermanual_0051__section1627013490104:

Creating a Custom Policy in the JSON View
-----------------------------------------

#. Log in to the management console.

#. Choose **Management & Deployment** > **Identity and Access Management**.

   The **Identity and Access Management** page is displayed.

#. In the left navigation pane, choose Policies.

#. Click **Create Custom Policy**.

   The **Create Custom Policy** page is displayed.

#. Enter a policy name.

#. Select a scope in which the policy will take effect based on the type of services to be set in this policy.

   -  **Global services**: Select this option if the services to which the policy is related are available for all regions once deployed. When creating custom policies for globally deployed services, specify the scope as **Global services**. Custom policies of this scope must be attached to user groups in the Global service region.
   -  **Project-level services**: Select this option if the services to which the policy is related are deployed in specific regions. When creating custom policies for regionally deployed services, specify the scope as **Project-level services**. Custom policies of this scope must be attached to user groups in specific regions except the Global service region.

   Select **Project-level services** here.

   .. note::

      A custom policy can contain actions of multiple services that are all globally available or all deployed only in specific projects. To define permissions required for accessing both globally available and project-specific services, create two custom policies and specify the scope respectively as **Global services** and **Project-level services**.

#. Select **JSON**.

#. (Optional) Click **Select Existing Policy**, and select a policy to use it as template, such as **DNS FullAccess**.

#. Click **OK**.

#. Modify the statements in the template.

   -  **Effect**: Enter **Allow** or **Deny**.
   -  **Action**: Enter the actions listed in the DNS API actions table, for example, dns:zone:create.

   .. note::

      The **Version** value of a custom policy must be **1.1**.

#. (Optional) Describe the policy.

#. Click **OK**. If the policy list is displayed, the policy is created successfully. If a message indicating incorrect policy content is displayed, modify the policy.

#. Assign the policy to a user group so that users in the group can inherit the permissions of the policy by referring to :ref:`Creating a User and Granting DNS Permissions <dns_usermanual_0027>`.
