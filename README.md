# Elastic SIEM Configuration and Management.
# Overview
Elastic  SIEM Configuration and Management: Successfully set up and configured Elastic  SIEM in a home lab environment. Demonstrated proficiency in deploying a Kali Linux VM, configuring Elastic Agents for log collection, and forwarding data to the SIEM for effective security event monitoring.
< br />
<br />
# Kali Linux Virtual Machine Deployment on Oracle virtual Box.
The first thing would be to deploy kali linux vm on oracle virtual box as shown below.(the default username is kali, the default password is kali)
<br />
<br />
<img src="https://github.com/user-attachments/assets/d0175eb1-f267-4056-9d65-240914d74753" height="30%" width="90%" alt="Kali-machine-deployed">
# Creating an elastic acount and Setting up Elastic Defend Integration.
This allows us to obtain the elastic agent that will allow us to collect event logs from the kali machine
<br />
<br />
<img src="https://github.com/user-attachments/assets/1a87f446-8d6d-4b44-936e-91dec9ef3f11" height="30%" width="90%" alt="Elastic defence integration">

# Installing the elastic  agent onto the virtual machine
Installing an agent onto the virtual machine that allows the collection of event logs to elasticstack onto the kali virtual machine.
<br />
<br />
<img src="https://github.com/user-attachments/assets/49e406d6-25ed-47c4-ab34-2d9dc48f6145" height="30%" width="90%" alt="Installing the elastic stack agaent onto the virtual machine">

# Creating an alert rule for nmap scans that will log and alert you of any nmap scans to you Virtual machine.
Here we used the KQL Query to <code>process.arg:"nmap"</code> as our custom rule for our alerts and after doing so run some nmap scans on our virtual machine to tst the rule and the entire system and the alerts 

