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

![MySQL Config Wizard](https://i.imgur.com/zDMkkCz.png)

---

### Step 6: Register PHP with IIS

1. Open IIS as an administrator.
2. Click your server name in the left panel.
3. Open **PHP Manager**.
4. Click **Register new PHP version**.
5. Browse to `php-cgi` inside `C:\PHP` and select it.
6. Click **OK**, then restart the server by clicking the server name on the left and **Restart** on the right.

![PHP Manager](https://i.imgur.com/zdhfcSG.png)
![IIS Restart](https://i.imgur.com/bq3s4S6.png)

---

### Step 7: Install osTicket Files

1. Extract `osTicket-v1.15.8.zip` to a preferred location.
2. Open the extracted folder and locate the `upload` directory.
3. Copy the `upload` folder to `C:\inetpub\wwwroot`.
4. Rename the folder to **osTicket** (must be exactly this name).

![Upload Folder](https://i.imgur.com/MvaApo4.png)
![Move to wwwroot](https://i.imgur.com/8ZQwpNR.png)
![Move to wwwroot](https://i.imgur.com/Jcbv4BB.png)
---

### Step 8: Launch osTicket in Browser

1. Open IIS.
2. Navigate to **Sites > Default Web Site > osTicket**.
3. On the right panel, click **Browse** to launch the site in your browser.

![Launch Site](https://i.imgur.com/8OdVLje.png)

You will see a page showing required and recommended PHP extensions.

![osTicket Prerequisites](https://i.imgur.com/SMiw3yR.png)

---

### Step 9: Enable Required PHP Extensions

1. Go back to IIS and open **PHP Manager** for the osTicket site.
2. Click **Enable or disable an extension**.
3. Enable any missing extensions listed on the prerequisites page.

![PHP Manager for osTicket](https://i.imgur.com/j4aFN4u.png)
![Enable Extensions](https://i.imgur.com/5eF3CH4.png)
![Extension List](https://i.imgur.com/xZMXPOV.png)

---

### Step 10: Rename and Set Permissions on Config File

1. Navigate to `C:\inetpub\wwwroot\osTicket\include`.
2. Rename `ost-sampleconfig.php` to `ost-config.php`.

![Rename Config](https://i.imgur.com/epjpiyk.png)

2. Right-click `ost-config.php`, choose **Properties**, and go to the **Security** tab.
3. Click **Advanced** → **Disable inheritance** → Remove all inherited permissions.
4. Click **Add** → **Select a principal** → Add the IIS App Pool user (e.g., `IIS AppPool\DefaultAppPool`).
5. Grant **Full Control**, click **Apply**, then **OK**.

![File Permissions](https://i.imgur.com/fKv2cia.png)
![Add Principal](https://i.imgur.com/90PGGy5.png)

> 🔒 **Security Note:** After osTicket is successfully installed, remove **Write** and **Modify** permissions from `ost-config.php` to protect against unauthorized changes.

---

### Step 11: Install osTicket via Browser

1. Return to the osTicket browser tab.
2. Click **Continue** to proceed with setup.

![Continue Setup](https://i.imgur.com/iITn8TA.png)

3. Install HeidiSQL and launch it.

![Launch HeidiSQL](https://i.imgur.com/1gxeD16.png)

4. Click **New**, enter your MySQL credentials, then click **Open**.

![HeidiSQL Connection](https://i.imgur.com/LyiWeq8.png)

5. Right-click your server in the left panel → **Create new > Database** → Name it `osTicket`.

![Create Database](https://i.imgur.com/V9Lm2bb.png)

6. Return to the browser and click **Continue**.

![Continue Again](https://i.imgur.com/iITn8TA.png)

7. Fill in your site name, admin credentials, and database info, then click **Install Now**.

![Installation Final Step](https://i.imgur.com/IcMesmx.png)

---

## 🎉 osTicket is Now Installed!

![osTicket Installed](https://i.imgur.com/Clzj7Xs.png)


