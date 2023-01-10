# <p align="center">
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

- Windows 10 VM in Azure
- RDP
- os Ticket
- enable IIS
- PHP manager for IIS
-  MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/CfitwNr.png" height="80%" width="80%" alt="osticket to root file"/>
</p>
<p>
After Fulfilling the prerequisties you would then have to download the osTicket software and click on the zipfile, which you would then extract and copy the upload folder to c:\inetpub\wwwroot, and rename it osTicket. You would then reload IIS and go to sites, to the default, and you will find OsTicket.
 
</p>
<br />

<p>
<img src="https://i.imgur.com/cCxvpXp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you would go on the right and click on browse .80 and this will take you to the osTicket website you have now created
</p>
<br />

<p>
<img src="https://i.imgur.com/XHvNJgV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Note that some extensions arent enabled so we will now go back to IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/msFHN72.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In IIS we will double click on PHP manager. then we will click on "enable or disable an extension" which will take us here, in here we can enable the required extensions which are: Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
  we will also rename a file called ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php in that folder, then we will go to the properties of that file, under security, then advanced and we will disable the inheritance and grant new permissions to everyone so they are all able to use the software. After all that is done we will go back to the site and fill out all the info except for the SQL database server which we have to install.

</p>
<br />
<p>
<img src="https://i.imgur.com/WPYnTq2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we install Heidi SQL we will create and then connect to the session using the information we used when installing My SQL 5.5.62, and we will create a database called "osticket"
</p>
<br />

<p>
<img src="https://i.imgur.com/fuIUXZP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well fill out the info from the SQL server on the osTicket site and osticket is now setup, all that remains is some cleanup in which we Delete: C:\inetpub\wwwroot\osTicket\setup, and we will also Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php. After that osTicket is setup and we can start resolving tickets/
</p>
<br />



