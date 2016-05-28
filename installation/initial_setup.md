# Initial Setup for Satellite 6.0/6.1:

The **katello-installer** is used to perform the initial setup and any future changes to the existing config. Its a puppet based installation and so can be re-run without overiding the previous settings.

We will create an "all-in-one" deployment, meaning that the Satellite will have the additional roles of TFTP proxy, DHCP server and DNS server added at install time.

```
katello-installer  --capsule-dns true --capsule-dns-forwarders \
8.8.8.8 --capsule-dns-interface eth0 --capsule-dns-zone \
example.com --capsule-dns-reverse 30.16.172.in-addr.arpa \
--capsule-dhcp true --capsule-dhcp-interface eth0 \
--capsule-dhcp-gateway 172.16.30.1 --capsule-tftp true
```

>**Note**: It is highly recommended that you set an initial organisation and location before installing the product. The organisation should be the company using the product such as Redhat. The Location should be the datacenter location at which the product is installed (such as Europe, West Europe or EMEA).

>**Note**: forwarders are stored in ```/etc/named/options.conf``` should you wish to change them later.

>**Note**: if you omit  ```--capsule-dhcp-nameservers``` then a default nameservers option will be created in the dhcp config for the satellite servers own address, meaning that the DHCP server will advertise the satellite as the DNS server. If this is not what you want, you can add something like   ```--capsule-dhcp-nameservers 10.0.0.1, 10.0.0.2``` to the main katello-installer options above

A full list of other katello-setup options are available via
```
katello installer --help
```

Once the installer has finished, you should be able to login by pointing your browser to ```https://<servername>``` (assuming you have made the necessary firewall changes).

The installer can be re-run to enable missing options or options that have been misconfigured. It can also be used if the admin password has been lost. 

# Initial Setup for Satellite 6.2 and higher:

The katello-installer has been replaced in Satellite 6.2 and above with foreman-installer. To find the full list of options available for the foreman-installer run the command:

```
foreman-installer --help
```

>**Note**: It is highly recommended that you set an initial organisation and location before installing the product. The organisation should be the company using the product such as Redhat. The Location should be the datacenter location at which the product is installed (such as Europe, West Europe or EMEA).

Next, run the installer:

```
foreman-installer --scenario katello \
--foreman-initial-organisation "Redhat" \
--foreman-initial-location "EMEA" \
```

The installer can be re-run to enable missing options or options that have been misconfigured. It can also be used if the admin password has been lost.
