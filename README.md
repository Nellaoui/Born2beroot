# Born To Be Root

# 👹                           **Table of content**                              👹

# What is Virtual Machine (MC) ❓

> compute resource that. uses software instead of a physical computer to run programs and deploy one or more virtual machine run on physical “host” machine. Each virtual machine runs its own operating system and separately from the other VMs.
> 

<aside>
<img src="https://www.notion.so/icons/cursor_gray.svg" alt="https://www.notion.so/icons/cursor_gray.svg" width="40px" /> Compute resource is a service is that provide virtual equipment (Compute resources) by combining CPUs. Memory. and Disk to create virtual machine, Compute resource are provided by virtualizing servers and storage devices shared by multiple users.

</aside>

# Root 💥

> **Root** is the name of the most powerful account on a Debian system. The root user account can do everything on the machine. Root is also known as super user and administrator. Root's home (~) folder is /root.
> 

<aside>
<img src="https://www.notion.so/icons/cursor_gray.svg" alt="https://www.notion.so/icons/cursor_gray.svg" width="40px" /> In a terminal : you can use [su](https://manpages.debian.org/man/1/su) to change your identity to root. However, it's recommended to configure and use [sudo](https://wiki.debian.org/sudo)  to run a given command.

</aside>

# LVM(Logical Volume Management) 🚨

> It is a system of managing logical volumes, or filesystems, that is much more advanced and flexible than the traditional method of partitioning a disk into one or more segments and formatting that partition with a filesystem.
> 

<aside>
<img src="https://www.notion.so/icons/cursor-click_gray.svg" alt="https://www.notion.so/icons/cursor-click_gray.svg" width="40px" /> **filesystems** : used to handle the data management of the storage. It helps to arrange the file on the disk storage. It manages the file name, file size, creation date, and much more information about a file.

</aside>

# UFW(Uncomplicated fire wall) 🧱

> is a [firewall](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands), it stands for uncomplicated firewall a firewall is a network security system that prevents unauthorized access from entering a private network by filtering the incoming network data, based on its rules (access control list, contains IP, protocol, destination and port)
> 

# Secure Shell (SSH) ☎️

> is a network protocol  that gives users particularly system administrators, a secure way to access a computer over an unsecured network. and allows users to control and modify their severs over the internet due to an authentication mechanism. Provides a mechanism to authenticate user remotely, transfer data from the client to the host, and return a response to the request made by the client.
> 

<aside>
<img src="https://www.notion.so/icons/cursor_gray.svg" alt="https://www.notion.so/icons/cursor_gray.svg" width="40px" /> SSH uses encryption techniques to ensure that all client-to-host and host-to-client communications are done in encrypted form. One of the advantages of SSS is that a user using Linux or MacOS can use SSH on their server to communicate with it remotely through their computer terminal. Once authenticated, that user will be able to use the terminal to work on the server.

</aside>

## Port 🛑

> A port is a Virtual point where network connections start and end, with each port assigned a number, Most are reserved for certain [protocols](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/).
> 

### What is a port number ❓

> Ports are standardized across all network-connected devices, with each port assigned a number, Mosts ports are reserved for certain Protocols.
> 

## TCP 🚦

> TCP stands for Transmission Control Protocol a communications standard that enables application programs and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over network.
> 

# AppArmor 🧨

> `AppAromor` is a **Mandatory Access Control** security. in fact `AppArmor` allows the system administrator to restrict the action that process can perform. 
Example : if an installed application can take photos by accessing the camera application but the administrator denies this privilege the application will not be able to access the camera application, if a vulnerability occurs (some of the restricted tasks are performed), `AppArmor` blocks the application so that the damage does not spread to the rest of the system .in AppArmor, processes are restricted by profiles. profiles can work in complain-mode and in enforce-mode . 
In enforce mode, `AppAromor` prohibits applications from preforming restricted tasks. In complain mode, `AppArmore` allows application to do these tasks, but creates a registry entry to display the complaint
> 

<aside>
<img src="https://www.notion.so/icons/cursor_gray.svg" alt="https://www.notion.so/icons/cursor_gray.svg" width="40px" /> AppArmor `profiles` are simple text files located in `/etc/apparmor.d/`.
The files are named after the full path to the executable they profile replacing the “/” with “.”. For example `/etc/apparmor.d/bin.ping`
 is the AppArmor profile for the `/bin/ping`command.

</aside>

# Commands & Packages 💢

## Lsblk

<img width="815" alt="Screen_Shot_2022-11-27_at_11 54 11_PM" src="https://user-images.githubusercontent.com/103364555/209560718-7b3fd594-aeb4-4fcd-b27f-3f4484d258a6.png">
---

`lsblk` produce a tree-like output including all the block devices attached to the operating system. its very useful to identify devices and their partition.

---

`sda5` : is a standard partition, and we can understand from the graph, it has some children devices. The first one is a `sda5` identified by `sda5_crypt`. Being the system installed on a lvm on `sda5_crypt`, the `sda5_crypt` is marked as a physical volume, and contains some logical volumes.

---

`lsblk -p` for display path of devices.

---

`MAJ:MIN` is the numbers are used by the `karnel` to identify the devices, the first number is specifying the device type.

---

`RM` its indicate for removable devices RM{0, 1} = (1 : for removable).

---

`SIZE` if you not understand this by default, you need a doctor ASAP.

---

`RO` its indicate for read-only or not like `RM`, `RO{0,1}` = (1 : mean. the device is read-only).

---

`TYPE` we mentioned before this is for identify the device or partition type, For example `crypt` is for identify the `sda5_crypt` while lvm is for `identify logical volume device`, and disk is used for `raw block` like. `sda`

# Partition

`Boot` : The boot partition is the Disk partition that contains the operating system fold also is a primary partition that contains the boot loader.

`Swap` : The primary function of swap space is to substitute disk space for RAM memory when real RAM fills up un more space is needed.

# `MOUNTPOINT`

- / : represents the root directory. All other and directories are contained in the root directory.
- /root : But don’t get / confused with /root!/ /root is the home directory of the root user, or superuser. It’s a directory called /root, but it isn’t the root directory.
- /bin : this directory contains “binaries,” executable files which are essential  to the operation of the system administrator might want to use.
- /sbin this directory contains “system binaries”, things that the root user or system administrator might want to use.
- /user : contains most of the files you’ll be interested in. It has many subdirectories
    
    <aside>
    <img src="https://www.notion.so/icons/cursor-click_gray.svg" alt="https://www.notion.so/icons/cursor-click_gray.svg" width="40px" /> `/user/bin` and `/user/sbin` are pretty much like `/bin` and `/sbin`, except that eh directories in / user are not considered “essential to the operation if to the system”
    
    </aside>
    
     while not essential to get the computer operating `/user` does contain the applications you’ll use to get real work done. also in `/user` you’ll find the `/user/info`, and `/user/doc` directories - these contain manual pages, info pages, and other documentation, respectively
    
- /etc : contains all the system-wide configuration files, whenever you want to change something that affects all users of your computer - such as how you connect to the internet, or what kind of video card you have - you’ll probably have to log as root and change a file in `/etc` .
- /tmp : here you’ll find temporary files, most of them created by system. this directory is generally erased on a regular basis, or every time you reboot the system. You can create files here if you want , just be aware they might get deleted.
- /var : contains “variable” files, that the system changes automatically,. For example incoming mail is stored here. The system keeps a log of its actions here. there are a number of other automatically generated files here as well. You’ll mostly be interested in the contents of /var/log, where you can find error messaged and try to figure out what you’re system’s up if something goes wrong.
- /srv : contains site-specific data which is served by this system.
- /var/log : the records that linux stores for administrators to keep track and monitor important events about the server, kernel, services, and applications

## Sudo 💢
![ezgif-5-96cf850ba0](https://user-images.githubusercontent.com/103364555/209560961-e2308579-a5e0-442a-92a3-f25d087e59d9.png)

> is a command stand for “super user do!” it give power to  users to run some commands as root.
> 

![fun right ?]

## Apt - Aptitude

## Apt

> Advanced Packaging Tool utility for installing, updating, removing, and otherwise managing packages in Debian and related Linux distributions.
> 

<aside>
💡 Most of the apt commands must be run as user with `sudo` privileges.

</aside>

### Aptitude

> it also advanced packaging Tool. based front-end to nymerous Apt libraries, which are also used by Apt, the default Debian package manager. Aptitude based and run from a terminal.
> 

### Differences between Apt and Aptitude

- The first difference you will notice is that APT is a lower-level package manager, and Aptitude is a high-level package manager. This means that APT can be used in other higher-level package managers.
- Apt It has many features reverse Aptitude for example apt —help —purg …when you install a packages using the apt then apt if found a wrong advantages, does nothing unlike Aptitude if found wrong he update them and install the package without any problem.
- when you want to upgrade system by (apt upgrade), then apt Updates packages except dor packages related to a system 
`Exemple :` if you are on version 12 you will not convert to version 13 Unless you use apt `dist-upgrade.`
then aptitude upgrade without any problem
    
![1_vRgjWvlyZsTHhO3_4Qsvlg](https://user-images.githubusercontent.com/103364555/209561045-3a37d8b4-593f-4299-8706-3b7b45901072.png)
### hostname

> The hostname is used to distinguish devices within a local network. In addition, computers can be found by others through the hostname
> 

```jsx
sudo hostnamectl set-hostname <name>
or 
sudo vi /etc/hostname
```

### Systemctl

> systemctl command is a utility which is responsabile for examing and controling the system and service manager.
> 

### addgroup & adduser

Add user to sudo group by following command :

```jsx
	$> adduser <user> sudo
```

verify whether user was successfully

```jsx
	$>cat /etc/group | grep sudo
```

create new user42 group :

```jsx
	$> sudo addgroup <group>
```

add user to user42 group : 

```jsx
	$> sudo adduser <user> <group>
```

verify whether user was successfully added :

```jsx
	$> cat /etc/group | grep <group>
```

## **libpam-pwquality**

libpwquality's purpose is to provide common functions for password quality checking and also scoring them based on their apparent randomness. The library also provides a function for generating random passwords with good pronounceability.

This module can be plugged into the password stack of a given service to provide some plug-in strength-checking for passwords

## Visudo

### [**Visudo**](https://www.digitalocean.com/community/tutorials/how-to-edit-the-sudoers-file)

## Sudoers

we will discuss how to correctly and securely obtain **root** privileges, with a special focus on editing the `/etc/sudoers`file.

as we know to become Root we use the commend Below :

```jsx
	$ su
```

### so what is Visudo ?

The `sudo` command is configured through a file located at /etc/sudoers.

 

<aside>
💡 Warning : never edit this file with a normal text editor ! Always use the `visudo` command instead

</aside>

# Files of Debian 🧰

[MONTPOINT](https://github.com/Nellaoui/Born2beroot/blob/main/README.md#mountpoint)

## /etc/group Columns

Use the following command to list groups on your system.

```jsx
$ cat /etc/group
```

But what do the columns of the group file even represent?
![etc-group-file](https://user-images.githubusercontent.com/103364555/209561126-7f01f879-6b4b-4c9c-96c3-5e708daa10a5.png)

<aside>
💡 Note : the password field is not used most of the time, it is reserved to create privileged groups on your system.

</aside>

to achieve that, you can either **use the cut command or the AWK command or Grep.**

```jsx
$ cat /etc/group | cut -d: -f1
```

```jsx
$ cat /etc/group | awk -F: '{print $1}'
```
