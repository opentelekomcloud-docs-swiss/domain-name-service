:original_name: dns_api_70005.html

.. _dns_api_70005:

Tag
===

.. table:: **Table 1** Tag management

   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Permission                              | API                                                              | Action      | Dependent Permission | IAM Project | Enterprise Project |
   |                                         |                                                                  |             |                      |             |                    |
   |                                         |                                                                  |             |                      | (Project)   |                    |
   +=========================================+==================================================================+=============+======================+=============+====================+
   | Add a resource tag.                     | POST /v2/{project_id}/{resource_type}/{resource_id}/tags         | dns:tag:set | ``-``                | Y           | x                  |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Add or delete resource tags in batches. | POST /v2/{project_id}/{resource_type}/{resource_id}/tags/action  |             |                      |             |                    |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Delete a resource tag.                  | DELETE /v2/{project_id}/{resource_type}/{resource_id}/tags/{key} |             |                      |             |                    |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Query tags of a resource.               | GET /v2/{project_id}/{resource_type}/{resource_id}/tags          | dns:tag:get | ``-``                | Y           | x                  |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Query project tags.                     | GET /v2/{project_id}/{resource_type}/tags                        |             |                      |             |                    |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
   | Query resources by tag.                 | POST /v2/{project_id}/{resource_type}/resource_instances/action  |             |                      |             |                    |
   +-----------------------------------------+------------------------------------------------------------------+-------------+----------------------+-------------+--------------------+
