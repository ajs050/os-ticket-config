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
- Windows 10 (4 vCPUs)
- osTicket v1.15.8


<h2>🎯 Purpose</h2>

Gain hands‑on experience with:
- Azure VM deployment
- IIS and PHP configuration
- Database setup and integration
- osTicket installation and initial configuration

<h2>Installation Steps</h2>

Step 1: Create Azure VM
- Name: osticket-vm
- OS: Windows 10
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

Configure PHP and register it in IIS

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/0dcd30df-363b-4fe1-bd68-96d336468de6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/3f8068bf-c86e-4c7c-8f9a-8af9d261fc7f" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/e412b0a8-120b-4528-bc7b-f53d3df611a2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/c6742f4e-7dfe-41df-8846-9e02cde66fd1" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/159162a1-c57d-4e98-9685-af234a3ba754" />


From the osTicket-Installation-Files folder:

  Install PHP Manager for IIS
Install the Rewrite Module 
Create the directory: C:\PHP.
Extract the PHP 7.3.8 into C:\PHP.
Install the Visual C++ Redistributable
Install MySQL 5.5.62 with: Typical Setup, then standard configuration, then apply username and password. 🧑‍💻

</p>
<br />
Item 3:
<p>
<img src="https://i.imgur.com/Y662nUV.png" height="60%" width="60%" alt=/>  
  
</p>
<p>
We will open IIS as Administrator.
Register PHP in IIS (PHP Manager → Register New PHP Version → C:\PHP\php-cgi.exe).
Restart IIS (Stop and Start the server).
</p>
<br />
Item 4:
<p>
<img src="https://i.imgur.com/bO1OGqH.png" height="60%" width="60%" alt=/>  
<img src="https://i.imgur.com/63te02v.png" height="60%" width="60%" alt=/>

</p>
<p>
From the osTicket-Installation-Files folder:

To install osTicket we must now extract osTicket-v1.15.8.zip.
Copy the upload folder to C:\inetpub\wwwroot.
Rename the upload folder to osTicket. 🚀
Restart IIS again.
</p>
<br />
<p>
<img src="https://i.imgur.com/XunS4np.png"60%" width="60%" alt=/>  
<img src="https://i.imgur.com/pWkUiLR.png" height="60%" width="60%" alt=/>

</p>
<p>

We will now set Up Configurations for mySQL and osTicket

Rename the sample configuration file:
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Update permissions for ost-config.php:
Disable inheritance, remove all existing permissions
<p>

  Item 5: 

<img src="https://i.imgur.com/N5PdxII.png" height="60%" width="60%" alt=/>

</p>
<p>
Complete the osTicket Setup in the Browser.

Open the osTicket setup page in your browser.
Provide the following: Helpdesk name, default email for customer queries.👌

Item 6:

<img src="https://i.imgur.com/ZyRfSaw.png" height="60%" width="60%" alt=/>

Install and open HeidiSQL.
Create a new session (Username: root, Password: root) 
Connect and create a new database named osTicket.
Return to the browser setup and input:
Database Name: osTicket

You are now able to access the admin panel! 😊🎊
osTicket system complete! 🚀

<img src="https://i.imgur.com/PJI1207.png" height="60%" width="60%" alt=/>
