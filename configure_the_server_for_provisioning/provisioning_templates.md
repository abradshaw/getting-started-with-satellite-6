# Provisioning Templates

One of the changes from the beta version is that now, copies of provisioning templates are copied to your location and organisation, but they are read only copies. You can see this from the small padlocks in the **Locked** Column

This is a nice last minute change (from the beta) as editing one template no longer affects other orgs.

If you want to change one of them, then you will need to clone it

The two that we require for provisioning are **Kickstart default PXELinux** and **Satellite Kickstart Default**. The later brings in the **subscription_manager_registration** snippet also

![](../images/provisioning-templates.png)

Only one change is required at this point. For both  **Kickstart default PXELinux** and **Satellite Kickstart Default** click on them and go to the Association tab and associate them to the **Operating System** - in this case **RHEL Server 6.5**

![Provisioning template association](../images/provisioning-template-association.png)

