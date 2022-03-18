# Web server Project

![VirtualBox](https://badgen.net/badge/icon/VirtualBox/183A61?labelColor=FFF&icon=https://simpleicons.org/icons/virtualbox.svg&label) ![VMware](https://badgen.net/badge/icon/VMware/607078?labelColor=FFF&icon=https://simpleicons.org/icons/vmware.svg&label) ![Hyper-V](https://badgen.net/badge/icon/Hyper-V/0078D7?labelColor=FFF&icon=https://simpleicons.org/icons/microsoft.svg&label) ![xAMPP](https://badgen.net/badge/icon/xAMPP/F97300?labelColor=FFF&icon=https://simpleicons.org/icons/xampp.svg&label) ![Apache](https://badgen.net/badge/icon/Apache/D22128?labelColor=FFF&icon=https://simpleicons.org/icons/apache.svg&label) ![MySQL](https://badgen.net/badge/icon/MySQL/4479A1?labelColor=FFF&icon=https://simpleicons.org/icons/mysql.svg&label) ![PHP](https://badgen.net/badge/icon/PHP/777BB4?labelColor=FFF&icon=https://simpleicons.org/icons/php.svg&label)

![ProjectName](https://badgen.net/badge/Project%20Name/Webserver/0058E7?labelColor=000) ![Version](https://badgen.net/badge/Version/01.01/cyan?labelColor=000) ![Author](https://badgen.net/badge/Authors/Sabaini%20Chiara/60C?labelColor=000)


---

## Content

- [Requirements](#requirements)
- [Setting up the enviroment](#setting-up-the-enviroment)
    - [Setup of the xAMPP stack on a Windows system](#setting-up-xampp-on-a-windows-system)
    - [Setup of the LAMPP stack on a Linux based system](#setting-up-lampp-on-a-linux-based-system)
    - [Testing the setup](#testing-the-setup)

---

## Requirements ![VM](https://badgen.net/badge/VM/Unix-based/D80150?labelColor=000) ![VM](https://badgen.net/badge/VM/Windows/0078D6?labelColor=000) ![VMM](https://badgen.net/badge/VMM/any/F80102?labelColor=000)

- average knowledge of
    - how to setup and work with a VMs
    - GNU/Linux's command line
    - Windows's command line
    - how to google stuff
- 1 VMM (eg.: VirtualBox, HyperV, VMWare)
- 2 VMs
    - 1 with a Linux based OS
    - 1 with Windows

---
### Setting up the enviroment

In the following paragraphs I'm going to explain how to create a local server environment on your machine.

I'm going to use the xAMPP stack.\
xAMPP stands for ***X &#x2192; cross-platform***, ***A &#x2192; Apache***, ***M &#x2192; MySQL***, ***P &#x2192; PHP***, ***P &#x2192; Perl***.\
It is a completely free and open source solution that gives you an incredible local web server to work on.

Installing the xAMPP stack simply gives you a control panel to manage all the inclusive components and sets you free from learning and remembering commands to run Apache, MySQL, etc.

---

### Setting up xAMPP on a Windows system
![VM](https://badgen.net/badge/icon/Windows/0078D6?labelColor=FFF&icon=https://simpleicons.org/icons/windows.svg&label) ![xAMPP](https://badgen.net/badge/icon/xAMPP/F97300?labelColor=FFF&icon=https://simpleicons.org/icons/xampp.svg&label)

- **Step 1 - Download and install xAMPP**\
To download and install xAMPP, go to the official [downloads page](https://www.apachefriends.org/download.html).\
You will see xAMPP ready to download for cross-platform like Windows, Linux, Mac OS X. Since we are discussing How to install xAMPP on a VM hosting Windows, therefore, we will **choose the Windows option**.
<br>

- **Step 2 - Run the installer to install xAMPP**<br>
    - ***1. xAMPP Setup Wizard***<br>
    During the installation process, you may come across warning pop-ups. But you would probably **click <kbd>Yes’ </kbd>o start the installation process**. Soon after you click on the downloaded file, the xAMPP setup wizard will open.<br>
    Now click on the <kbd>Next</kbd> Button to proceed.
    <br>

    - ***2. Select Components***<br>
    Next, you need to check the components which you want to install and can uncheck or leave as it is which you don’t want to install.<br>
    *You can see there are a few options which are light grey in color. These are the options which are necessary to run the software and will automatically be installed.*<br>
    Now click on the <kbd>Next</kbd> button to continue.
    <br>

    - ***3. Select Installation Folder***<br>
    Now you need to choose the folder where you want to install the xAMPP. You can **choose the default location or  any location of your choice**.<br>
    Then click the <kbd>Next</kbd> button to move ahead.
    <br>

    - ***4. Ready to Install xAMPP***<br>
    Now you’ll see another window with a message “Setup is now ready to begin installing xAMPP on your computer” like shown below.<br>
    **You just have to hit the <kbd>Next</kbd> button to proceed.**
    <br>

    - ***5. xAMPP Installation***<br>
    Now just be patient and wait for the installation to complete.<br>
    Once the installation is completed, you will be asked whether you would like to start the control panel now or not, displaying the message “Do you want to start the control panel now?”.<br>
    **Check the box and click on the <kbd>Finish</kbd> button and see if the xAMPP is working fine.**

- **Step 3 - xAMPP is now Installed on Windows, run it**<br>
If the entire process of xAMPP installation went correctly, then the control panel would open smoothly.<br>
Now **click on the <kbd>Start</kbd> button corresponding to Apache and MySQL**.


That’s it. You have successfully installed xAMPP on Windows. Or say you have successfully installed xAMPP locally.<br>
Once you start the modules, you should see their status turn to green. Whereas, on the right side, you can see the process ID number and port numbers every module is using.

---

### Setting up LAMPP on a Linux based system
![VM](https://badgen.net/badge/icon/Unix-based/D80150?labelColor=FFF&icon=https://simpleicons.org/icons/linux.svg&label) ![LAMPP](https://badgen.net/badge/icon/LAMPP/F97300?labelColor=FFF&icon=https://simpleicons.org/icons/xampp.svg&label)

> LAMPP is acronym for Linux operating system xAMPP stack.

**Prerequisites:** you will need a root user, in order to be able to execute all the commands

- ***Step 1 — Installing Apache and Updating the Firewall***
![Apache](https://badgen.net/badge/icon/Apache/D22128?labelColor=FFF&icon=https://simpleicons.org/icons/apache.svg&label)

Start by updating the package manager cache. If this is the first time you’re using sudo within this session, you’ll be prompted to provide your user’s password to confirm you have the right privileges to manage system packages with apt.<br>

```bash
$ sudo apt update && upgrade
```

Then, install Apache using the following command:

```bash
$ sudo apt install apache2
```
 
 You’ll also be prompted to confirm Apache’s installation by pressing <kbd>Y</kbd>, then <kbd>ENTER</kbd>.

Once the installation is finished, you’ll need to adjust your firewall settings to allow HTTP traffic. UFW has different application profiles that you can leverage for accomplishing that. To list all currently available UFW application profiles, you can run:

```bash
$ sudo ufw app list
```

The output should look like this:

```bash
Available applications:
  Apache
  Apache Full
  Apache Secure
  OpenSSH
```

>Here’s what each of these profiles mean:<br>
**Apache**: This profile opens only port 80 (normal, unencrypted web traffic).<br>
**Apache Full**: This profile opens both port 80 (normal, unencrypted web traffic) and port 443 (TLS/SSL encrypted traffic).<br>
**Apache Secure**: This profile opens only port 443 (TLS/SSL encrypted traffic).<br>

For now, it’s best to allow only connections on port `80`.

To only allow traffic on port `80`, use the Apache profile:

```bash
$ sudo ufw allow in "Apache"
```

You can verify the change with:

```bash
$ sudo ufw status
```

Output:

```bash
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere                                
Apache                     ALLOW       Anywhere                  
OpenSSH (v6)               ALLOW       Anywhere (v6)                    
Apache (v6)                ALLOW       Anywhere (v6)     
```

Traffic on port `80` is now allowed through the firewall.

To check if everything went as planned paste this url into your browser: `http://localhost`. You should be able to see the default Apache web page.

*If it returns `Status: incative`, just run `sudo ufw enable` and check again.*


- ***Step 2 — Installing MySQL***
![MySQL](https://badgen.net/badge/icon/MySQL/4479A1?labelColor=FFF&icon=https://simpleicons.org/icons/mysql.svg&label)

Now that your web server is up and running, it's time to install the database system, to be able to store and manage data for your site.<br>
MySQL is a popular database management system used within PHP environments.

Again, use apt to acquire and install this software:

```bash
$ sudo apt install mysql-server
```
Confirm the installation by typing <kbd>Y</kbd>, and then <kbd>ENTER</kbd>.

- ***Step 3 - Installing PHP***
![PHP](https://badgen.net/badge/icon/PHP/777BB4?labelColor=FFF&icon=https://simpleicons.org/icons/php.svg&label)

PHP is the component of our setup that will process code to display dynamic content to the final user.\
In addition to the `php` package, you’ll need `php-mysql` (PHP module that allows PHP to communicate with MySQL-based databases) and `libapache2-mod-php` (enables Apache to handle PHP files).

To install these packages, run:

```bash
$ sudo apt install php libapache2-mod-php php-mysql
```

Once the installation is finished, you can run this command to check your PHP version:

```bash
$ php -v
```

Output:

```bash
PHP 7.4.3 (cli) (built: Oct 21 2021 9:13:35) ( NTS )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
    with Zend OPcache v7.4.3, Copyright (c), by Zend Technologies
```

- ***Step 4 - Creating a Virtual Host***
![Virtual Host](https://badgen.net/badge/icon/Virtual%20Host/D22128?labelColor=FFF&icon=https://simpleicons.org/icons/apache.svg&label)

Apache's virtual hosts (similar to server blocks in Nginx) it's used to encapsulate configuration details and host more than one domain from a single server.

Apache (on Ubuntu) has one server block enabled by default that is configured to serve documents from the `/var/www/html` directory.\
This works well for a single site, but it can become unwieldy if you are hosting multiple sites.\
Instead of modifying `/var/www/html`, we’ll create a directory structure within `/var/www` for `<your_domain>` site, leaving `/var/www/html` in place as the default directory to be served if a client request doesn’t match any other sites.

First, you need to create the directory for `<your_domain>` as follows:

```bash
$ sudo mkdir /var/www/<your_domain>
```

Then, assign ownership of the directory with the `$USER` environment variable, which will reference your current system user:

```bash
$ sudo chown -R $USER:$USER /var/www/<your_domain>
```

Now, open a new configuration file in Apache’s `sites-available` directory using your preferred cli editor.\
I’ll use nano:

```bash
$ sudo nano /etc/apache2/sites-available/<your_domain>.conf
```

This will create a new blank file. Paste in the following bare-bones configuration:

```xml
<VirtualHost *:80>
    ServerName <your_domain>
    ServerAlias www.<your_domain>
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/<your_domain>
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Save and close the file when you’re done. If you’re using nano, you can do that by pressing <kbd>CTRL+X</kbd>, then <kbd>Y</kbd> and <kbd>ENTER</kbd>.

With this VirtualHost configuration, we’re telling Apache to serve `<your_domain>` using `/var/www/your_domain` as the web root directory. If you’d like to test Apache without a domain name, you can remove or comment out the options `ServerName` and `ServerAlias` by adding a `#` character in the beginning of each option’s lines.

You can now use `a2ensite` to enable the new virtual host:

```bash
$ sudo a2ensite your_domain
```

You might want to disable the default website that comes installed with Apache.\
This is required if you’re not using a custom domain name, because in this case Apache’s default configuration would overwrite your virtual host.

To disable Apache’s default website, type:

```bash
$ sudo a2dissite 000-default
```

To be sure that your configuration file doesn’t contain syntax errors, run:

```bash
$ sudo apache2ctl configtest
```
 
Finally, reload Apache to apply this changes:

```bash
$ sudo systemctl reload apache2
```

---

### Testing the setup
![Testing](https://badgen.net/badge/icon/Testing/0E0?labelColor=FFF&icon=https://www.reshot.com/preview-assets/icons/Y3PM7Z5ELC/testing-Y3PM7Z5ELC.svg&label)

- ***Step 1 - Testing the Virtual Host***

Your new website is now active, but the web root `/var/www/your_domain` is still empty. Create an `index.html` file in that location so that we can test that the virtual host works as expected:

```bash
$ nano /var/www/your_domain/index.html
```

Include the following content in this file:

```html
<html>
  <head>
    <title>Hello world!</title>
  </head>
  <body>
    <h1>Hello World!</h1>

    <p>This is the landing page of <strong>my new website</strong>.</p>
  </body>
</html>
```
 
Now go to your browser and access your server’s domain name or IP address once again: `http://server_domain_or_IP`

You’ll see a page like this:

<add pic>

***Changing the `DirectoryIndex` setup on Apache***

With the default `DirectoryIndex` settings on Apache, a file named `index.html` will always take precedence over an `index.php` file. This is useful for setting up maintenance pages in PHP applications, by creating a temporary `index.html` file containing an informative message to visitors. Because this page will take precedence over the `index.php` page, it will then become the landing page for the application. Once maintenance is over, the `index.html` is renamed or removed from the document root, bringing back the regular application page.

In case you want to change this behavior, you’ll need to edit the `/etc/apache2/mods-enabled/dir.conf` file and modify the order in which the index.php file is listed within the `DirectoryIndex` directive:

```bash
$ sudo nano /etc/apache2/mods-enabled/dir.conf
```

It's content has to look like this:
```xml
<IfModule mod_dir.c>
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```

After saving and closing the file, you’ll need to reload Apache so the changes take effect:

```bash
$ sudo systemctl reload apache2
```

- ***Step 2 - Testing PHP processing on your webserver***

Now, we’ll create a PHP test script to confirm that Apache is able to handle and process requests for PHP files.

Create a new file named `info.php` inside your custom web root folder:

```bash
$ nano /var/www/your_domain/info.php
```

This will open a blank file. Add the following text, which is valid PHP code, inside the file:

```php
<?php
phpinfo();
>
```
Save and close the file.

To test this script, go to your web browser and access your server’s domain name or IP address, followed by the script name, which in this case is `info.php`:

`http://<server_domain_or_IP>/info.php`

You’ll see a page similar to this:
![phpinfo](https://assets.digitalocean.com/articles/lamp_ubuntu2004/phpinfo.png)

If you can see this page in your browser, then your PHP installation is working as expected.

- ***Step 3 - Testing DB connection from PHP***

We're going to create test table with dummy data and query for its contents from a PHP script. Before we can do that, we need to create a test database and a new MySQL user properly configured to access it.

First, connect to the MySQL console using the root account:

```bash
$ sudo mysql
```

To create a new database, run the following command from your MySQL console:

```bash
mysql> CREATE DATABASE dummyDB;
```

Now you can create a new user and grant them full privileges on the custom database you’ve just created.

The following command creates a new user named `admin`, using `mysql_native_password` as default authentication method. We’re defining this user’s password as `password`, but you should replace this value with a secure password of your own choosing.

```bash
mysql> CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

To give this user permission over the `dummyDB` database:

```bash
mysql> GRANT ALL ON dummyDB.* TO 'admin'@'localhost';
```

It's time to create a table (I'll call it `students`):
```bash
mysql> CREATE TABLE students(
                mat INT,
                name VARCHAR(25),
                surname VARCHAR(25),
                PRIMARY KEY(mat)
            );
```

Now we can execute an INSERT to insert some data in the table:

```bash
mysql> INSERT INTO students VALUES(18910, "Marilyn", "Monroe");
```

