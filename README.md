<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Prerequisites</h2>

- Installation Files from: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/oHsLR36.png" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs
</p>
<br />

<p>
<img src="https://i.imgur.com/Dkf09PC.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install/Enable IIS in Windows with CGI and Common HTTP and IIS Management Console
</p>
<br />

<p>
<img src="https://i.imgur.com/YZXWj8C.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation files, download and install PHP Manager for IIS: PHPManagerForIIS_V1.5.0.msi
</p>
<br />

<p>
<img src="https://i.imgur.com/eT4TRR7.jpg" height="100%" width="100%" alt="Rewrite Module 2 Installation"/>
</p>
<p>
From the installation files, download and install the Rewrite Module: rewrite_amd64_en-US.msi
</p>
<br />

<p>
<img src="https://i.imgur.com/3JNDMYl.png" height="100%" width="100%" alt="PHP Installation"/>
</p>
<p>
Create the directory C:\PHP and then from the installation files, download PHP 7.3.8 and unzip the contents into C:\PHP. If prompted, select "keep" and "keep anyway."
</p>
<br />

<p>
<img src="https://i.imgur.com/VgcOipr.png" height="100%" width="100%" alt="C++ Installation"/>
</p>
<p>
From the Installation Files, download and install VC_redist.x86.exe
</p>
<br />

<p>
<img src="https://i.imgur.com/AzcEPep.png" height="100%" width="100%" alt="MySQL Installation"/>
</p>
<p>
From the Installation Files, download and install MySQL 5.5.62. Typical Setup --> Launch Configuration Wizard after installation --> Standard Configuration --> Set the password.
</p>
<br />

<p>
<img src="https://i.imgur.com/z0BDvSw.png" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Open IIS as an Admin. Register PHP from within IIS. Reload IIS by restarting the server from within IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/bNlbsOn.png" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Download osTicket from the Installation Files | Extract and copy the "upload" folder to C:\inetpub\wwwroot | Rename the "upload" folder to "osTicket"
</p>
<br />

<p>
<img src="https://i.imgur.com/PX84dzh.jpg" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Go to sites --> Default --> osTicket. On the right, click "Browse *:80" | Note that some extensions are not enabled. Go back to IIS, sites --> Default --> osTicket. Double-click PHP Manager. Click “Enable or disable an extension.” Enable: php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket site in your browse, and observe the changes.
</p>
<br />

<p>
<img src="https://i.imgur.com/RJgQYly.jpg" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Rename: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php --> C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/My9zymD.png" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Assign Permissions: ost-config.php | Disable inheritance --> Remove All | New Permissions --> Everyone --> All | Continue setting up osTicket in the browser: click Continue, name the Helpdesk and default email
</p>
<br />

<p>
<img src="https://i.imgur.com/ArGaetw.jpg" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
From the Installation Files, download and install HeidiSQL | MySQL Database: osTicket | MySQL Username: root | Set the Password | Click Install Now
</p>
<br />

<p>
<img src="https://i.imgur.com/K9JGopF.jpg" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Congratulations, hopefully, it is installed with no errors! | Helpdesk Login Page: http://localhost/osTicket/scp/login.php | End Users osTicket URL: http://localhost/osTicket/
</p>
<br />

<p>
<img src="https://i.imgur.com/ZQUvEBe.png" height="100%" width="100%" alt="Azure VM"/>
</p>
<p>
Delete: C:\inetpub|wwwroot\osTicket\setup | Set Permissions to "Read" only for C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />
