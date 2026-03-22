# labb1_azure_CS
In this lab, I deploy and secure a Linux VM in Microsoft Azure using NSG (Network Security Groups) and centralized logging with Log Analytics.  The goal of the lab is to simulate a basic cloud environment and apply security best practices such as restricted SSH access and monitoring.

Simulated Scenario:
The virtual machine, which was exposed to the internet, was secured by restricting SSH access and enabling logging to detect unauthorized access attempts.

********************************************************************************************************************
Architecture:

    Platform: Azure
        Resource Group

            Virtual Network (VNet)

                App Subnet

            NSG (Network Security Groups)

                SSH access is restricted to my IP address

            Linux VM (Ubuntu)

                Nginx web server

            Log Analytics Workspace
********************************************************************************************************************

Security Configuration:
SSH access aws restricted to a single IP address (mine)
NSG inbound rule allowing only port 22
Public IP used temporarily for access
Logging enabled via Azure Log Analytics

Mishaps:
Trouble connecting the Log Analytics Workspace with the VM. (Unresolved)

What worked:
I managed to successfully connect via SSH
Verified web server access via Nginx

Skills demonstrated in the lab:
Azure networking (VNet, Subnets)
NSG (Network Security Groups)
Linux VM management
Webserver deployment (Nginx)

Improvements to the lab:
Remove public IP and use Azure Bastion, add NSG flow logs for traffic analysis, integrate Microsoft Defender for Cloud, and store secrets in Azure Key Vault
