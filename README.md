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
  - Instructions on how to create and configure Azure resource groups. 
  - *Screenshot: Resource group configuration.*

- **Configure Virtual Network Settings**:
  - Detailed steps for setting up a virtual network in Azure.
  - *Screenshot: Virtual network setup.*

### Step 2: Active Directory Installation
- **Install AD Domain Services on a New VM**:
  - Steps for installing AD DS on a VM in Azure.
  - *Screenshot: Installation process.*

- **Promote the VM to Domain Controller**:
  - Instructions on promoting the VM to act as a domain controller.
  - *Screenshot: Promotion to domain controller.*

### Step 3: Network Configuration
- **Adjust DNS Settings for AD Operations**:
  - How to configure DNS settings for your AD domain.
  - *Screenshot: DNS configuration.*

- **Set Up Firewall Rules for Secure AD Communication**:
  - Steps to configure firewall rules to secure communication between AD components.
  - *Screenshot: Firewall settings.*

### Step 4: System Testing
- **User Creation and Role Assignments**:
  - Procedure for creating users and assigning roles in AD.
  - *Screenshot: User creation and role assignment.*

- **Test Authentication and Authorization**:
  - Steps to verify correct authentication and authorization processes.
  - *Screenshot: Testing authentication.*

## Conclusion
Deploying an Active Directory on Azure offers a scalable, secure, and robust platform for managing identities in a cloud environment. This project showcases the integration of traditional IT systems with modern cloud infrastructure, providing a foundation for hybrid identity solutions.

## Connect with Me
- *LinkedIn:* [https://www.linkedin.com/in/chazz-c-382a75122/](#)
