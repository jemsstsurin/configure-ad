<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory
- Set up a Domain Controller (DC)
- Promote a Server to a Domain Controller
- Group Policy Management Configuration

<h2>Deployment and Configuration Steps</h2>


![image](https://github.com/user-attachments/assets/d0ffeca7-3c14-4460-999e-1e7255718403)
![image](https://github.com/user-attachments/assets/0b5f8c85-598b-4381-b1bb-a2dc946560d9)


<p>
To install Active Directory you first got to Server Manager. Then you got to Add Roles and Features. Next in Server Roles you are going to install Active Directory Domain and Services. Then click next until your see Install then click it.
</p>
<br />

![image](https://github.com/user-attachments/assets/47d6acb7-88b4-4625-bd7d-46c6f263c015)
![image](https://github.com/user-attachments/assets/8e133e83-2d76-48cc-9911-94207c68f335)
![image](https://github.com/user-attachments/assets/3d0de934-6362-4185-9cca-6a86533f9925)



<p>
To setup domain controller you first need to click the flag icon on the top right and click "Promote this server to a domain controller". Then click "Add a new forest" and in "root domain name" put mydomain.com then click Next. On the Domain Control Option page you just put your password and click Next until you reach the "Prerequisite Check" page then press Install then your computer will Restart.
</p>
<br />

![image](https://github.com/user-attachments/assets/c7618e04-9cf6-46f4-a069-25a4379bcca4)

![image](https://github.com/user-attachments/assets/a6da2515-2529-4615-a1e9-0797ada17e77)

![image](https://github.com/user-attachments/assets/4fa816a2-cce4-4c34-807f-d8f7566b96c2)



<p>
To open the Group Policy Management Console click Start, and type gpmc.msc in the search box, then press Enter. In the GPMC, navigate to the Group Policy Objects section. Then Right-click Group Policy Objects and select New to create a new GPO, or right-click an existing GPO and select Edit to modify it. In the Group Policy Management Editor, expand the following:
Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy. And there you can Configure Account Lockout Policy Settings such as (Account Lockout Duration, Account Lockout Threshold, and Reset Account Lockout Counter After.
</p>
<br />
