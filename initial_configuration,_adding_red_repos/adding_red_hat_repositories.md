# Adding Red Hat Repositories

Once the manifest file has been imported, the repositories required need to be selected and synchronised.

You will need three repositories at the very least to be selected:

>*NOTE*: I shall focus on provisioning RHEL 6.5 hosts in my example but if you prefer to stick with the latest version, its better to use the **6Server** repository. The RHEL7 repositories have t

>*NOTE*: The 6Server or 7Server offer a rolling release repository. It is highly recommended to sync the kickstarts even if you're not using them.

Red Hat Enterprise Linux 6 Server _Kickstart_

![RHEL6 Kickstart](../images/repository-selection-1.png)

Red Hat Enterprise Linux 6 Server _RPMs_

![RHEL6 RPMs](../images/repository-selection-2.png)

RH Common RPMs

![RH Common RPMs](../images/repository-selection-3.png)
