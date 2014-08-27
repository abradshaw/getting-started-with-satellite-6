<style>
div.warn {
    background-color: #fcf2f2;
    border-color: #dFb5b4;
    border-left: 5px solid #dfb5b4;
    padding: 0.5em;
    }
 </style>

# Adding Red Hat Repositories

Once the manifest file has been imported, the repositories required need to be selected and syncronised

You will need three repositories at the very least to be selected

I shall focus on provisioning RHEL 6.5 hosts

Red Hat Enterprise Linux 6 Server _Kickstart_

![RHEL6 Kickstart](../images/repository-selection-1.png)

Red Hat Enterprise Linux 6 Server _RPMs_

![RHEL6 RPMs](../images/repository-selection-2.png)

Both of those are available on the main RPMs tab but the next one is available from the **Beta** tab

<div class=warn>**NOTE**
At the time of writing, Red Hat only shipped Puppet in the **RH Common Beta RPMs** channel. When Satellite 6 goes GA, it will be shipped in the non-beta version of the channel
</div>

RH Common Beta RPMs

![RH Common Beta RPMs](../images/repository-selection-3.png)

