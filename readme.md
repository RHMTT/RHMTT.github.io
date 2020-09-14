# Ansible Workshop - Ansible for CI/CD Automation

Ansible is a simple yet powerful IT automation engine for application deployment, configuration management, and orchestration that you can learn quickly.

Ansible Tower is one of the components that makes up Red Hat Ansible Automation Platform and serves as the web ui, api and control node that executes Ansible playbooks.

This workshop will guide students through configuring Ansible Tower to connect and run through typical CI/CD processes against instances created for this workshop. Once Ansible Tower is configured, students will then progress through exercises that highlight the simplicity of Ansible as a language for automation while introducing more complex operations. 

All Ansible automations for this workshop are executed from Ansible Tower but we will be showcasing how we can trigger these from other tools in a typical CI/CD Flow.

## Presentations

The presenter deck is available here:
[Ansible CI/CD Automation](../../decks/ansible_cicd.pdf)

## Time planning

The time required to do the workshops strongly depends on a couple factors: the number of participants and how much discussions are done in between.

Having said that, the exercises themselves should take roughly 4-5 hours. The accompanying presentation itself adds another hour.

If your experience is different in schedulung these workshops, please let us know and file an issue.

## Exercises

- [Exercise 1-1 - Intro and configuration of Ansible Tower](1-1-tower)
- [Exercise 1-2 - Tower Ad-hoc commands](1-2-adhoc)
- [Exercise 1-3 - Intro to playbooks](1-3-playbook)
- [Exercise 1-4 - Ansible Tower Inventory from Git](1-4-git-inventory)
- [Exercise 1-5 - Ansible Tower Job Template](1-5-job-template)
- [Exercise 1-6 - Ansible roles](1-6-roles)
- [Exercise 1-7 - Creating Workflows](1-7-workflows)
- [Exercise 1-8 - Setting up GitLab Token](1-8-gitlab-token)
- [Exercise 1-9 - Setting up GitLab Webhook](1-9-gitlab-webhook)
- [Exercise 2-1 - Git Commit triggers](2-1-git-commit)
- [Exercise 2-2 - Git merge triggers](2-2-git-merge)
- [Exercise 3-1 - Deploy Jenkins](3-1-deploy-jenkins)
- [Exercise 3-2 - Set up Jenkins to Tower](3-2-jenkins-setup-tower)
- [Exercise 3-3 - Running Tower jobs from Jenkins](3-3-jenkins-run-tower-job)
- [Exercise 3-4 - Adding in Tower jobs into a pipeline](3-4-jenkins-pipeline)

