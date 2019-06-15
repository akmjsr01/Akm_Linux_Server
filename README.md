# LINUX SERVER CONFIGURATION PROJECT
> by Anil Mishra

The task is to conduct a baseline installation of a Linux server and make it ready for hosting  a web applications. Also it has to be secured from many attack vectors, installed and configure a database server.


## Table of contents

- [SSH Client Info](#ssh-client-info)
- [Project Steps](#project-steps)
- [References](#references)


## SSH Client info

It's possible to connect to my instance using following address:
IP address: 54.212.66.211
Accessible SSH port: 2200
sudo
## Project steps

##### 1. Update all currently installed packages.
```
sudo apt-get update
sudo apt-get upgrade
```

##### 2. Install finger, a utility software to check users' status:
``sudo apt-get install finger``

##### 3. Add new users grader and give permission to sudo for this user
Create grader user:

``sudo add user grader``

Add sudo premission:

``sudo nano /etc/sudoers.d/grader `` type in ``grader ALL=(ALL:ALL) ALL`` save and quit.

Verify if permission was given correctly:

``sudo ls /etc/sudoers.d``



#### 4. Change the SSH port from 22 to 2200. Make sure to configure the Lightsail firewall to allow it.

6. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).



# References
- https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/
