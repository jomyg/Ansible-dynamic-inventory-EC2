# Ansible-dynamic-inventory-EC2-apache


In this demo, we will utilize [Dynamic inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html) feature of Ansible to track the details of newly created instances and deploy a sample HTML website to these EC2 instances. Often an Ansible inventory(static) fluctuates over time, with hosts spinning up and shutting down in response to business demands and the static inventory solutions will not be able to serve the needs. You may need to track hosts for multiple instances and it can be hectic to manage the inventory file each time.Hence, to overcome this we can make use of the option dynamic inventory to get the details of the instances and provison the EC2 according to the requirements.

## Overview

We will be provisioning the following :

- Provision an SSH keypair, security groups and EC2 instance through Ansible.
- Retrieve the IP Address of instance using dynamic inventory concept.
- Configuring the web server through Ansible.

## Prerequisite

- Access key and secret key for AWS IAM user with administrator access.
- Install Ansible2 on your machine which is master.
