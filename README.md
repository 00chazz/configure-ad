# On-premises Active Directory Deployed in Azure

## Overview
This comprehensive project involves deploying an on-premises Active Directory (AD) infrastructure within Microsoft Azure. This setup demonstrates extending traditional AD services to the cloud, ensuring scalable and secure identity management solutions using Azure Virtual Machines.

## Environments and Technologies Used
- **Microsoft Azure**: Virtual Machines (VMs), Virtual Networks
- **Remote Desktop**
- **Active Directory Domain Services**
- **PowerShell**
- **Operating Systems Used**:
  - Windows Server 2022 (Domain Controller)
  - Windows 10 (Client Machine)

## High-Level Deployment and Configuration Steps
1. **Prepare Azure Environment**:
   - Set up Azure Virtual Machines for the domain controller and member servers within the same virtual network.
2. **Install and Configure Active Directory**:
   - Install Active Directory Domain Services on the designated domain controller VM and promote it.
3. **Configure Networking and Firewall Settings**:
   - Adjust DNS and firewall settings to support AD operations.
4. **Validation and Testing**:
   - Test connectivity and authentication across domain-joined machines.

## Detailed Deployment and Configuration Steps

### Step 1: Azure Setup
- **Create Resource Groups and Virtual Network**:
  - Create a new resource group and virtual network in Azure. Set up two VMs (DC-1 for Domain Controller and Client-1 for client operations) within this network.
  - Here is all of our resources within our resource group: ![image](https://github.com/00chazz/configure-ad/assets/63687898/eeb0ff50-74ef-43da-9688-24b72bb8c176)

<br />

### Step 2: Active Directory Installation
- **Install and Promote Active Directory Domain Services**:
  - Install AD DS on DC-1, set up a new forest (e.g., `mydomain.com`), and promote it to a domain controller.
  - After deploying, we can promote it to a domain controller:
    ![image](https://github.com/00chazz/configure-ad/assets/63687898/5c5c56f2-e75a-43c7-944f-b163acb6cb70)

<br />

- **Network Configuration and Connectivity**:
  - Ensure both VMs are in the same Vnet. From Client-1, verify connectivity by pinging DC-1.
  - Successful ping results from Client-1 to DC-1 after enabling ICMP through firewall:
    ![image](https://github.com/00chazz/configure-ad/assets/63687898/52f38d10-3b4e-474e-955b-1741e8578c00)

<br />

### Step 3: User and Computer Management
- **Organizational Units and User Setup**:
  - Create organizational units (OUs) in AD for employees and admins. Create user accounts, including an administrative account (`john_admin`).
  - Employee and admin OUs are created, with new user john_admin in the Domain Admins group:.![image](https://github.com/00chazz/configure-ad/assets/63687898/6dfccff2-aac1-4d56-bfb4-d889b6562e08)

<br />

- **Join Client VM to Domain and Test Remote Desktop**:
  - Adjust Client-1’s DNS settings to point to DC-1. Join Client-1 to `mydomain.com` and verify its appearance in ADUC under the Computers container.
  - Client-1 was added to the domain, and does indeed appear in ADUC:![image](https://github.com/00chazz/configure-ad/assets/63687898/1bad10e3-4121-465b-9850-3a15c484ef9e)

<br />

### Step 4: System Testing and Policy Implementation
- **Remote Desktop Configuration**:
  - Configure remote desktop settings on Client-1 to allow access for domain users.
  - The system properties window showing Domain Users can access the CLient-1 desktop: ![image](https://github.com/00chazz/configure-ad/assets/63687898/59830771-fdbc-4b8c-ad7e-9c15a35c788f)


<br />

- **User Login Tests**:
  - Create additional users using a PowerShell script and test logging into Client-1 with these accounts.
  - Users being created, and successfull login with random user "kof.vehi":
     ![image](https://github.com/00chazz/configure-ad/assets/63687898/74fdc050-5d0c-4def-8932-0f6afac3aa10)
   ![image](https://github.com/00chazz/configure-ad/assets/63687898/9ed4ecd4-2ddb-43df-b08c-636dfa04da73)



<br />

## Conclusion
Deploying an Active Directory on Azure provides a robust platform for managing organizational identities and enhances security through centralized administration. This demonstrates integration of traditional IT systems with advanced cloud infrastructure and creating a dynamic environment suitable for modern business needs.

## Connect with Me:
- *LinkedIn:* [Chazz Conino](https://www.linkedin.com/in/chazz-c-382a75122/)
