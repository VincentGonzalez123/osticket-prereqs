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
<img src="https://i.imgur.com/84kdklz.jpg" height="80%" width="80%"/>
</p>
<br />

<h4>Install / Enable IIS in Windows WITH CGI</h4>

-	World Wide Web Services -> Application Development Features -> [X] CGI

- From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

- From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

- Create the directory C:\PHP

- From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
  - !! ATTENTION !!
 If this appears, choose to “Keep” the file:


<p>
<img src="https://i.imgur.com/0qgsz0t.png" height="50%" width="50%" />
<img src="https://i.imgur.com/jkKq9XG.png" height="50%" width="50%" />
</p>
<p>

<br />

 - From the Installation Files, download and install VC_redist.x86.exe.

 - From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
   - Typical Setup ->
   - Launch Configuration Wizard (after install) ->
   - Standard Configuration ->
   - Password1

 - Open IIS as an Admin

 - Register PHP from within IIS

 - Reload IIS (Open IIS, Stop and Start the server)

<p>
<img src="https://i.imgur.com/9Nzrzzi.png" height="80%" width="80%"/>
</p>

- Install osTicket v1.15.8
    - Download osTicket from the Installation Files Folder
    - Extract and copy “upload” folder to c:\inetpub\wwwroot
    - Within c:\inetpub\wwwroot, Rename “upload” to “osTicket"
    
- Reload IIS (Open IIS, Stop and Start the server)

- Go to sites -> Default -> osTicket
    - On the right, click “Browse *:80”
    
- Note that some extensions are not enabled

<p>
<img src="https://i.imgur.com/KGDGl3g.png" height="80%" width="80%"/>
</p>

- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
    - Enable: php_imap.dll
    - Enable: php_intl.dll
    -	Enable: php_opcache.dll

<p>
<img src="https://i.imgur.com/cK5fasE.png" height="80%" width="80%"/>
</p>

-	Refresh the osTicket site in your browse, observe the changes
<p>
<img src="https://i.imgur.com/6FmbQZn.png" height="80%" width="80%"/>
</p>

</p>


- Rename: ost-config.php
    - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
    - To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign Permissions: ost-config.php
    - Disable inheritance -> Remove All
    - New Permissions -> Everyone -> All
    
- Continue Setting up osTicket in the browser (click Continue)
    - Name Helpdesk
    - Default email (receives email from customers)

- From the Installation Files, download and install HeidiSQL.
    - Open Heidi SQL
    -	Create a new session, root/Password1
    - Connect to the session
    - Create a database called “osTicket”

- Continue Setting up osticket in the browser
    - MySQL Database: osTicket
    - MySQL Username: root
    - MySQL Password: Password1
    - Click “Install Now!”

<h4>Congratulations, hopefully it is installed with no errors!</h4>

- Browse to your help desk login page: http://localhost/osTicket/scp/login.php

<p>
<img src="https://i.imgur.com/fa1tAhH.png" height="80%" width="80%"/>
</p>

<br />
