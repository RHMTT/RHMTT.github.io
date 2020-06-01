
# Objective

Demonstrate the use of [Ansible Tower workflow](https://docs.ansible.com/ansible-tower/latest/html/userguide/workflows.html).  Workflows allow you to configure a sequence of disparate job templates (or workflow templates) that may or may not share inventory, playbooks, or permissions.

For this exercise we will create a workflow to check if our server is online and responding with our tomcat url, if it is report back with the system health information, but if it isnt then run a remediation to install tomcat onto the server.

# Guide

## Step 1: Create a Job Template

1. Make sure you are logged in as the **admin** user.

2. Click on the **Templates** link on the left menu.  

3. Click on the green **+** button. Select the **Workflow Template**.  

4. Fill out the the form as follows:

| Parameter | Value |
|---|---|
| Name  | Workshop Workflow  |
|  Organization |  Default |
|  Inventory |  Student Inventory |

5. Click on the **Save** button

![workflow creation](images/workflow_create.gif)

## Step 2: The Workflow Visualizer

1. When you click the **SAVE** the **WORKFLOW VISUALIZER** should automatically open.  If not click on the blue **WORKFLOW VISUALIZER** button.  

2. By default only a green **START** button will appear.  Click on the **START** button.  

3. The **ADD A TEMPLATE** window will appear on the right.  Select the *Create SVM and Interface* Job Template that was created for you.  Use the drop down box to select run.  Click the green **SELECT** button.

   ![add a template](images/add-a-template.png)

   The `Create SVM and Interface` job template is now a node.  Job or workflow templates are linked together using a graph-like structure called nodes. These nodes can be jobs, project syncs, or inventory syncs. A template can be part of different workflows or used multiple times in the same workflow. A copy of the graph structure is saved to a workflow job when you launch the workflow.

   ![configure backup node](images/configure-backup.png)

## Step 3: Add the Enable NFS Job Template

1. Hover over the *Create SVM and Interface* node and click the green **+** symbol.  The **ADD A TEMPLATE** window will appear again.

2. Select the **Enable NFS** Job Template.  For the **Run** parameter select **On Success** from the drop down menu.

3. Click **SELECT**

4.  A green line should exist between **Create SVM and Interface** and **Enable NFS**

    ![banner node](images/enable-nfs.png)

## Step 4: Add the Create Policy Job Template

1. Hover over the *Create SVM and Interface* node (not the **Enable NFS** node) and click the green **+** symbol.  The **ADD A TEMPLATE** will appear again.

2. Select the **Create Policy** Job Template.  For the **Run** parameter, select **On Success** from the drop down menu.  Once the **SELECT** button appears green click it.

    ![configure user node](images/create-policy.png)


## Step 5: Add the Create NFS Mounts Job Template

1.  Hover over the **Enable NFS** node and click the green **+** symbol.  The **ADD A TEMPLATE** will appear again.

2. Select the **Create NFS Mounts** job template.  For the **Run** parameter, select **On Success** from the drop down menu.  

   ![configure restore node](images/create-nfs.png)

## Step 6: Create a converged link

1. Hover over the **Network-User** node and click the blue **chain** symbol.

2. Now, click on the existing **Network-Restore**.  A **ADD LINK** window will appear.  For the **RUN** parameter choose **On Failure**.

    ![restore node](images/complete-storage-workflow.png)

3. Click the green **SAVE** button

## Step 7: Run the Workflow - NOT GOING TO WORK.  HASN'T BEEN TESTED YET

1. Return to the **Templates** window

2. Click the rocket ship to launch the **Workshop Workflow** workflow template.

   ![workflow job launched](images/running-workflow.png)

    At any time during the workflow job you can select an individual job template by clicking on the node to see the status.

# Takeaways

You have
 - created a workflow template that creates a backup, attempts to create a user and banner for all network nodes
 - made the workflow robust, if either job template fails it will restore to the specified backup
 - launched the workflow template and explored the **VISUALIZER**

---

# Complete

You have completed lab exercise 9


