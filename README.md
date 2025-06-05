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

**Intillation files needed for osTicket**

[osTicket Releases](https://github.com/osTicket/osTicket/releases)

[HeidiSQL 12.3.0.6589](https://www.npackd.org/p/heidisql/12.3.0.6589)

[MySQL Community Server 5.5.62](https://www.npackd.org/p/com.mysql.MySQLCommunityServer/5.5.62)

[Latest PHP for Windows](https://windows.php.net/downloads/releases/latest/)

[PHP Manager 1.5.0 for IIS 10](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10)

[URL Rewrite for IIS](https://www.iis.net/downloads/microsoft/url-rewrite)

[Microsoft Visual C++ Redistributable 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48145)
</p>

  <img src="https://i.imgur.com/AO9Uq0j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>  
  
**Enabling IIS and CGI on Windows**

**1.Open the Control Panel.**

**2.Navigate to Programs > Programs and Features.**

**3.Click Turn Windows features on or off (on the left panel).**

**4.In the window that appears, scroll down and check the box for Internet Information Services (IIS).**

**5.Expand the Internet Information Services section by clicking the plus sign or arrow.**

**6.Expand World Wide Web Services > Application Development Features.**

**7.Check the box for CGI.**

**8.Click OK to apply the changes.** 

<p>
</p>
<img src="https://i.imgur.com/GsfGXep.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<p>



</p>
<br />

<h2>Installation Steps</h2>

**1. Run PHPManagerForIIS_V1.5.0 to install PHP Manager for IIS.**

**2. After that, run rewrite_amd64_en-US to install the IIS URL Rewrite Module.**
</p>
<br />
<img src="https://i.imgur.com/AO9Uq0j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**Create a directory C:\PHP**
</p>
<br />
<img src="https://i.imgur.com/Erj5REY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**1.Right-click the ZIP file and choose “Extract All...”**

**2.Set the destination folder to C:\PHP and extract the files there.**

</p>
<br />
<img src="https://i.imgur.com/cimO4NA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**Install VC_redist.x86**

</p>
<br />
<img src="https://i.imgur.com/AO9Uq0j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**Install MySQL 5.5.62 using the installer mysql-5.5.62-win32**

**On the first and second windows, click next.**



</p>
<br />
<img src="https://i.imgur.com/X5oZZFh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<br />
<img src="https://i.imgur.com/FmQZEYe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**On the third window, select "Typical Setup."**

**Then select install**

</p>
<br />
<img src="https://i.imgur.com/8GAUk1c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

**After the installation completes, launch the MySQL Configuration Wizard.**

**Select Standard Configuration.**

**Set a username and a password.**

</p>
<br />
<img src="https://i.imgur.com/6uEkKyj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/t6D92Kg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/poMWWFg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
