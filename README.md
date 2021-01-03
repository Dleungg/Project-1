# Project-1
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Ansible file may be used to install only certain pieces of it, such as Filebeat.

*Elk Playbook

*Filebeat Playbook

This document contains the following details:

Description of the Topologu
Access Policies
ELK Configuration

Beats in Use
Machines Being Monitored


How to Use the Ansible Build


Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
Load balancing ensures that the application will be highly reliable and accessible, in addition to restricting traffic to the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log data and system metrics and statistics.


The configuration details of each machine may be found below.



Name
Function
IP Address
Operating System




Jump Box
Gateway
10.0.0.1
Linux


Elk-VM
Gateway




TODO





TODO







Access Policies
The machines on the internal network are not exposed to the public Internet.
Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

TODO: Add whitelisted IP addresses

Machines within the network can only be accessed by _____.

TODO: Which machine did you allow to access your ELK VM? What was its IP address?

A summary of the access policies in place can be found in the table below.



Name
Publicly Accessible
Allowed IP Addresses




Jump Box
Yes/No
10.0.0.1 10.0.0.2














Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...

*The Ansible Playbook/Script can be used install a variety of different servers within a infrastructure. The primary advantage of Ansible is that it allows IT administrators to automate *********************************************
TODO: What is the main advantage of automating configuration with Ansible?

The playbook implements the following tasks:

After running the Ansible playbook, the installation of ELK is firstly constructed by :

1. Installing an application called Docker
  - Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.
 
2. Once Docker is installed the Playbook installs Python3-pip
  - This is a package-management system written in Python which allows a connection to an online repository of public and paid-for private packages to install onto your servers.

3. Because the size of the ELK server is greater than the amount allowed on the Virtual Machine, within the Playbook ensuring that the virtual memory is up to date a command within the playbook is used to ensure that there is enough memory

4. Once everything is up to date, the Virtual machine will test to ensure that everything was installed smoothly.



Target Machines & Beats
This ELK server is configured to monitor the following machines:

*104.43.214.193

*103.41.210.192

We have installed the following Beats on these machines:

*Filebeat 

*Metricbeat

These Beats allow us to collect the following information from each machine:

Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.

Metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as Elasticsearch or Logstash.

Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:
SSH into the control node and follow the steps below:

Copy the ansible playbook file to virtual machine.
Update the ansible.cfg file to include the host domain to where you would like the installion to occur
Run the playbook, and navigate to ELK server URL which is http://[your.IP]:5601/app/kibana to check that the installation worked as expected.
