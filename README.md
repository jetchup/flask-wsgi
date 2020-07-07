# flask-wsgi

Project located in http://3.121.226.37/, port 80

## Setup
-----------------
* Started an Amazon Lightsail instance with Ubuntu 16.04.
* Updated all packages.
* Changed the SSH port from 22 to 2200.
* Configured the Lightsail firewall to allow it.
* Configured  the instance's UFW to only allow incoming connections for SSH on port 2200, HTTP on port 80, and NTP on port 123.
* Created a new user account named grader.
* Gave grader the permission to sudo.
* Created an SSH key pair for grader using the ssh-keygen tool locally.
* Copied the .pub key and located it in grader's ~/.ssh folder as authorized_keys file.
* Configured the local timezone to UTC.

## Installed software
-----------------
* Apache
    * configured to serve a wsgi application.
* PostgreSQL
    * does not allow remote connections.
* Git

## Deployed project
* Cloned https://github.com/jetchup/catalog
    * created and populated the database in a virtualenv
    * set up configuration files to serve it in the virtualenv (Flask) on root on port 80
