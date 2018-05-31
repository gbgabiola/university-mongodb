# Lab 2.0: Create an Atlas Sandbox Cluster (Ungraded)

Please note that, while we've labeled this as a lab, it is **ungraded**. This writeup is here simply to get you started on creating an Atlas cluster.

1. Go to https://cloud.mongodb.com/links/registerForAtlas and complete the account creation form you see on that page. Please make sure you see the message "Sign up for MongoDB Atlas" at the top of the page.
2. Once you have completed the registration form, in the next page that appears, you will be asked to choose a new group name. We use groups to manage access to Atlas clusters. Please use the name, **m001-sandbox**.
3. Once you have created a group, in the next page, enter the name, **Sandbox** for your cluster.
4. On the same page, select the **M0** instance size. Note that the "Pricing" now changes to say "$0.00/forever". You do **NOT** need to enter a credit card to create a free-tier Atlas cluster (M0). They are free.
5. Scroll to the bottom of the cluster-creation form and enter an administrative username and password. Please enter the username, **m001-student** and the password, **m001-mongodb-basics**
6. Once you've entered your username and password, click **Confirm & Deploy**. You will need to wait a few minutes for your cluster to be spun up.
7. Once your cluster is ready, click on the **Security tab** and then on the **IP Whitelist** tab. Click the **ADD IP ADDRESS** button and, then, in the modal that pops up, click **ALLOW ACCESS FROM ANYWHERE**. Click the **CONFIRM** button and wait while the security settings for your cluster are configured.

*Note that we do not generally recommend opening an Atlas cluster to allow access from anywhere. We do that for this class to minimize network issues that you might run into.*