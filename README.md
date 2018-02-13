### Partybarge Car Catalog - Final Project for FSND Linux Server Configuration:

## Server Info
Server Hosted by Amazon Lightsail

Web URL = http://ec2-18-217-137-212.us-east-2.compute.amazonaws.com

IP Addr = 18.217.137.212 

*IP address different in examples due to
a reboot of the AWS server.
 
SSH Port = 2200


## The SSH key submitted with the project can be used to log in as grader on the server.

PassPhrase: Partybarge


-----BEGIN RSA PRIVATE KEY-----
Proc-Type: 4,ENCRYPTED
DEK-Info: AES-128-CBC,55922AC80D3F5BBF721665C7B0C9AB9F

P4zFuIvGW06gNaFscM+9GSvljqMDOPSCZvsrBNmw7MmSVZjT3JwscuVNMn06hv2M
kQC78Wqc+zmQx3ybcosRWB8L+QoUsNg8/LPYInWH5GEyn0iej302ShOYyYQZlDM5
2/STqpC5O6fpEifoVSmSj6Ay9Ev/0agwRVXkomwL1v28fPsqiA+aPiwI+lVN52zm
0s/QnBeJgpOV1DZfyfJtExOfLjDIQ85Tkv6F9FdeoB71UYX3tH+5lIqvfOsrskGd
sQnNPzDxMO0ZOHkCota/qYc7yM5lmiWBuMgnfduvktXYAu59g7/PCjd6jdu+mysw
Cmg6noXlpgOfjhT5LqzWRQcnicHOE6+F3rtBQwoHwTU75gJpQRuzYPUWGMPKH8Rx
/vUt6c+mG+xyP9d3QFKb2r/L6uVg5WPM1x/Mbcn1Gdo105DZmPYXsedd298pogMl
kp5BD8OwNhAXEzfGfWm+RkkSLCzogyU8sSB2xje0zaizmOMcKP6uE5n3izh4j0Wz
4Ha6XhpKP5lLJjZzg3c0ErUzuPIyGqvTJHCQy2SHUzPamerHuhYf4gP001xNB28r
nn2I/GihrTnzOX3TX/3hjasukIAAy+rH2ToexgLU3W6gtH4tU9PlhnXU5SMI4g+6
epSqhSd1rVQ16N6NRzAMF3RSzTqsBpsgz+/dvc7XxUBcCWThPsz/KCiDIAJMVy8o
+beeGOWey8YUOk6B6nH7P3aH0BtD1pXum+EcQwyoGZUO0Qf1S1JwQosIfjm036bo
hIKh9zgOYD8IZtaQXFthROxtcXcc81x5JOk9Ez75ZSHXRwHNiORIPrZRbn4CUl3A
mErKpIPJ2MeaHx6mgZ+XmfsJD9jFfhmGGM0sJ81hxrQD2P1z9Ai2u3bmQVQ4QYSe
FjRb2J8ql8iPmlusrK5+v/g+PasqVsQKHK7o08dJUe4v1TOUL+KsvLF0DmWv5Piz
kYoreXnt+UXutcBNiRp5CTnSCzhTQGTVQSP1WOK7xb6vuKy8JNHN8/Zy6C90U7oU
TaAuSjrJXv0fO7EmfOBHhiYiSA6vXFEgwLBkDuNhUezX8/vmLZwdkyxpcci43Jll
iG7jnBdg0LHAYj+YFV7XYXRhLN63QWAD1PgDLguZkTeFbrx260RYD9LZ4xLZJ+u3
LxiyPdN3awjZx/8K04s4/kAIStNuWPRRNqbXeqK5acvQ/38x4LhHDe/J3GsYkANX
xb5t+hZj9Bjzyk3D7yD1N8coGEScvQPNvbguL76UrisnBNvvNlo0God2dLpT4waN
5aB1dOuxO26y1YQ+2NPm7X6fxv/cgUQjGXN7r5Lo4pglfFR0ktGJcD0rNMHikRx2
yO3GS0OhLHwRc100aKpqNiteb9B3UbeJ/j+0lNe/PfCLELLfElaZIb/D4u5SQam9
omTOOeOVPz0U+ecX6T7DbbeCl9/GQQrLVaFedo3z3b7my3aAaky6EmsOMrApvTjT
GeSLRv8EL6ErwGHV31XhB6bSLYHyu6sJ8XE3DchFJjB9Zs8aoL12rI8xvcteWxAq
5H1cZ9MPbrocT9kt73R7L1yFJW7FRYZPlBu5rWrcAsVa4luzacbaJCQ96jAkqdys
-----END RSA PRIVATE KEY-----

# Login as grader  <--password grader

dana ~ $ ssh grader@52.15.228.45 -p 2200 -i ~/.ssh/amazon_aws
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-1013-aws x86_64)


# The grader user can run commands using sudo to inspect files that are readable only by root.

grader@ip-172-26-3-183:~$ sudo /etc/passwd
[sudo] password for grader: 
grader@ip-172-26-3-183:~$ sudo cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash
dh3008:x:1001:1001:Dana Hazelton,,,:/home/dh3008:/bin/bash
grader:x:1002:1002:grader,,,:/home/grader:/bin/bash


## Port Configuration:
Only allow connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).

dana ~ $ ssh dh3008@52.15.228.45 -p 22 -i ~/.ssh/amazon_aws
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-1013-aws x86_64)


*** System restart required ***
Last login: Mon Feb  5 20:13:37 2018 from 108.252.105.240
dh3008@ip-172-26-3-183:~$ sudo ufw deny 22
Rule updated
Rule updated (v6)
dh3008@ip-172-26-3-183:~$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
22                         DENY        Anywhere                  
80/tcp                     ALLOW       Anywhere                  
123/udp                    ALLOW       Anywhere                  
2200/tcp                   ALLOW       Anywhere                  
23/tcp                     DENY        Anywhere                  
22 (v6)                    DENY        Anywhere (v6)             
80/tcp (v6)                ALLOW       Anywhere (v6)             
123/udp (v6)               ALLOW       Anywhere (v6)             
2200/tcp (v6)              ALLOW       Anywhere (v6)             
23/tcp (v6)                DENY        Anywhere (v6)   


## Key-based SSH authentication is enforced.

Change to no to disable tunnelled clear text passwords
dh3008@ip-172-26-3-183:~$ sudo nano /etc/ssh/sshd_config
PasswordAuthentication no

## SSH is hosted on non-default port.

What ports, IPs and protocols we listen for

dana ~ $ ssh dh3008@52.15.228.45 -p 2200 -i ~/.ssh/amazon_aws
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-1013-aws x86_64)

Port 22 <--default is deny
Port 2200 <-- allowed for shh

# You cannot log in as root remotely.
## Authentication:
LoginGraceTime 120
PermitRootLogin no <-- disabled
StrictModes yes


    PermitRootLogin
             Specifies whether root can log in using ssh(1).  The argument must be “yes”, “prohibit-password”,
             “without-password”, “forced-commands-only”, or “no”.  The default is “prohibit-password”.

             If this option is set to “prohibit-password” or “without-password”, password and keyboard-interactive authen‐
             tication are disabled for root.

             If this option is set to “forced-commands-only”, root login with public key authentication will be allowed,
             but only if the command option has been specified (which may be useful for taking remote backups even if root
             login is normally not allowed).  All other authentication methods are disabled for root.

             If this option is set to “no”, root is not allowed to log in.


# SSH is hosted on non-default port.

dh3008@ip-172-26-3-183:~$ sudo cat /etc/ssh/sshd_config
## Package generated configuration file
## See the sshd_config(5) manpage for details

## What ports, IPs and protocols we listen for
Port 2200

dana ~ $ ssh dh3008@52.15.228.45 -p 2200 -i ~/.ssh/amazon_aws
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-1013-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

18 packages can be updated.
6 updates are security updates.


*** System restart required ***
Last login: Tue Feb  6 01:33:26 2018 from 108.252.105.240


# The web server responds on port 80.


## Change timezone to UTC
Check the timezone with the date command. This will display the current timezone after the time. If it's not UTC change it like this:

Config Local TimeZone to UTC:
dh3008@ip-172-26-3-183:~$ sudo timedatectl set-timezone UTC

dh3008@ip-172-26-3-183:~$ date
Sat Feb 10 18:33:43 UTC 2018


## Install GIT and Pull Catalog App into Server:

grader@ip-172-26-3-183:~$ cd /srv
grader@ip-172-26-3-183:/srv$ ls -ls
total 0
grader@ip-172-26-3-183:/srv$ sudo mkdir catalog
[sudo] password for grader: 
grader@ip-172-26-3-183:/srv$ sudo chown www-data:www-data catalog/
grader@ip-172-26-3-183:/srv$ ls -lsa
total 12
4 drwxr-xr-x  3 root     root     4096 Feb 10 18:49 .
4 drwxr-xr-x 23 root     root     4096 Feb  5 06:05 ..
4 drwxr-xr-x  2 www-data www-data 4096 Feb 10 18:49 catalog

grader@ip-172-26-3-183:/srv$ sudo -u www-data git clone https://github.com/Partybarge02/CarCatolog.git catalog
Cloning into 'catalog'...
remote: Counting objects: 53, done.
remote: Compressing objects: 100% (37/37), done.
remote: Total 53 (delta 7), reused 53 (delta 7), pack-reused 0
Unpacking objects: 100% (53/53), done.
Checking connectivity... done.

grader@ip-172-26-3-183:/srv$ ls -lsa
total 12
4 drwxr-xr-x  3 root     root     4096 Feb 10 18:49 .
4 drwxr-xr-x 23 root     root     4096 Feb  5 06:05 ..
4 drwxr-xr-x  5 www-data www-data 4096 Feb 10 18:51 catalog

grader@ip-172-26-3-183:/srv$ cd catalog
grader@ip-172-26-3-183:/srv/catalog$ ls -lsa
total 24
4 drwxr-xr-x 5 www-data www-data 4096 Feb 10 18:51 .
4 drwxr-xr-x 3 root     root     4096 Feb 10 18:49 ..
4 drwxr-xr-x 8 www-data www-data 4096 Feb 10 18:51 .git
4 drwxr-xr-x 4 www-data www-data 4096 Feb 10 18:51 ItemCatalog
4 drwxr-xr-x 3 www-data www-data 4096 Feb 10 18:51 .vagrant
4 -rw-r--r-- 1 www-data www-data 1906 Feb 10 18:51 Vagrantfile


## Install Flask, SQLAlchemy, etc:
grader@ip-172-26-3-183:~$ sudo apt-get install python-psycopg2 python-flask

grader@ip-172-26-3-183:~$ sudo apt-get install python-sqlalchemy python-pip

grader@ip-172-26-3-183:~$ sudo pip install oauth2client
Successfully installed httplib2-0.10.3 oauth2client-4.1.2 pyasn1-modules-0.2.1 rsa-3.4.2
You are using pip version 8.1.1, however version 9.0.1 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.

grader@ip-172-26-3-183:~$ sudo pip install --upgrade pip
Successfully installed pip-9.0.1


grader@ip-172-26-3-183:~$ sudo pip install requests
Successfully installed certifi-2018.1.18 chardet-3.0.4 idna-2.6 requests-2.18.4 urllib3-1.22

grader@ip-172-26-3-183:~$ sudo pip install httplib2.
Requirement already satisfied: httplib2 in /usr/local/lib/python2.7/dist-packages



grader@ip-172-26-3-183:~$ sudo pip install flask-seasurf
Successfully installed flask-seasurf-0.2.2


## PostgreSQL:

grader@ip-172-26-3-183:~$ sudo apt-get install postgresql postgresql-contrib
Reading package lists... Done
Building dependency tree       
Reading state information... Done
postgresql is already the newest version (9.5+173ubuntu0.1).
The following NEW packages will be installed:
  postgresql-contrib
0 upgraded, 1 newly installed, 0 to remove and 4 not upgraded.
Need to get 5,456 B of archives.
After this operation, 59.4 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://us-east-2.ec2.archive.ubuntu.com/ubuntu xenial-updates/main amd64 postgresql-contrib all 9.5+173ubuntu0.1 [5,456 B]
Fetched 5,456 B in 0s (28.5 kB/s)       
Selecting previously unselected package postgresql-contrib.
(Reading database ... 84965 files and directories currently installed.)
Preparing to unpack .../postgresql-contrib_9.5+173ubuntu0.1_all.deb ...
Unpacking postgresql-contrib (9.5+173ubuntu0.1) ...
Setting up postgresql-contrib (9.5+173ubuntu0.1) ...


## To ensure that remote connections to PostgreSQL are not allowed:
##"local" is for Unix domain socket connections only
local   all             all                                     peer
## IPv4 local connections:
host    all             all             127.0.0.1/32            md5
## IPv6 local connections:
host    all             all             ::1/128                 md5

## Allow replication connections from localhost, by a user with the
## replication privilege.
## local   replication     postgres                                peer
## host    replication     postgres        127.0.0.1/32            md5
## host    replication     postgres        ::1/128                 md5


## Confige Postgres Database to Serve Web App.

dh3008@ip-172-26-3-183:~$ sudo apt-get install git
Reading package lists... Done
Building dependency tree       
Reading state information... Done
git is already the newest version (1:2.7.4-0ubuntu1.3).
0 upgraded, 0 newly installed, 0 to remove and 4 not upgraded.


postgres=# CREATE USER dh3008 with password 'Trailhawk!15';
CREATE ROLE
postgres=# \du
postgres=# ALTER USER dh3008 WITH SUPERUSER;
ALTER ROLE

postgres=# CREATE USER catalog with password 'catalog';
CREATE ROLE

## Database catalog created
postgres=# CREATE DATABASE catalog;
CREATE DATABASE


dh3008@ip-172-26-3-183:~$ sudo su postgres
[sudo] password for dh3008: 
postgres@ip-172-26-3-183:/home/dh3008$ psql
psql (9.5.11)
Type "help" for help.

postgres=# \l
                                  List of databases
   Name    |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges   
-----------+----------+----------+-------------+-------------+-----------------------
 catalog   | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | 
 postgres  | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | 
 template0 | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
(4 rows)

## Set user catalog OWNER of the catalog DATABASE:
postgres=# ALTER DATABASE catalog OWNER TO catalog;
ALTER DATABASE
postgres=# \l
                                  List of databases
   Name    |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges   
-----------+----------+----------+-------------+-------------+-----------------------
 catalog   | catalog  | UTF8     | en_US.UTF-8 | en_US.UTF-8 | 
 postgres  | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | 
 template0 | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.UTF-8 | en_US.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
(4 rows)



## Error Log:

sudo tail 10 /var/log/apache2/error.log


## Restart server after core config  changes:
sudo service apache2 restart

### Required code changes to make the APP work:

grader@ip-172-26-3-183:/srv/catalog$ ll
total 20
drwxr-xr-x 4 www-data www-data 4096 Feb 12 23:18 ./
drwxr-xr-x 3 root     root     4096 Feb 10 18:49 ../
-rw-r--r-- 1 root     root      862 Feb 11 22:11 catalog.wsgi <--created file so App anf server can communicate
drwxr-xr-x 8 www-data www-data 4096 Feb 10 18:51 .git/
drwxr-xr-x 4 www-data www-data 4096 Feb 12 02:59 ItemCatalog/ <-- App files

## WSGI file:
grader@ip-172-26-3-183:/srv/catalog$ cat catalog.wsgi 
#!/usr/bin/python
import sys
import logging
logging.basicConfig(stream=sys.stderr)
sys.path.insert(0, '/srv/catalog/ItemCatalog')

from __init__ import app as application

application.secret_key = 'super_secret_key'
 

# Item Catalog files:
grader@ip-172-26-3-183:/srv/catalog/ItemCatalog$ ll
total 68
drwxr-xr-x 4 www-data www-data  4096 Feb 12 02:59 ./
drwxr-xr-x 4 www-data www-data  4096 Feb 12 23:22 ../
-rw-r--r-- 1 www-data www-data  1613 Feb 11 13:15 catalog_dbsu.py 
-rw-r--r-- 1 www-data www-data  2411 Feb 11 20:13 catalog_dbsu.pyc
-rw-r--r-- 1 www-data www-data  4103 Feb 11 13:14 Cats_Items.py
-rw-r--r-- 1 www-data www-data   549 Feb 12 02:41 client_secrets.json
-rw-r--r-- 1 www-data www-data 13108 Feb 12 02:59 __init__.py
-rw-r--r-- 1 www-data www-data 10945 Feb 12 02:59 __init__.pyc
-rw-r--r-- 1 www-data www-data  2439 Feb 10 18:51 README.md
drwxr-xr-x 5 www-data www-data  4096 Feb 10 18:51 static/
drwxr-xr-x 2 www-data www-data  4096 Feb 12 02:33 templates/

## Files pointing to sqlite database needed to be repointed to Postgresql Database we created:
__init_.py, catalog_dbsu.py # Cats_Items:
engine = create_engine('postgresql://catalog:catalog@localhost:5432/catalog')

## For OAuth to function  __init__.py & client_secrets.json required modification:

## __init__.py

CLIENT_ID = json.loads(
    open('/srv/catalog/ItemCatalog/client_secrets.json', 'r').read())['web']['client_id']

def gconnect():
	# Upgrade the authorization code into a credentials object
        oauth_flow = flow_from_clientsecrets('/srv/catalog/ItemCatalog/client_secrets.json', scope='')


## client_secrets.json

To match server addresses
"javascript_origins":["http://18.217.137.212"," http://ec2-18-217-137-212.us-east-2.compute.amazonaws.com"]}}

## Trouble with Filenames in templates directory:
	Renamed all file names in directory with lowercase only - resolved issue 


# Create and enabed catalog.conf(config file):

Created file here:
grader@ip-172-26-3-183:/etc/apache2/sites-available$ ll
total 24
drwxr-xr-x 2 root root 4096 Feb 12 01:38 ./
drwxr-xr-x 8 root root 4096 Feb 12 00:25 ../
-rw-r--r-- 1 root root 1377 Feb  6 02:18 000-default.conf
-rw-r--r-- 1 root root 1824 Feb 12 01:38 catalog-app.conf <---
-rw-r--r-- 1 root root 6338 Apr  5  2016 default-ssl.conf

grader@ip-172-26-3-183:/etc/apache2/sites-available$ cat catalog-app.conf 
<VirtualHost *:80>
        # The ServerName directive sets the request scheme, hostname and port that
        # the server uses to identify itself. This is used when creating
        # redirection URLs. In the context of virtual hosts, the ServerName
        # specifies what hostname must appear in the request's Host: header to
        # match this virtual host. For the default virtual host (this file) this
        # value is not decisive as it is used as a last resort host regardless.
        # However, you must set it for any further virtual host explicitly.
        ServerName 52.15.228.45 <--Server name

        ServerAdmin dh3008@localhost <-- Adim Address

        # Define WSGI parameters. The daemon process runs as the www-data user.
        WSGIDaemonProcess catalog user=www-data group=www-data threads=5
        WSGIProcessGroup catalog <----
        WSGIApplicationGroup %{GLOBAL}

        # Define the location of the app's WSGI file
        WSGIScriptAlias / /srv/catalog/catalog.wsgi <----

        # Allow Apache to serve the WSGI app from the catalog app directory
        <Directory /srv/catalog/> <----
                Require all granted
        </Directory>

        # Setup the static directory (contains CSS, Javascript, etc.)
        Alias /static /srv/catalog/ItemCatalog/static <----

        # Allow Apache to serve the files from the static directory
        <Directory  /srv/catalog/ItemCatalog/static> <----
                Require all granted
        </Directory>

        # Available loglevels: trace8, ..., trace1, debug, info, notice, warn,
        # error, crit, alert, emerg.
        # It is also possible to configure the loglevel for particular
        # modules, e.g.
        #LogLevel info ssl:warn

        ErrorLog ${APACHE_LOG_DIR}/error.log
        LogLevel warn
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

## Then needed to enable config file on server to get it working:

grader@ip-172-26-3-183:/etc/apache2/sites-enabled$ ll
total 8
drwxr-xr-x 2 root root 4096 Feb 10 22:01 ./
drwxr-xr-x 8 root root 4096 Feb 12 00:25 ../
lrwxrwxrwx 1 root root   35 Feb 10 22:01 catalog-app.conf -> ../sites-available/catalog-app.conf 

## This required diabling the default.conf file :
sudo a2dissite 000-default.conf

## Then enable catalog.conf
sudo a2ensite catalog-app.conf

## To make this changes and provisioning active on server restart is required:
sudo service apache2 restart


# Resourses and Documentation used to complete project:

Udacity course work Linux Server Configuration
Amazon light sail
Amazon lightsail Documentation
Udacity foroum pages (alot of them)
Ubuntu - https://help.ubuntu.com/lts/serverguide/index.html
http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/
Google
Stackoverflow
WWW


# Linux-Server-Configuration
