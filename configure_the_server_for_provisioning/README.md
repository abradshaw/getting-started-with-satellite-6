# Configure the Server for Provisioning

There are a number of things that need to be defined before we can add a new host to be provisioned.

The following items need to be defined

* Architecture *
* Domain *
* Activation Key
* Partition Table
* Subnet
* DHCP Proxy
* DNS Proxy
* Realm Proxy
* TFTP Proxy
* Provisioning Templates

NOTES:
1. Content View First **Example@org**
  * Only need Kickstart RPMS and RH Common Beta - Promote

1. Activation Key, **Example@org** Create one, in the AK
  * set the release ver
  * set the content view
  On the Next Tab
  * add a subscription

1. ProvisionTemplates **Any Context** >
  * Kickstart Default PXE Linux > Association - tick RHEL Server 6.5 (On the Association Tab)
  * Satellite Kickstart Default for RHEL  (Same as above)

1. Subnet Needs to be defined, we cheat by going to Capsules and clicking menu Import Subnet. Fill in the values, the config that was created sets up a DCHP server with no pool, so chose your own

* Once the subnet is created, click on it and set (only needs to be down once)
  * Domains (tick example.com)
  * Proxies (set DHCP, DNS, TFTP)

1. Operating Systems
  * Partition Table - tick Kickstart Default
  * **Templates** - set **Provision** and **PXE Linux**

1. Now create the Host Group
  * Host Group
  * Network (dont bother with Realm for now
  * Operating System
  * Locations
  * Organisations
  * Activation Key

Now into Operating System and set Partition Table and Templates

Then the Host
