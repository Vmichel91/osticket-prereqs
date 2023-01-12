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

- Add Internet Information Services
- Add MySQL 5.5
- Add all simple versions of x86 PHP up to v7.3
- Install osTicket v1.15.8
- Reload IIS (open IIS, Stop and Start the server) 
- Enable extensions in IIS
- Refresh the osTicket site in your browser and observe the changes
- Clean up files for optimal use

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/kZYYuqn.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> Step 1
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
<img src="https://i.imgur.com/THXv7zF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Add all simple versions of x86 PHP up to v7.3</h3>

<p>
<img src="https://i.imgur.com/X7Fu35v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search the web and install: "Web Platform Installer" & open "Web Platform Installer". In the dialog box, search Web Platform Installer to add "MySQL 5.5" & search to add all simple versions of (x86) PHP up until 7.3. 
</p>
<br />
<p>
<img src="https://i.imgur.com/gWpbvb3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a username and password when asked to finish installation. 
</p>
<br />
<p>
<img src="https://i.imgur.com/HTBMgNO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Web installer will attempt to finish installing all of the prerequistes that are checked (some of the downloads will fail, just manually download C++ redistribuable & PHP Manager via files found online). Continue to finish with installation. Find and install "PHP Manager" version 7.3.8 & version 1.5.0.
</p>
<br />
<p>
<img src="https://i.imgur.com/Pkh9Y3s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Microsoft Visual C++ 
</p>
<br />
<p>
<img src="https://i.imgur.com/xcIWPE5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager
</p>
<br />

<h3>Install osTicket v1.15.8</h3>

<p>
<img src="https://i.imgur.com/eqFSUiY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Installation errors should be fixed at this point.  Download and install the osTicket software.  You will need to extract the zip file once downloaded. 
</p>
<br />
<p>
<img src="https://i.imgur.com/UPXpiYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once osTicket has been installed, open the download folder and copy it into your wwwroot folder that was created from IIS and rename the folder from upload to osTicket. filepath ThisPC/Windows (C:)/inetpub/wwwroot
</p>
<br />
<p>
<img src="https://i.imgur.com/mzNsDKY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename the upload folder to osTicket in the wwwroot folder
</p>
<br />

<h3>Reload IIS (open IIS, Stop and Start the server)</h3>

<p>
<img src="https://i.imgur.com/oXT19Dq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to -->Taskbar-->Type IIS in the searchbar and open the program-->You will need to restart the web server by selecting the browse 80 folder in the connections folder. -->Sites-->osTicket-->browse80-->stop-->restart
</p>
<br />


<p>
<img src="https://i.imgur.com/5gIVfsA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If the program was properly installed, you will see this prerequesite screen.  If not, please go back and install the missing php, C++, or php manager.  We will now enable eextensions. 
</p>
<br />

<h3>Enable extensions in IIS</h3>

<p>
<img src="https://i.imgur.com/udxfNHH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable the following extenions, php_imap.dll, php_intl.dll, and php_opcache.  Please refresh the osTicket site and oberve the changes. 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/9Jyrbzi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:-->inetpub-->wwwroot-->osTicket-->include and right-click the ost-sampleconfig.php file and rename it to ost-config.php
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/uZR6cvY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable automatic permissions for everyone in this file by right-clicking on the file and select -->Properties-->Advanced-->Disable inheritance-->type everyone in the next dialog box-->selct the Full Access radio button-->Select the Apply button-->Select the Ok button 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/8fczdiw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL for osTicket to have a client database that connects to MySQL that was installed previously. 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/EP3idvb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To create a database, you will need the username and password that was used to install MySQL.  Create a new database by right-clicking on SSS-->New-->Database-->> name your database osTicket and click Ok.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/KWNWOKb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to your osTicket installer in your browser tab and fill out the following information in the fields.  --> System Settings-->Admin User-->Database Settings--> Click on "Install Now" 
</p>
<br />

<h3>Refresh the osTicket site in your browser and observe the changes</h3>

<p>
<img src="https://i.imgur.com/8G89n6U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This screen will show a successful installation of osTicket
</p>
<br />
<h3>Clean up files for optimal use</h3>

<p>
<img src="https://i.imgur.com/KTZ9fhl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, we will clean up some files during installation to prevent future performance issues with osTicket. Go to your C:-->inetpub-->wwwroog-->osTicket and delete the setup file
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/nacJmFL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:-->Inetpub-->wwwroot-->osTicket-->inlclude and right click on ost-config.php and select securities tab-->advanced-->click edit to change permissions for everyone to only have read & execute by deselecting the radio buttons.  Click on apply-->Ok
