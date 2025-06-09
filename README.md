![osTicket logo](https://i.imgur.com/Clzj7Xs.png)

# osTicket - Prerequisites and Installation

This tutorial outlines the prerequisites and installation steps for the open-source help desk ticketing system **osTicket**.

---

## Environments and Technologies Used

* Microsoft Azure (Virtual Machines / Compute)
* Remote Desktop
* Internet Information Services (IIS)

## Operating System Used

* Windows 10 (21H2)

---

## Installation Files for osTicket

* [osTicket Releases](https://github.com/osTicket/osTicket/releases)
* [HeidiSQL 12.3.0.6589](https://www.npackd.org/p/heidisql/12.3.0.6589)
* [MySQL Community Server 5.5.62](https://www.npackd.org/p/com.mysql.MySQLCommunityServer/5.5.62)
* [Latest PHP for Windows](https://windows.php.net/downloads/releases/latest/)
* [PHP Manager 1.5.0 for IIS 10](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10)
* [URL Rewrite for IIS](https://www.iis.net/downloads/microsoft/url-rewrite)
* [Microsoft Visual C++ Redistributable 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48145)

---

## Enabling IIS and CGI on Windows

1. Open **Control Panel**.
2. Navigate to **Programs > Programs and Features**.
3. Click **Turn Windows features on or off**.
4. Scroll down and check **Internet Information Services (IIS)**.
5. Expand **Internet Information Services > World Wide Web Services > Application Development Features**.
6. Check the box for **CGI**.
7. Click **OK** to apply the changes.

![Enable IIS](https://i.imgur.com/GsfGXep.png)

---

## Installation Steps

### Step 1: Install PHP Manager and URL Rewrite Module

1. Run `PHPManagerForIIS_V1.5.0.msi` to install PHP Manager for IIS.
2. Run `rewrite_amd64_en-US.msi` to install the IIS URL Rewrite Module.

### Step 2: Install and Configure PHP

1. Create a folder at `C:\PHP`.
2. Download the ZIP file `php-7.3.8-nts-Win32-VC15-x86.zip`.
3. Right-click the ZIP file and select **Extract All...**
4. Extract the contents to `C:\PHP`.

![Extract PHP](https://i.imgur.com/Erj5REY.png)

### Step 3: Install Visual C++ Redistributable

* Install `VC_redist.x86.exe` from the official Microsoft website.

### Step 4: Install MySQL 5.5.62

1. Run `mysql-5.5.62-win32.msi`.
2. Click **Next** on the first and second screens.
3. Select **Typical Setup**, click **Next**, then click **Install**.

![MySQL Setup](https://i.imgur.com/8GAUk1c.png)

### Step 5: Configure MySQL

1. After installation, the **MySQL Configuration Wizard** should launch automatically. If not, launch it manually from the Start Menu.
2. On the welcome screen, click **Next**.
3. Select **Standard Configuration**, then click **Next**.
4. Leave the default settings and click **Next**.
5. When prompted:

   * Set the username to `root`.
   * Enter and confirm the password (e.g., `root`).
6. Click **Execute** to apply the configuration.

![MySQL Config Wizard](https://i.imgur.com/poMWWFg.png)

---

## Next Steps

* Install osTicket and configure it to connect to the MySQL database.
* Verify PHP is properly registered in IIS.
* Set file and folder permissions as required.

---

Open ISS as an admin click PHP manager from within ISS
</p>
<br />
<img src="https://i.imgur.com/zlAfhVj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Click register a new PHP version click on the three dot to browser to php-cgi within the C:/PHP folder double click it then click ok
 
</p>
<br />
<img src="https://i.imgur.com/zdhfcSG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now reastart the sever by clicking the first link on the left the restart on the right
</p>
<br />
<img src="https://i.imgur.com/bq3s4S6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we will install osTicket.
first, we will extract osTicket-v1.15.8.zip to a desired location
</p>
<br />
<img src="https://i.imgur.com/MvaApo4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now open the unzipped folder name osTicket-v1.15.8 you will see a upload folder you will copy the folder into C:\inetpub\wwwroot then remame the folder exacly osTicket cannot be name anhything diffently
</p>
<br />
<img src="https://i.imgur.com/8ZQwpNR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<img src="https://i.imgur.com/QkqPcOD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<img src="https://i.imgur.com/vXJTSHq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we will open IIS and restart the server click the server on the left click restart on the right
</p>
<br />
<img src="https://i.imgur.com/bq3s4S6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
now we will load the osTicket site through ISS. on the left select the drop down menu of your sever then got to sites and select the drop down menu then default web site then click on osTicket then on the right click browse
</p>
<br />
<img src="https://i.imgur.com/8OdVLje.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now seeing the osTicket site you can see the prerequisites some of the recommended extentions on the list are not enabled so we will be enabling them.
</p>
<br />
<img src="https://i.imgur.com/SMiw3yR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
To enable them we will return to ISS click the server drop down menu then sites dropdown menu then default web site dropdown menu then click on osTicket then from there click PHP manager
</p>
<br />
<img src="https://i.imgur.com/j4aFN4u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
now click on enable or disable an extention
</p>
<br />
<img src="https://i.imgur.com/5eF3CH4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now look for the extentions that need to be enable and enable them 
</p>
<br />
<img src="https://i.imgur.com/xZMXPOV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we are going rename ost-sampleconfig.php to ost-config.php
go to c:\drive look for intetpub open the file look for wwwroot open that file then osTicket file then within the include file look for ost-sampleconfig.php and rename it ost-config.php
</p>
<br />
<img src="https://i.imgur.com/epjpiyk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we will asssing permmisions to the ost-config.php file.
right click the file go to properties and Disable inheritance and remove all inheritance permmsions from this object 
</p>
<br />
<img src="https://i.imgur.com/fKv2cia.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now click on add then click on select a pincipal and add a user, group, or built-in  security principla then click ok then check full control and click apply then ok
</p>
<br />
<img src="https://i.imgur.com/90PGGy5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now go back to the osTicket browser and click countinue  
</p>
<br />
<img src="https://i.imgur.com/iITn8TA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we will instal HeidiSQL 12.3.0.6589 and launch it
</p>
<br />
<img src="https://i.imgur.com/1gxeD16.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Click new and then type in your SQL username and password and click open 
</p>
<br />
<img src="https://i.imgur.com/LyiWeq8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now we will create a new database by right clicking top option on the left and clicking create new then clicking database name it osTicket
</p>
<br />
<img src="https://i.imgur.com/V9Lm2bb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now back on the osTicket site we will click continue 
</p>
<br />
<img src="https://i.imgur.com/iITn8TA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Now set up your system settings, admin user, and database settings. then click install now
</p>
<br />
<img src="https://i.imgur.com/IcMesmx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
osTicket is now installed
</p>
<br />
<img src="https://i.imgur.com/Clzj7Xs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

