## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Network Diagram](https://github.com/arminadeli/Deployment-Automation/blob/main/Diagram/USYD-CS_Network_diagram.pdf)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Filebeat-playbook.yml file may be used to install only certain pieces of it, such as Filebeat.

  - _Filebeat-playbook.yml_
  - _metricbeat-playbook.yml_

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting unwanted access to the network.
- _Load balancer has been added to utilise HA of the application_
- _Jumpbox has been added as an extra layer of security to limit admin access to application servers_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the configuraiton and system health.
- _Filebeat monitors all logs and configuration changes on the server_
- _Metricbeat monitors system health and provide visualable metrics _

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function          | IP Address | Operating System |
|----------|-------------------|------------|------------------|
| Jump Box | Gateway           | 10.1.0.4   | Linux            |
| Web-1    | Web Server        | 10.1.0.5   | Linux            |
| Web-2    | Web Server        | 10.1.0.6   | Linux            |
| Web-3    | Web Server        | 10.1.0.7   | Linux            |
| ELK      | Monitoring Server | 10.2.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet.

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _119.18.1.1

Machines within the network can only be accessed by Jump Box.
- _ELK can be accessed via 10.1.0.0/24

A summary of the access policies in place can be found in the table below.

| Name     | Publicly available | IP          | Port |
|----------|--------------------|-------------|------|
| Jump box | Yes                | 119.118.1.1 | 22   |
| Web-1    | Yes                | Any         | 80   |
| Web-2    | Yes                | Any         | 80   |
| Web-3    | Yes                | Any         | 80   |
| ELK      | Yes                | Any         | 5601 |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _It will reduce the manual work
- _Reduce the human error of the configuration

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?
