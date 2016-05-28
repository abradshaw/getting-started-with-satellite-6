# Prepare for Manifest Import

Once the manifest has been created, we simple need to import it into our Satellite server.

>*NOTE*: If you added the initial-organization and initial-location options to the installer you don't need to perform these steps unless you want to create additional locations or organisations. Also note that organisations and locations can be nested such as EMEA/UK or EMEA/Spain. 

However, first we must create our **Organization** and **Location**

Login to the Satellite web interface and select the Manage Organisation menu item

![Manage Organisation](../images/manage-org.png)

Click on the New Organisation button

 ![Manage Organisation](../images/new-org.png)

and fill in the entries on the first page and hit submit

![Manage Organisation](../images/new-org-page1.png)

This takes you to the second page (seen below). Here it is asking where to assign the existing node (the Satellite server itself)

![Manage Organisation](../images/new-org-page2.png)

Click the green **Assign All**

Now you will see that your new organisation has been created

![Manage Organisation](../images/new-org-final.png)

Follow a similar process to create a **location**. I created a location called Europe
