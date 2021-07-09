
**Welcome!**
---------------------------- 
Oberon is a fork of HestiaCP and VestaCP. Like HestiaCP, Oberon lets you manage web domains, mail accounts, DNS zones, and databases from one central dashboard without the hassle of manually deploying and configuring individual components or services. 

Features and Services
----------------------------
* Apache2 and NGINX with PHP-FPM
* Multiple PHP versions (5.6 - 8.0, 7.4 as default)
* DNS Server (Bind) with clustering capabilities
* POP/IMAP/SMTP mail services with Anti-Virus, Anti-Spam, and Webmail (ClamAV, SpamAssassin, Roundcube, Rainloop)
* MariaDB or PostgreSQL databases
* Let's Encrypt SSL support with wildcard certificates
* Firewall with brute-force attack detection and IP lists (iptables, fail2ban, and ipset).

Supported platforms and operating systems
----------------------------
* **CPU Architecture:** AMD64 (x86_64 Intel/AMD)
* **Debian:** 10 or 9
* **Ubuntu:** 20.04 LTS or 18.04 LTS
* **NOTE:** Hestia Control Panel must be installed on top of a fresh operating system installation to ensure proper functionality.

Installing Oberon
============================
While we have taken every effort to make the installation process and the control panel interface as friendly as possible (even for new users), it is assumed that you will have some prior knowledge and understanding in the basics how to set up a Linux server before continuing.

## Step 1: Log in
To start the installation, you will need to be logged in as **root** or a user with super-user privileges. You can perform the installation either directly from the command line console or remotely via SSH:
```bash
ssh root@your.server
```
## Step 2: Download
Download the installation script for the latest release:
```bash
wget https://raw.githubusercontent.com/kasperireland/oberon/main/install/hst-install.sh
```
If the download fails due to an SSL validation error, please be sure you've installed the ca-certificate package on your system - you can do this with the following command:
```bash
apt-get update && apt-get install ca-certificates
```

## Step 3: Run
To begin the installation process, simply run the script and follow the on-screen prompts:
```bash
bash hst-install.sh
```
You will receive a welcome email at the address specified during installation (if applicable) and on-screen instructions after the installation is completed to log in and access your server.



How to upgrade an existing installation
============================
Automatic Updates are enabled by default on new installations of Oberon Control Panel and can be managed from **Server Settings > Updates**. To manually check for and install available updates, use the apt package manager:
```bash
apt-get update
apt-get upgrade
```


License
=============================
Oberon Control Panel is licensed under [GPL v3](https://github.com/hestiacp/hestiacp/blob/release/LICENSE) license, and is based on the [VestaCP](https://www.vestacp.com/) project.<br>
