Enable Webhook to our Install Apache Job Template
========================

Lets go back to our Apache Basic Job Template and reconfigure it for bi-directional communication to GitLab.

Under Options we want to select **ENABLE WEBHOOK**

![Add Webhook](images/tower-webhook.png)

Select SAVE ![Save](images/at_save.png)  

After saving we can have the **WEBHOOK** URL and **WEBHOOk KEY**

![Add SCM Credential](images/tower-webhook-key.png)

We need to copy these and add them to GitLab

Enable Webhook to our GitLab Project
==================

Navigate in GitLab to our Project and select on the left hand verticle Settings and then Webhooks

![Add GitLab Webhook](images/GitLab_WebHook.png)

Copy the URL from tower to **URL** and the WEBHOOK KEY to **Secret Token**
Set the trigger to be on **Push events** and lock it to the **master** branch

![GitLab WebHook Setup](images/GitLab_WebHook_Setup.png)

Select Add webhook ![Save](images/add_webhook.png)