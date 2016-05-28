# Capsules / Smart Proxies

Satellite 6 has the concept of **Capsules** which are analogous to **Smart Proxies** in [Foreman](http://theforeman.org)

A **Capsule** provides functionality to the Satellite server.
Examples of **Capsules** are

* DHCP Capsule  - enabling Satellite 6 to reserve IP addresses on a DHCP server, including all the options necessary for a PXE boot
* DNS Capsule   - enabling the Satellite to create, update and remove forward and reverse DNS records
* Realm Capsule - enabling Satellite to create Kerberos Host Principles on a Kerberos Server
* TFTP Capsule  - enabling the Satellite server to place files required for PXE booting a Host
* Puppet Capsule - Providing Puppet functionality to Satellite (usually the Satellite server itself)

These are usually, but not always, on remote servers and not on the main Satellite server itself. However, that said, in this introductory session we configured our Satellite to have multiple local **Capsules**.

We chose to run TFTP,DHCP & DNS **Capsules** on our main Satellite server

**Capsules** can be found via the **Infrastructure** menu
