<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Tenant or subscription
- osTicket Installation Files: 
https://drive.google.com/drive/u/0/folders/1yOJcSZyWcX4HeN3-w3MDfObmSkPKzFbY

<h2>Installation Steps</h2>

- Create an Azure Virtual Machine Windows 10, 4 vCPUs
  1.	When creating the VM, allow it to create a new Virtual Network (Vnet)
-	Name: Vm-osticket
-	Username: labuser (for example/whatever you chose)
-	Password: osTicketPassword1! (for example/whatever you chose)

<p>
<img src="https://i.imgur.com/84kdklz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h4>Install / Enable IIS in Windows WITH CGI</h4>

-	World Wide Web Services -> Application Development Features -> [X] CGI

- From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

- From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

- Create the directory C:\PHP

- From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
