# Ansible-dynamic-inventory-EC2-apache


[![Build](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


Simple ansible dynamic inventory EC2 creation with apache. In this demo, we will utilize [Dynamic inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html) feature of Ansible to track the details of newly created instances and deploy a sample HTML website to these EC2 instances. Often an Ansible inventory(static) fluctuates over time, with hosts spinning up and shutting down in response to business demands and the static inventory solutions will not be able to serve the needs. You may need to track hosts for multiple instances and it can be hectic to manage the inventory file each time.Hence, to overcome this we can make use of the option dynamic inventory to get the details of the instances and provison the EC2 according to the requirements.

## Overview

We will be provisioning the following :

- Provision an SSH keypair, security groups and EC2 instance through Ansible.
- Retrieve the IP Address of instance using dynamic inventory concept.
- Configuring the web server through Ansible.


## Prerequisite
-----
- Need to install ansible2 on Master node to run
- AWS CLI Programmatic user
- python3
- python3-pip
- boto3
- awscli with latest version 
-----

### Ansible installation 

```sh
amazon-linux-extras install epel -y
amazon-linux-extras install ansible2 -y
yum install python3
yum install python3-pip
pip install awscli --upgrade
ansible-galaxy collection install amazon.aws
pip3 install boto3
pip3 install boto
pip3 install botocore
```
> You need to verify the localhost ansible is now able to communicate with python3. For verify

```sh
$ ansible -i hosts localhost -m setup | grep "ansible_python_version"
        "ansible_python_version": "3.7.10"
 ```
