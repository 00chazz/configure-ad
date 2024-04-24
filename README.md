# On-premises Active Directory Deployed in Azure

## Overview
This project involves deploying an on-premises Active Directory (AD) infrastructure within Microsoft Azure. Utilizing Azure Virtual Machines, this demonstration extends traditional AD services to the cloud, providing scalable and robust identity management solutions.

## Environments and Technologies Used
- **Microsoft Azure**: Virtual Machines (VMs)
- **Remote Desktop**
- **Active Directory Domain Services**
- **PowerShell**
- **Operating Systems Used**:
  - Windows Server 2022
  - Windows 10

## High-Level Deployment and Configuration Steps
1. **Prepare Azure Environment**:
   - Set up Azure Virtual Machines for the domain controller and member servers.
2. **Install and Configure Active Directory**:
   - Install Active Directory Domain Services on the designated VM.
   - Promote the VM to a domain controller.
3. **Configure Networking and Firewall Settings**:
   - Adjust network settings to ensure proper AD operations across the network.
4. **Validation and Testing**:
   - Perform system checks and validate AD functionalities within Azure.

## Detailed Deployment and Configuration Steps

### Step 1: Azure Setup
- **Create Resource Groups**:
  - Navigate to the Azure portal and create a new resource group by selecting Resource groups -> Add. Provide a name and select the region that matches your requirements.
  - **Screenshot**: Capture the Azure portal screen showing the newly created resource group with its name and location.

- **Configure Virtual Network Settings**:
  - In the same resource group, create a virtual network by selecting Virtual networks -> Add. Define the subnet details and ensure it is properly linked to the created resource group.
  - **Screenshot**: Display the virtual network settings with the subnet configuration.

### Step 2: Active Directory Installation
- **Install AD Domain Services on a New VM**:
  - Create a new VM within your resource group. During the VM setup, select the image for Windows Server 2022 and ensure that it includes the AD Domain Services role.
  - **Screenshot**: Take a screenshot of the VM overview page showing the Windows Server 2022 operating system and the role as AD Domain Services.

- **Promote the VM to Domain Controller**:
  - After the VM deployment, connect to the VM using Remote Desktop. Open Server Manager, go to Roles and Features, and promote the server to a domain controller.
  - **Screenshot**: Capture the final screen of the Active Directory Domain Services Configuration Wizard showing the successful promotion.

### Step 3: Network Configuration
- **Adjust DNS Settings for AD Operations**:
  - Configure the DNS settings within the VM to ensure all domain requests are properly routed. This is done through the network interface settings.
  - **Screenshot**: Show the DNS configuration within the network settings of the Azure VM.

- **Set Up Firewall Rules for Secure AD Communication**:
  - Configure the necessary firewall rules to allow AD communications. This typically involves allowing LDAP, Kerberos, and DNS protocols through the Windows Firewall.
  - **Screenshot**: Capture the Windows Firewall settings showing the rules for Active Directory.

### Step 4: System Testing
- **User Creation and Role Assignments**:
  - Create a test user in Active Directory Users and Computers snap-in. Assign a role and verify group membership.
  - **Screenshot**: Take a screenshot of the new user account properties dialog box showing the assigned groups and roles.

- **Test Authentication and Authorization**:
  - Log in using the test user account via Remote Desktop or another authentication method to verify correct setup.
  - **Screenshot**: Capture the successful login attempt, possibly showing the user desktop or a logged event in the event viewer.


## Conclusion
Deploying an Active Directory on Azure offers a scalable, secure, and robust platform for managing identities in a cloud environment. This project showcases the integration of traditional IT systems with modern cloud infrastructure, providing a foundation for hybrid identity solutions.

## Connect with Me
- *LinkedIn:* [https://www.linkedin.com/in/chazz-c-382a75122/](#)
