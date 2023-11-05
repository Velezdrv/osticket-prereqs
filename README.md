<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Set up an Azure Virtual Machine (VM) environment (Windows 10 4 vCPUs Recommended)
- osTicket Installation Files (Download these files on your Azure Virtual Machine)
- Enable IIS in I.I.S.
- Install Web Platform Installer
- Install MySQL and set up username and password
- Install C++ Redistributable
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

- Install/Enable IIS
- Control Panel, turn on or off windows features, Internet Information Services, World Wide Web Services, Application and Development Features, check CGI, Common HTTP Features and check all.

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/43bbbdd1-3f21-4c3d-9a99-72a90490f0e3)

- Verify IIS, web browse 127.0.0.1 (Local Host)
- Install PHP Manager https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/5aaa780a-00d5-4240-b62b-e35c976811e3)

- Install Rewrite Module https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/0a4ef878-dc3a-4911-b619-d9d96792f6fb)

- Create PHP Folder in C Drive
- Install PHP and Extract all to C Drive PHP Folder https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=drive_link

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/dcbd2c2d-1800-4990-affd-d4dd23a71ae8)

- Install Microstoft Visual C++ Redistributable https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/5b2175e1-b325-4cfb-a762-40668f36f5ff)

- Install MySQL Server https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link
- Standard Configuration, Root User Name and setup password

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/77a7f0cc-8988-472a-bc04-748cacb840ed)

- Run IIS as Administrator
- Open PHP Manager and Register New PHP Version

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/65dd8fdc-2d95-4118-87d2-62c8642317e4)
- Recommended (Restart IIS Manager after any changes are made.)

- Install osTicket https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link
- Drag and Drop Upload Folder to c:\inetpub\wwwroot
- Rename to osTicket

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/90a0e6f7-6305-478a-b4e2-bc783b466182)

- Launch osTicket, Left side tab click Sites, Default, osTicket then Browse *:80
- Enable Extensions in osTicket
- Sites. Default. osTicket, PHP Manager, Enable or disable Extensions
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/d1894407-9e58-4b6c-94c4-9fdb590d424d)

- Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php (Just delete sample in the name)

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/4d0d060c-d90e-418f-8a67-d3a297c4f7a4)

- Set Permissions To Everyone
- Right Click ost-config.php and go to properties
- Click Security then Advance and disable inheritance
- Add, Select a Principal and enter a Name, Everyone and click ok
- Give Everyone Full Control

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/336b4b1e-3373-48bc-8fde-fd38525b82bf)
  
- Continue Setup of osTicket
- Create Helpdesk Name
- Default Email (Where Customers emails will be received)

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/ca8a2437-48cb-4c41-aa53-5a723c219aa8)


- Set up User Profile and Install HeidiSQL https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/1f78c0ac-a1b8-4d13-9845-d5af29f6b2a3)

- Create New Session With User created during MySQL

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/f4c21546-cf34-4c85-9dfc-fe5496e027db)

- Create New Database for osTicket

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/ab341588-808c-40c4-8f9f-c5b1bcdbabaa)

- Delete Setup Folder in c:\inetpub\wwwroot\osTicket
- Reset Permissions on C:\inetpub\wwwroot\osTicket\include\ost-config.php to read only

![image](https://github.com/Velezdrv/osticket-prereqs/assets/147437260/60080701-2386-4660-99ea-b6370933512e)
