Configuring GitLab
=========================

Now that we have Ansible Tower configured to pull down our initial repository from Gitlab, we want to configure Gitlab and Tower so that the communication is bi-directional, thus at the end of this section we should be able to perform a git commit and see it automaticatlly tell Tower to kick off a job template it is referenced from.

Logging into Gitlab
==================

Your GitLab url and credentials were supplied to you on the page created for this workshop.

Creating a Personal Access Token
=============================
Step 1:
-------
In GitLab click on your user icon and select settings

![GitLab Settings](images/GitLab_User_Settings.png)

Step 2:
-------
Now Select the Access Tokens menu

![GitLab Access Token](images/GitLab_User_Access_Token.png)

Step 3:
-------
Fill out the form

| Key          | Value           |
|--------------|-----------------|------------------------------------------|
| Name         | Student Tower Token|                                          
| Expires at | Leave Blank                 |
| Scope         | API

![GitLab Access Token](images/GitLab_User_Create_Access_Token.png)

Step 4:
-------
Click on Create personal access token.

![GitLab Save Token](images/GitLab_Create_Token_Button.png)

Step 5:
-------
Once created make sure to copy the token as it will become a hidden secret afterwards.

![GitLab Access Token](images/GitLab_User_Token.png)

Create Gitlab Token Credential in Tower
========================

Go to Credentials in Tower and create a new credential

Step 6:
-------

Select CREDENTIALS from the left hand panel under resources

![Cred](images/1-tower-credentials.png)

Step 7:
-------

Click the ![Add](images/add.png) icon and add new credential

Step 8:
-------

Complete the form using the following entries:

| Key          | Value           
|--------------|-----------------|------------------------------------------|
| Name         | Studen GitLab Token |                                          |
| Organization | Default         |                                          |
| Type         | GitLab Personal Access Token         |                                          |
| TOKEN     | **Replace # with your student number**   |        | 

![Tower GitLab Token](images/Tower_GitLab_Token_Credential.png)

Step 9:
-------

Select SAVE ![Save](images/at_save.png)  

