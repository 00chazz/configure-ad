<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>

<h2>Overview</h2>
This project involved the deployment of an on-premises AD infrastructure within Microsoft Azure. Using VMs through Azure, this demonstrates extending traditional AD services to the cloud, providing scalable and robust identity management solutions.

- <h2>Environments and Technologies Used</h2>
- <b>Microsoft Azure:</b> Azure Virtual Machines </b>
- <b>Remote Desktop</b>
- <b>Active Directory Domain Services</b>
- <b>PowerShell</b>
- <b>Operating Systems: </b>
  - Windows Server 2022
  - Windows 10
- <h2>High-Level Deployment and Configuration Steps</h2>
1. <b>Prepare Azure environment: </b>
   - Set up Azure Virtual Machines for the domain controller and member servers.
2. <b>Install and Configure Active Directory: </b>
   - Install Active Directory Domain Services on the designated VM.
   - Promote the VM to a domain controller.
3. <b>Configure Networking and Firewall Settings: </b>
   - Adjust network settings to allow proper AD operations across the network.
4. <b>Validation and Testing: </b>
   - Perform system checks and validate AD functionalities within Azure.
  
- <h2>Detailed Deployment and Configuration Steps</h2>
1. <b>Azure Setup: </b>
   - Create Resource Groups:
     
   - Configure Virtual Network Settings:
  
2. <b>Active Directory Installation </b>
   - Install AD Domain Services on a new VM:
     
   - Promote the VM to a domain controller:
     
3. <b>Network Configuration </b>
   - Adjust DNS settings for AD operations:
  
   - Set up Firewall rules for secure AD communication:
  
4. <b>System Testing </b>
   - User Creation and Role Assignments:
     
   - Test Authentication and Authorization:

