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

- IIS and IIS Management Services
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- C++ Redistributable
- MySQL
- HeidiSQL
- osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/JpfDHG0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, install and enable IIS in Windows. Open Control Panel -> Programs -> Turn Windows Features on or off -> Internet Information Services. From here, enable Web Management Tools. Next, in the IIS dropdown, click on World Wide Web Services -> Application Development Features and enable CGI. Navigate back to World Wide Web Services, and open the Common HTTP Features tab and ensure all of the boxes are checked
</p>
<br />

<p>
<img src="https://imgur.com/Z7HMQ9F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To verify that IIS was installed correctly, open any browser and search 127.0.0.1. The result should look like the photo above.
</p>
<br />

<p>
<img src="https://imgur.com/axsIExC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, download all prerequisite files and create the directiory C:\php to unzip the contents of PHP 7.3.8 into. You will use a typical setup and standard configuration when installing MySQL. Make sure to take note of the password that is used here.
</p>
<br />

<p>
<img src="https://imgur.com/ZR9VA2t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, open IIS as an administrator. Register PHP by clicking on PHP Manager -> Register new PHP Version. Provide a path to the .exe file by going to C: -> php -> php-cgi.exe. Once that is done, reload the server by either clicking reload or clicking stop and start.
</p>
<br />

<p>
<img src="https://imgur.com/gMXgWQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket and copy the "upload" folder to c:\inetpub\root. Rename this new folder to "osTicket". Reload IIS, and from IIS, go to sites -> Default -> osTicket. Select "Browse *:80" and note that some extensions on the osTicket installer are disabled. To enable these, go back to IIS -> sites -> Default -> osTicket and double-click PHP Manager. Select "Enable or disable an extension", and enable php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket site in the browser and notice the changes.
</p>
<br />

<p>
<img src="https://imgur.com/i7JENHW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://imgur.com/0EF8yWD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, rename ost-sampleconfig.php to ost-config.php. To do this, open the C drive -> inetpub -> wwwroot -> osTicket -> include and rename the file. Change the file's permissions by right-clicking and selecting properties -> security -> advanced -> disable Inheritance -> Remove all. Then, add properties by clicking on add -> select principal and in the text box, type "Everyone" and click on search names. Give everyone Full Control, and select apply.
</p>
<br />

<p>
<img src="https://imgur.com/E2QhTfi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue setting up osTicket by clicking continue and filling in the name and email of your helpdesk as well as account information. Stop at the third section, and open HeidiSQL. Create a new session using the credentials from MySQL and create a new database called "osTicket".
</p>
<br />

<p>
<img src="https://imgur.com/nPz5rfe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue setting up osTicket in the browser by filling in the third row with the database, username, and password used and created in the last step.
</p>
<br />

<p>
<img src="https://imgur.com/pHQqknu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Assuming everything works, your screen should look like the photo above. Congratulations! You have successfully set up osTicket. To finish, change the permissions of C:\inetpub\wwwroot\osTicket\include\ost-config.php to "read only" and delete C:\inetpub\wwwroot\osTicket\setup.
</p>
<br />

<h2>🤳Connect with me:</h2>

[<img align="left" alt="Joseph | LinkedIn" width="22px" src="https://imgur.com/yJ22BHw.png" />][linkedin]
[<img align="left" alt="Joseph | Instagram" width="22px" src="https://imgur.com/JnlEgDK.png" />][instagram]
[<img align="left" alt="Joseph | Discord" width="22px" src="https://imgur.com/YGezWPR.png" />][discord]


[instagram]: https://www.instagram.com/jenkins5937/
[linkedin]: https://www.linkedin.com/in/joseph-jenkins-521a49241
[discord]: https://www.discordapp.com/users/262825628695396352
