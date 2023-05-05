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

<h2>List of Prerequisites</h2>

- Item 1: Enable IIS in Windows WITH CGI
- Item 2: PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Item 3: the Rewrite Module (rewrite_amd64_en-US.msi)
- Item 4: PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- Item 5: VC_redist.x86.exe.
- Item 6: MySQL 5.5.62 (mysql-5.5.62-win32.msi)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/aiTApGp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After I have downloaded and enabled or installed all of my pre-requisites with standard configurations. I now move on to the installation and set up of osTicket.
I have opened IIS as an Admin, Register PHP from within IIS and Reloaded IIS (Open IIS, Stop and ReStart the server). 
</p>
<br />

<p>
<img src="https://i.imgur.com/Hdd631A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I took the following steps to start installing osTIcket v1.15.8
A. Download osTicket from
B. Extract and copy “upload” folder to c:\inetpub\wwwroot
C. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket
</p>
<br />


<p>
<img src="https://i.imgur.com/s8yLk27.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/tQh4UTC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now back in IIS I went to 'sites', clicked on 'Default web store', then 'osTicket'. OsTicket then opened in the browser and observed that some extensions were not yet enabled. I have enabled the following extensions:php_imap.dll
php_intl.dll
php_opcache.dll
</p>
<br />

<p>
<img src="https://i.imgur.com/shMcMiG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then renamed the file C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to, C:\inetpub\wwwroot\osTicket\include\ost-config.php. I also set the permission on the file as to who can and cannot access this file. I have allowed "everyone" to access this file.
</p>
<br />

<p>
<img src="https://i.imgur.com/orB7Oke.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next I continued setting up osTicket in the browser, creating a name for my helpdesk and setting a default email I chose:Help desk name: Jecara Help deskDefault email (receives email from customers): jecara@helper.com.
</p>
<br />

<p>
<img src="https://i.imgur.com/M7g40Af.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then downloaded and installed HeidiSQL. After installation was completed, I opened HeidiSQL and created a new database called osTicket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/YmlyCr6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, I head back to the web browser with osTicket pulled up and continue setting up osTicket. I entered my new MYSQL database name"osTicket", MYSQL username and password. Finally I clicked "Install Now". I also did some cleaning up at the end of the installation, heading back to the osTicket folder in the C drive, I then deleted the set up folder. I've also set the Permissions to “Read” only in the same wroot folder.
</p>
<br />


<p>
<img src="https://i.imgur.com/abJr2d7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/aYVALSZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here is what the final osTicket help desk login page and the end users os Ticket page looks like in web browser
Jecara help desk login page: http://localhost/osTicket/scp/login.php
End Users osTicket URL: http://localhost/osTicket/.
</p>
<br />
