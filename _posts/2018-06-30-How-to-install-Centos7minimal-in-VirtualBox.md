---
title: "How to install Centos 7 Minimal in Oracle VM VirtualBox"
date:   2018-06-30 00:53:10 +0800
categories: "QAEngineers"
---
# Introduction
<hr>

## What is Centos 7?
CentOS is a Linux distribution that provides a free, enterprise-class, community-supported computing platform functionally compatible with its upstream source, Red Hat Enterprise Linux

## What is Virtual Machine?
In computing, a virtual machine is an emulation of a computer system. Virtual machines are based on computer architectures and provide functionality of a physical computer.

## Why should you use Centos 7 and VirtualBox?
Well, they're free and beginner friendly _(I think lol :trollface:)_

## Prerequisites :
_You need to download these and install Virtual Box in your Windows system_
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads) <br>
* [Centos 7 Minimal](http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1804.iso)

## Note
Press _(right CTRL in your keyboard)_ to take your mouse cursor out of the Virtual Machine
<hr>
<br>

# Getting Started
<hr>

## 1.) Create your Virtual Machine
![Image with caption](https://i.imgur.com/AcO9Smy.jpg "Image with caption")
_Fig. 1 - Name your server, Select Linux as Type and Select Red Hat (64bit) then click Next. Just select your desired RAM and HDD space for your Virtual Machine, I like mine with 20GB HDD and 4GB RAM_

![Image with caption](https://i.imgur.com/3ixUErC.jpg "Image with caption")
_Fig. 2 - It will look like this after you're done creating your Virtual Machine_

## 2.) Configuring your Virtual Machine's network
![Image with caption](https://i.imgur.com/PivsumL.jpg "Image with caption")
_Fig. 3 - Right click your Virtual Machine(Codeception), select settings -> network -> adapter 1, then enable network adapter and changed Attached to: FROM NAT to Bridged Adapter_

## 3.) Installing Centos 7 Minimal in your Virtual Machine
![Image with caption](https://i.imgur.com/mSMSxFh.jpg "Image with caption")
_Fig. 4 - Double click your Virtual Machine, then find your Centos 7 Minimal .iso file_

![Image with caption](https://i.imgur.com/Y8z7nW7.jpg "Image with caption")
_Fig. 5 - Navigate with your up and down arrow keys, then select Install Centos 7_

![Image with caption](https://i.imgur.com/NURsC20.jpg "Image with caption")
_Fig. 6 - Just click that Continue button_

![Image with caption](https://i.imgur.com/MFIhs4Q.jpg "Image with caption")
_Fig. 7 - Click NETWORK & HOST NAME_

![Image with caption](https://i.imgur.com/VW5U2YQ.jpg "Image with caption")
_Fig. 8 - toggle ON switch to automatically set up your network settings_

![Image with caption](https://i.imgur.com/0wmOY46.jpg "Image with caption")
_Fig. 9 - You should see your IP there_

![Image with caption](https://i.imgur.com/w8LB6fr.jpg "Image with caption")
_Fig. 10 - Set up your ROOT password and user account for the server_

![Image with caption](https://i.imgur.com/bunSODw.jpg "Image with caption")
_Fig. 11 - This is how it should look like after setting up your root password and user account, reboot after Centos 7 Installation_

## 4.) Accessing your Centos 7 Minimal server via puTTy
![Image with caption](https://i.imgur.com/ef4zXOK.jpg "Image with caption")
_Fig. 12 - Login using your root/user account, type ip a in your centos 7 minimal OS, it will show your IP address. you'll need it to access your server via PuTTy_

![Image with caption](https://i.imgur.com/gfy32rz.jpg "Image with caption")
_Fig. 13 - Open your puTTy, then type in your IP address in the IP Address textbox, then click open. sorry about the background lol_

![Image with caption](https://i.imgur.com/M73qYl0.jpg "Image with caption")
_Fig. 14 - Just click Yes_

![Image with caption](https://i.imgur.com/Ac5n9o9.jpg "Image with caption")
_Fig. 15 - Tadaa! we can now login to our server via puTTy! Enjoy!_

## 5.) Initial setup
### Disable SELINUX
`command : sestatus`

![Image with caption](https://i.imgur.com/zYiWekN.jpg "Image with caption")
_Fig. 16 - Check if SELINUX is enabled_

`command : vi /etc/sysconfig/selinux`

![Image with caption](https://i.imgur.com/1OdR0Hi.jpg "Image with caption")
_Fig. 17 - vi /etc/sysconfig/selinux results, click I in your keyboard to insert texts_

![Image with caption](https://i.imgur.com/Ta9AAGe.jpg "Image with caption")
_Fig. 18 - selinux=disabled, after editing press esc button, type :wq then click enter to save and exit_

![Image with caption](https://i.imgur.com/qxnZffs.jpg "Image with caption")
_Fig. 19 - This is how it should look like even after editing the selinux file, because you need to reboot. to reboot, just type reboot then press enter_

![Image with caption](https://i.imgur.com/JQp3wFs.jpg "Image with caption")
_Fig. 20 - Selinux is now disabled_

### Disable FIREWALL
`command :` <br>
`systemctl disable firewalld` <br>
`systemctl stop firewalld` <br>
`systemctl status firewalld` <br>

![Image with caption](https://i.imgur.com/KoS7KiZ.jpg "Image with caption")
_Fig. 21 - Result after executing above command_

_Thank you for reading!_