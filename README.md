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
- SSH access was restricted to a single IP address (my own).
- NSG inbound rule allowing only port 22 for administrative access.
- A public IP address was used temporarily for testing and access.
- Logging enabled via Azure Log Analytics.
- Nginx was installed to validate connectivity and exposed service behavior.

Challenges:
- I had trouble fully connecting the Log Analytics Workspace with the VM.
- Centralized logging was created, but VM-to-workspace integration remains unresolved.

What worked/Validation:
- I managed to connect via SSH successfully, using key-based authentication.
- Verified web server access via Nginx.
- Successfully deployed Azure VM. 
- NSG (Network Security Groups) configuration for SSH restriction.
- Successful creation of a Log Analytics Workspace.

Skills demonstrated in the lab:
- Azure networking (VNet, Subnets).
- NSG (Network Security Groups) and access control.
- SSH key-based authentication.
- Security-oriented cloud configuration.
- Linux VM management.
- Web server deployment (Nginx).

Improvements to the lab:
- Remove public IP and use Azure Bastion.
- Add NSG flow logs for traffic analysis.
- Integrate Microsoft Defender for Cloud.
- Store secrets in Azure Key Vault.

Tools Used:
- Microsoft Azure
- Ubuntu Linux
- Nginx
- SSH
- Azure Network Security Groups
- Azure Log Analytics
