Installing Jenkins
=========================

Ansible can Install and configure Jenkins for us, we will be using a pre built role with a dependancy to show how this can be done and this should give you some insight into how your own Ansible roles can be used in the future.

Lets Examine the playbook we will be running.
```yaml
- name: Install and Configure Jenkins
  hosts: jenkins
  become: true

roles:
    - role: geerlingguy.java
    - role: geerlingguy.jenkins
```
We can see this has been limited to the hosts of Jenkins.
And we are going to be running 2 roles

Java is a dependancy for Jenkins so we need to ensure we have java installed first before installing Jenkins.

Both of these roles can be found on galaxy.ansible.com along with the documentation of what variables we can modify

https://galaxy.ansible.com/geerlingguy/jenkins

We will want to specify the following variables 
 - The version of Java
 - Jenkins Hostname
 - Jenkins Admin Password

