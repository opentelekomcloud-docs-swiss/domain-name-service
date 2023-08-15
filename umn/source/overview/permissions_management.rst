:original_name: dns_pd_0002.html

.. _dns_pd_0002:

Permissions Management
======================

If you need to assign different permissions to employees in your enterprise to access your DNS resources, IAM is an ideal choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control, helping you securely manage access to your cloud resources.

With IAM, you can use your account to create IAM users, and assign permissions to the users to control their access to specific resources. For example, some software developers in your enterprise need to use DNS resources but should not be able delete the resources or perform any other high-risk operations. In this scenario, you can create IAM users for the software developers and grant them only the permissions required for using specific resources.

Skip this part if your account does not require individual IAM users for permissions management.

IAM free of charge. You pay only for cloud resources you purchase or use.

DNS Permissions
---------------

By default, new IAM users do not have permissions assigned. You need to add a user to one or more groups, and attach permissions policies or roles to these groups. Users inherit permissions from the groups to which they are added and can perform specified operations on cloud services.

DNS resources include the following:

-  Private zone: project-level resource
-  PTR record: project-level resource

DNS permissions for global-level resources cannot be set in the global service project and must be granted for each project.

To assign DNS permissions to a user group, specify the scope as region-specific projects and select projects for the permissions to take effect. If **All projects** is selected, the permissions will take effect for the user group in all region-specific projects. When accessing the DNS service, users need to switch to a region where they have been authorized to use DNS resources.

You can grant users permissions by using roles and policies.

-  Roles: A type of coarse-grained authorization mechanism that defines permissions related to user responsibilities. This mechanism provides only a limited number of service-level roles for authorization. When using roles to grant permissions, you need to also assign other roles on which the permissions depend, for the permissions to take effect. However, roles are not ideal for fine-grained authorization and secure access control.
-  Policies: A type of fine-grained authorization mechanism that defines permissions required to perform operations on specific cloud resources under certain conditions. This mechanism allows for more flexible policy-based authorization, and meets the requirements for secure access control. For example, you can grant DNS users only the permissions for managing a certain type of DNS resources. Most policies define permissions based on APIs. For the API actions supported by the DNS service, see Permissions Policies and Supported Actions in the *Domain Name Service API Reference*.

:ref:`Table 1 <dns_pd_0002__table815366162217>` lists all system-defined roles or policies supported by DNS.

.. _dns_pd_0002__table815366162217:

.. table:: **Table 1** DNS roles or policies

   +--------------------+--------------------------------------------------------------------------------------------------+-----------------------+------------------------------------------------------------------------------------------------+
   | Role/Policy Name   | Description                                                                                      | Type                  | Dependency                                                                                     |
   +====================+==================================================================================================+=======================+================================================================================================+
   | DNS FullAccess     | All permissions on DNS.                                                                          | System-defined policy | None                                                                                           |
   +--------------------+--------------------------------------------------------------------------------------------------+-----------------------+------------------------------------------------------------------------------------------------+
   | DNS ReadOnlyAccess | Read-only permissions for DNS. Users granted with these permissions can only view DNS resources. | System-defined policy | None                                                                                           |
   +--------------------+--------------------------------------------------------------------------------------------------+-----------------------+------------------------------------------------------------------------------------------------+
   | DNS Administrator  | All permissions on DNS.                                                                          | System-defined role   | This role depends on the **Tenant Guest** and **VPC Administrator** roles in the same project. |
   +--------------------+--------------------------------------------------------------------------------------------------+-----------------------+------------------------------------------------------------------------------------------------+

:ref:`Table 2 <dns_pd_0002__table6721119192915>` lists the common operations supported by each DNS system policy or role. Choose proper system policies according to this table.

.. _dns_pd_0002__table6721119192915:

.. table:: **Table 2** Common operations supported by each system-defined DNS policy or role

   +------------------------------------------+----------------+--------------------+-------------------+
   | Operation                                | DNS FullAccess | DNS ReadOnlyAccess | DNS Administrator |
   +==========================================+================+====================+===================+
   | Creating a private zone                  | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Viewing a private zone                   | Y              | Y                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Modifying a private zone                 | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Deleting a private zone                  | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Deleting private zones in batches        | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Associating a VPC with a private zone    | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Disassociating a VPC from a private zone | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Adding a record set                      | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Viewing a record set                     | Y              | Y                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Modify a record set                      | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Deleting a record set                    | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+
   | Delete record sets in batches            | Y              | x                  | Y                 |
   +------------------------------------------+----------------+--------------------+-------------------+

Related References
------------------

-  `What Is IAM? <https://docs.sc.otc.t-systems.com/usermanual/iam/iam_01_0026.html>`__
-  :ref:`Creating a User and Granting DNS Permissions <dns_usermanual_0027>`
-  `Supported Actions <https://docs.sc.otc.t-systems.com/en-us/api/dns/dns_api_70001.html>`__
