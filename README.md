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
<p>
<img src="https://i.imgur.com/ZgRFUve.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Install and enable IIS (Internet Information Services) on Windows.
Go to World Wide Web Services, Application Development Features, and enable the CGI feature.

</p>
<br />
Item 2:
<p>
<img src="https://i.imgur.com/fy1PTju.png" height="60%" width="60%" alt=/>
<img src="https://i.imgur.com/LK1agin.png" height="60%" width="60%" alt=/>
<img src="https://imgur.com/QF8clgs" height="60%" width="60%" alt=/>
<img src="https://imgur.com/Y662nUV" height="60%" width="60%" alt=/>
<img src="https://i.imgur.com/QQp3lL0.png" height="60%" width="60%" alt=/>
<img src="https://i.imgur.com/jaDUQbX.png" height="80%" width="60%" alt=/>  
</p>
<p>
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
