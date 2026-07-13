<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This repository documents the setup and configuration of osTicket, an open‑source help desk system, deployed on an Azure Virtual Machine.
It focuses on installation, environment setup, and system configuration.<br />


<h2>🖥️ Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Windows 11 (4 vCPUs)
- osTicket v1.15.8


<h2>🎯 Purpose</h2>

Gain hands‑on experience with:
- Azure VM deployment
- IIS and PHP configuration
- Database setup and integration
- osTicket installation and initial configuration

<h2>Installation Steps</h2>

Step 1: Create Azure VM

Creating a Windows Virtual Machine through an Azure Subscription. 
- Name: osticket-vm
- OS: Windows 11
- Credentials: labuser / osTicketPassword1! (for lab use only)
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/5b382ca4-a27e-4a89-a700-25996200e2d3" />


<br />
<br />

Step 2: Install Requirements

We will first enable IIS with CGI through the Windows Control Panel. Then, after extracting the ZIP folder available on the OS's website, we will install the following items. 

- PHP Manager
- Rewrite Module
- VC Redistributable
- MySQL

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/0dcd30df-363b-4fe1-bd68-96d336468de6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/3f8068bf-c86e-4c7c-8f9a-8af9d261fc7f" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/e412b0a8-120b-4528-bc7b-f53d3df611a2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/c6742f4e-7dfe-41df-8846-9e02cde66fd1" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/159162a1-c57d-4e98-9685-af234a3ba754" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/138c1e87-586b-4cd8-9f77-9aa081a6c249" />

<br />
<br />


Step 3: Configure PHP and IIS


We will create a PHP Folder (C:\PHP) in Windows (C:) and unzip the PHP 7.3.8 files into this folder. Afterwards: 

- Open IIS as Administrator.
- Register PHP in IIS via PHP Manager → C:\PHP\php‑cgi.exe.
- Reload IIS (Stop and Start the server).
  
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/660e107b-d915-47c0-925d-190586a64c0e" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/b2f574f3-94d5-4f19-87cb-c0abe1499ac7" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/9ac0f390-aac7-4eeb-8496-b2ea035350c2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/03bf5b9d-2900-43bf-9650-389d7f70b402" />

  
<br />
<br />


Step 4: Install osTicket


After we unzip osTicket‑v1.15.8.zip from the osTicket‑Installation‑Files folder, we will: 

- Copy the upload folder into C:\inetpub\wwwroot.
- Rename upload to osTicket.
- Reload IIS (Stop and Start the server).
- Browse to http://localhost/osTicket to confirm the installation page loads.
  
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/026325db-c27e-41e7-8195-bfe763b12ef2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/1a8c284c-aedb-4084-baae-542f95f67ba6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/90d603e4-e6ca-4a70-b804-cba4218eaff3" />


<img width="1708" height="1070" alt="image" src="https://github.com/user-attachments/assets/429d6f9d-8c1e-4b06-b05c-2d776cd38786" />




<br />
<br />


Step 5: Post‑Installation Setup


After we unzip osTicket‑v1.15.8.zip from the osTicket‑Installation‑Files folder, we will: 

- Copy the upload folder into C:\inetpub\wwwroot.
- Rename upload to osTicket.
- Reload IIS (Stop and Start the server).
- Browse to http://localhost/osTicket to confirm the installation page loads.
  
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/026325db-c27e-41e7-8195-bfe763b12ef2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/1a8c284c-aedb-4084-baae-542f95f67ba6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/90d603e4-e6ca-4a70-b804-cba4218eaff3" />


<img width="1708" height="1070" alt="image" src="https://github.com/user-attachments/assets/429d6f9d-8c1e-4b06-b05c-2d776cd38786" />




You are now able to access the admin panel! 😊🎊
osTicket system complete! 🚀

<img src="https://i.imgur.com/PJI1207.png" height="60%" width="60%" alt=/>
