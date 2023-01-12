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
-Install or enable Internet Information Services

-Add MySQL 5.5

-Add all the simple versions of x86 PHP up to version 7.3

-Install osTicket version 1.15.8

-Restart IIS by opening it and stopping and starting the server

-Enable the required extensions in IIS

-Refresh the osTicket site in your browser to observe the changes

-Clean up files for optimal performance.


<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/kZYYuqn.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> 
  To set up IIS(Internet Information Services), first open the control panel. This will enable a web server on your computer, allowing you to run osTicket from the web. To access the control panel, simply search for it using the search bar located at the bottom of your desktop.
</p>
<br />
<p>
<img src="https://imgur.com/tWT3XK1.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the Programs menu and choose the option to uninstall a program.
</p>
<br />
<img src="https://imgur.com/Ap4P73j.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When you are on the "uninstall or change a program" screen, look for the option "Turn Windows features on or off" on the left side. 
</p>
<br />
<p>
<img src="https://imgur.com/ui6rnJZ.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the dialog box, select the Internet Information Services option and click Ok.
</p>
<br />
<p>
<img src="https://imgur.com/H9TBoFb.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After installing IIS, search for the Microsoft Web Platform Installer online and download it. This extension is required to install the remaining software necessary for osTicket.
</p>
<br />

<h3>Add MySQL 5.5</h3>
<p>
<img src="https://i.imgur.com/THXv7zF.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Add all simple versions of x86 PHP up to v7.3</h3>

<p>
<img src="https://i.imgur.com/X7Fu35v.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search for the "Web Platform Installer" online and install it. Once it is open, use the dialog box to search for "MySQL 5.5" and add it. Also, search for all versions of (x86) PHP up to 7.3 and add them as well. 
</p>
<br />
<p>
<img src="https://i.imgur.com/gWpbvb3.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When prompted, create a username and password to complete the installation.
</p>
<br />
<p>
<img src="https://i.imgur.com/HTBMgNO.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The web installer will try to complete the installation of all the prerequisites that are selected. Some of the downloads may not succeed, so you will need to manually download the C++ redistributable and PHP Manager from online sources. Proceed with the installation. Locate and install PHP Manager version 7.3.8 
</p>
<br />
<p>
<img src="https://i.imgur.com/Pkh9Y3s.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Microsoft Visual C++ 
</p>
<br />
<p>
<img src="https://i.imgur.com/xcIWPE5.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager
</p>
<br />

<h3>Install osTicket v1.15.8</h3>

<p>
<img src="https://i.imgur.com/eqFSUiY.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At this point, any installation errors should be resolved. Download and then extract the OsTicket software zip file before installing it. 
</p>
<br />
<p>
<img src="https://i.imgur.com/UPXpiYv.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After OsTicket has been installed, go to the download folder, copy it and paste it into the wwwroot folder that was created by IIS. Rename the folder from "upload" to "osTicket" and the file path should be: This PC/Windows (C:)/inetpub/wwwroot.
</p>
<br />
<p>
<img src="https://i.imgur.com/mzNsDKY.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename the upload folder to osTicket in the wwwroot folder
</p>
<br />

<h3>Reload IIS (open IIS, Stop and Start the server)</h3>

<p>
<img src="https://i.imgur.com/oXT19Dq.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To access IIS, go to the taskbar and type IIS in the search bar, then open the program. In order to restart the web server, navigate to the "Connections" folder, select the "browse 80" folder, then go to "Sites" -> "osTicket" -> "browse80" and select "stop" then "restart
</p>
<br />


<p>
<img src="https://i.imgur.com/5gIVfsA.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If the program was installed correctly, you will see a prerequisite screen. If not, please go back and check if any extensions like PHP, C++, or PHP Manager are missing and install them. Now, we will proceed to enable the extensions. 
</p>
<br />

<h3>Enable extensions in IIS</h3>

<p>
<img src="https://i.imgur.com/udxfNHH.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To proceed, enable the following extensions: php_imap.dll, php_intl.dll, and php_opcache. Once you have done that, refresh the osTicket site and observe the changes. 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/9Jyrbzi.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to C:-->inetpub-->wwwroot-->osTicket-->include. Once there, right-click on the ost-sampleconfig.php file and rename it to ost-config.php.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/uZR6cvY.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next Enable automatic permissions for everyone, right-click on the file, select Properties, then Advanced. Disable inheritance and in the next dialog box, type "everyone". Select the "Full Access" radio button, then click Apply and Ok
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/8fczdiw.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL which will allow osTicket to connect to the MySQL database installed earlier. Take note of username and password used to install MySQL 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/EP3idvb.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In order to create a new database, you will need the username and password that was used to install MySQL. To create a new database, right-click on SSS, select New, then Database. Name the new database "osTicket" and click Ok.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/KWNWOKb.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In your browser tab, navigate to the osTicket installer and fill out the information in the following fields: System Settings, Admin User, and Database Settings. Once you have completed this, click on "Install Now" 
</p>
<br />

<h3>Refresh the osTicket site in your browser and observe the changes</h3>

<p>
<img src="https://i.imgur.com/8G89n6U.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This screen will show a successful installation of osTicket
</p>
<br />
<h3>Clean up files for optimal use</h3>

<p>
<img src="https://i.imgur.com/KTZ9fhl.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, to avoid any future performance issues with osTicket, we will clean up some files during the installation process. Go to C:-->inetpub-->wwwroot-->osTicket and delete the setup file.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/nacJmFL.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to C:-->Inetpub-->wwwroot-->osTicket-->include, right click on ost-config.php and select security tab, then advanced. Click on edit to change permissions for everyone, allowing only read & execute by deselecting the other radio buttons. Click on apply and Ok.
