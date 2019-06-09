# ownCloud 9.0 Server Quick Start Linux Installation 

## System Requirements

### Operating System

- Ubuntu 14.04, 16.04  
- Debian 8  
- RHEL 7  
- CentOS 7  
- SLES 12  
- openSUSE 13.2, Leap 42.1  

### Database 

* MySql or MariaDB 5.5+*  
* Oracle 11g  
* PostgresSQL 9  
* SQLite  

``*``*It is currently required to disable Binary Logging when using MySQL/MariaDB*

### Webserver 

* Apache 2.4 with `prefork` and `mod_php`  

### PHP Runtime

* PHP Runtime 5.6  
* PHP Runtime 7.0  
* PHP Runtime 7.1  
* PHP Runtime 7.2  

### Mobile

* iOS 9.0+  
* Android 4.0+  

### Browser

- IE11+ (except Compatibility Mode)
- Firefox 14+  
* Chrome 18+  
* Safari 5+  

## Repository Options

- [Stable](https://download.owncloud.org/download/repositories/stable/owncloud/) will track the current stable ownCloud version  
- [Major releases](https://download.owncloud.org/download/repositories/9.0/owncloud/) can be specified   

Follow the instructions on the installation pages then proceed with the Installation Wizard.  

## Downgrading Not Supported

- Due to the risk of data corruption only fresh installations of older versions is supported. Data then can be restored from backup.  

## Installation Wizard

- Once all steps on the installation pages are complete and all files are installed the Installation Wizard should be run  

1.) In a browser navigate to [http://localhost/owncloud](http://localhost/owncloud)  
2.) Create the administrator account by entering any desired username and password  
3.) Click **Finish Setup**  

Database settings can now be configured. See the ownCloud [installation documentation](https://doc.owncloud.org/server/9.0/admin_manual/installation/installation_wizard.html#data-directory-location) for more information.  

## Configuring ownCloud



1.) Configure ownCloud to listen on the server's IP address and a custom port (in this instance 8080).  

- In the `config.php` file locate the `'dbname'` parameter   
- Change `'owncloud'` to the IP address and port   

		'dbname' => '192.168.0.2:8080'  

More configuration options are available in the ownCloud [Config.php Parameters](https://doc.owncloud.org/server/9.0/admin_manual/configuration_server/config_sample_php_parameters.html) documentation.   

2.) Create user accounts  

- Login to ownCloud  
- Navigate to the User Management page  
- Click in the `username` box at the top of the page  
- Add the desired username and password   
- Add the user to a group if desired  
- If **Send email to new user** was selected in the control panel an email address may also be specified. ownCloud will send an email notification with the new login information.   

Detailed information on user accounts can be found in the ownCloud [User Configuration manual](https://doc.owncloud.org/server/9.0/admin_manual/configuration_user/user_configuration.html).  

3.) Connect to the ownCloud server using a desktop or mobile client  

- To access from a desktop client users can use any of the supported browsers to navigate to the specified `dbname`. In this example [http://192.168.0.2:8080](http://192.168.0.2:8080).  

- When accessing the ownCloud site via a mobile device users will be presented with the option to download either the Android or iOS application  

