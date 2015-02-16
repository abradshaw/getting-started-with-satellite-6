# Activation Keys

Now we shall create an Activation Key.

>**NOTE** Unfortunatley the version of subscription manager shipped in RHEL6.5 (and below) does not function correctly with Activation Keys. The default **subscription_manager_registration** snippet has a fix to ensure that the RH Common repo is included, so that provisioning should work fine.
RHEL6.6 and RHEL7 do work correctly.

Before doing this step, make sure your **Content View** has finished publishing

To create an activation key - click

```Content > Activation Keys```

followed by the **New Activation Key** button. Fill in the Name, select the **Lifecycle Environment** and **Content View** and click **Save**

Once the key is created, make sure that the **Release Version** is set

![Set the release version](../images/activation-key-rel-ver.png)

and then go to the **Subscriptions** tab, to add your subscriptions.

![Add your subscriptions](../images/activation-key-add-subs.png)

Optionally, take a look on the **Product Content** to see if you you want change any of the defaults






