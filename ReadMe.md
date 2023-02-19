# Documentation of Creating Small Business Network Infrastructure

Networking lab project performed while at Divergence Academy.

Worked in a five-man team to create an SMB network with a LAN, DMZ, and Guest network. Used a GNS3, a network simulation environment, 
to deploy services across multiple servers including: a Windows domain controller and DNS environment, an IIS web server, a Windows FTP server, 
a Win10 workstation, and a LAMP web server running on Ubuntu 18.04 hosting a DokuWiki documentation site. Configured and utilized a FortiGate 
firewall with a VIP for the DMZ web server.

## Part 1: Standing Up the Network
![Starting Network](https://github.com/zachparker2014/Networking_Lab/blob/main/Images/NTNT%20Project-Stage1.drawio.png)

The first task was to build out the starting network shown above to match the basic network shown below.
1. Added the new devices to the lab workspace in GNS3.
2. Configured the LAN network on the firewall through the CLI.
3. Added a Win10 workstation to the LAN network.
4. Connected to the firewall GUI from the Win10 workstation.
5. Completed the network setup through the firewall GUI.

![Part 1 Network Setup](https://github.com/zachparker2014/Networking_Lab/blob/main/Images/NTNT%20Project-Stage2.drawio.png)
## Part 2: Setting Up the Domain Controller
Built a windows domain for the customers small business envirmonment.
1.  Prepared the Windows 2012 server for the Domain Controller server role.
2.  Installed the “Active Directory Domain Services” server role.
3.  Created new AD user accounts.
4.  Prepared Win10 to join the local domain.
5.  Joined Win10 to the local domain.
## Part 3: Setting Up an IIS Server
Built a IIS webserver on Win2012r2 server, and joined the server to the domain
1.  Added the new server to the GNS3 Workspace.
2.  Prepared a Windows 2012 server to join the domain.
3.  Installed the “Internet Information Services” server role.
4.  Added a test webpage, and verified access over the LAN network.

![Part 3 Network Setup](https://github.com/zachparker2014/Networking_Lab/blob/main/Images/NTNT%20Project-Stage3.drawio.png)
## Part 4: Creating a LAMP Webserver and a Dokuwiki
Built a LAMP Webserver on Ubuntu server  located on the DMZ netwrok
1.  Prepared Ubuntu 18.04 server.
2.  Installed DokuWiki on the server.
3.  Configured DokuWiki.
4.  Setup a VIP for the public side of the webserver on the firewall.

![Part 4 Network Setup](https://github.com/zachparker2014/Networking_Lab/blob/main/Images/NTNT%20Project-Stage4.drawio.png)
## Part 5: Configuring an FTP Server
Built an FTP Server on a Windows 2012 server located on the DMZ netwrok.
1.   Prepared a Windows 2012 server.
2.   Installed the FTP service.
3.   Configured the FTP service to only be modified/viewed by the admin group.

![Part 5 Network Setup](https://github.com/zachparker2014/Networking_Lab/blob/main/Images/NTNT%20Project-Stage5.drawio.png)
## Part 6: Hardening the enviroment
In this part, the group broke up and researched multiple topics on hardening a network. The results were compiled into the "Hardening Research" document. 
My section was the "Hardening Ubuntu Server 18.04" portion.
1.  Added a page for notes in the wiki.
2.  Researched hardening a FortiGate firewall.
3.  Researched hardening Windows 10.
4.  Researched hardening Windows Server 2012.
5.  Researched hardening Ubuntu Server 18.04.
6.  Presented findings to the senior engineer.

[Hardening Research](https://github.com/zachparker2014/Networking_Lab/blob/main/Hardening%20Research.docx)
## Stage 7 Scanning the environment
Conducted a vulnerability scan on the WAN interface and network environment
1.  Connected the network to a Greenbone server.
2.  Created a target of the WAN interface IP for the firewall.
3.  Scanned the target.
4.  Documented the results and submitted to the senior engineer.

[Vulnerabilty Report](https://github.com/zachparker2014/Networking_Lab/blob/main/Vulnerabilty_Report.docx)
