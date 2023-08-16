:original_name: dns_faq_002.html

.. _dns_faq_002:

What Are the Private DNS Servers Provided by the DNS Service?
=============================================================

Private DNS servers are used in VPCs to:

-  Resolve private domain names and internal domain names of cloud services.
-  Forward domain name requests to public DNS servers.

You can use private DNS servers provided by the DNS service to:

-  Resolve private domain names used in VPCs.
-  Access cloud services such as OBS and SMN.
-  Allow ECSs without EIPs to access the Internet.

:ref:`Table 1 <dns_faq_002__table1689717942520>` lists private DNS server addresses provided by the DNS service in different regions.

.. _dns_faq_002__table1689717942520:

.. table:: **Table 1** Private DNS server addresses

   ====== ============================
   Region Private DNS server addresses
   ====== ============================
   eu-ch2 100.125.4.25
   \      100.125.64.24
   ====== ============================
