
###  **Automated ELK Stack Deployment**

The files in this repository were used to configure the network depicted below.

![](Images/Digrams/Redteam_Network_DM.PNG)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the .yml file may be used to install only certain pieces of it, such as Filebeat.

The ansible-playbooks elk.yml and the filebeat-playbook.yml are needed to create and implement the Elk-Server.

This document contains the following details:

* Description of the Topology
* Access Policies
* ELK Configuration
* Beats in Use
* Machines Being Monitored
* How to Use the Ansible Build


## Description of the Topology


The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.


Load balancing ensures that the application will be highly available, in addition to restricting access to the network.


What aspect of security do load balancers protect?
Load Balancing contributes to the Availability aspect of security in regards to the CIA Triad.


What is the advantage of a jump box?
The advantage of a JumpBox is the orgination point for launching Administrative Tasks. This ultimately sets the JumpBox as a SAW (Secure Admin Workstation). All Administrators when conducting any Administrative Task will be required to connect to the JumpBox (SAW) before performing any task/assignment.
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.


What does Filebeat watch for?
Filebeat watches for log files/locations and collects log events.


What does Metricbeat record?
Metricbeat records metric and statistical data from the operating system and from services running on the server.


The configuration details of each machine may be found below:



Name
IP Address
Usage
OS




JumpBox
10.0.0.4
Ansible
Linux (Ubuntu 18.04)


DVWA-WEB-1
10.0.0.5
Docker-DVWA
Linux (Ubuntu 18.04)


DVWA-WEB-2
10.0.0.6
Docker-DVWA
Linux (Ubuntu 18.04)


DVWA-WEB-3
10.0.0.7
Docker-DVWA
Linux (Ubuntu 18.04)





ELk-Server
10.1.0.4
Elk
Linux (Ubuntu 18.04)



## **Access Policies
  
The machines on the internal network are not exposed to the public Internet.
Only the JumpBox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
-Personal IP Address
Machines within the network can only be accessed by SSH.

The only machine that is able to connect to the Elk-Server (10.1.0.4) is via JumpBox from Private IP (10.0.0.4)

A summary of the access policies in place can be found in the table below.
