# Elastic SIEM Configuration and Management
# Overview
Elastic  SIEM Configuration and Management: Successfully set up and configured Elastic  SIEM in a home lab environment. Demonstrated proficiency in deploying a Kali Linux VM, configuring Elastic Agents for log collection, and forwarding data to the SIEM for effective security event monitoring.
<br />
<br />
# languages and Utilities Used:
<li>Oracle virtual box</li>
<li>Elastic</li>
<li>Kali Linux</li>
<li>KQL</li>
<br />
<br />

# Kali Linux Virtual Machine Deployment on Oracle virtual Box
The first thing would be to deploy kali linux vm on oracle virtual box as shown below.(the default username is kali, the default password is kali)
<br />
<br />
<img src="https://github.com/user-attachments/assets/d0175eb1-f267-4056-9d65-240914d74753" height="30%" width="90%" alt="Kali-machine-deployed">
# Creating an elastic acount and Setting up Elastic Defend Integration
This allows us to obtain the elastic agent that will allow us to collect event logs from the kali machine
<br />
<br />
<img src="https://github.com/user-attachments/assets/1a87f446-8d6d-4b44-936e-91dec9ef3f11" height="30%" width="90%" alt="Elastic defence integration">

# Installing the elastic  agent onto the virtual machine
Installing an agent onto the virtual machine that allows the collection of event logs to elasticstack onto the kali virtual machine.
<br />
<br />
<img src="https://github.com/user-attachments/assets/49e406d6-25ed-47c4-ab34-2d9dc48f6145" height="30%" width="90%" alt="Installing the elastic stack agaent onto the virtual machine">

# Creating an alert rule for nmap scans.
Here we used the KQL Query to <code>process.arg:"nmap"</code> as our custom rule for our alerts and after doing so run some nmap scans on our virtual machine to test the rule and the entire system and the alerts \
<br />
<br />
<img src="https://github.com/user-attachments/assets/ea752a07-c5a7-4ba0-9e13-fea0b6bff054" height="30%" width="90%" alt="Creating the security rule for our virtual machine">


# Running nmap scans on the virtual machine
The next step would be to run nmap scans on the  virtual machines to test the alert rule. and the image below illustrates the nmap scans I ran on the virtual machine that are: <code>sudo nmap -A -p <vm's ip address > </code> and <code>sudo nmap -sT <vm's ip address></code>
<br />
<br />
<img src="https://github.com/user-attachments/assets/68137acf-c1f5-4d7a-9791-48b3804df76d" height="30%" width="90%" alt="Running Nmap scans">

# Observing logs on Elastic SIEM
Next we check the SIEM to confirm if any alerts have been raised from the nmap scan. In our case what happened was that alerts were raised from us running nmap scans.In our scenario about 213 nmap scans have been raised.
<br />
<br />
<img src="https://github.com/user-attachments/assets/51198f33-7835-40f0-b98f-3eb10d5c6006" height="30%" width="90%" alt="Running Nmap scans">

We can get a summary of when different alerts took place with the illustration below
<br />
<br />
<img src="https://github.com/user-attachments/assets/a0bfd36a-5081-432b-9362-2102b19d3c66" height="30%" width="90%" alt="Nmap">
