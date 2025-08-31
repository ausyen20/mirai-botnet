Mirai Botnet

* This is strictly for Educational & Research purposes

## Mirai Botnet – Overview

Mirai is one of the most notorious Internet of Things (IoT) botnets, first discovered in 2016. It gained worldwide attention after being used in some of the largest distributed denial-of-service (DDoS) attacks ever recorded at the time, targeting major websites and internet infrastructure providers.

The botnet primarily propagates by scanning the IPv4 address space for devices running insecure Telnet services (TCP ports 23/2323). Using a hardcoded list of common default usernames and passwords, Mirai brute-forces its way into vulnerable IoT devices such as IP cameras, DVRs, and routers. Once compromised, these devices are enrolled into the botnet, which can then be remotely controlled by a command-and-control (C2) server.

Key characteristics of Mirai include:

Simple propagation mechanism – relies on weak or default credentials.

Modular design – loader, bot, and C2 components.

Self-preservation – kills processes of competing malware and binds Telnet ports to block reinfection.

Massive scale – capable of recruiting hundreds of thousands of IoT devices globally.

Since its source code was publicly released in late 2016, numerous variants have emerged, each building on Mirai’s original blueprint by adding new exploits, attack vectors, and evasion techniques. This has made Mirai not just a one-time incident, but a persistent foundation for IoT malware research.


## Aim:
The environment is design to test Mirai botnet in an isolated LAN environment. 

## Prerequisites:
- Virtualbox 7.0
- Host 5 Different Virtual Machines (VMs), 4 in Ubuntu 22.04 and 1 in Kali Linux (latest version is fine)
- Configure all with "Internal Network" named "inet", with optional "NAT" to install updates

## Topology:

Requirements (Before building and running this code, ensure you have the following installed on VM2 (except from Kali):
1. Use "sudo apt install ....":
- gcc - GNU Compiler Collection
- golang - Go programming language
- electric-fence - Memory debugging library
- mysql-server - MySQL database server
- mysql-client - MySQL database client
2. Run tools/db.sql
  mysql -u root -p <enter your password>
  source db.sql;



Credits to:
1. https://github.com/jgamblin/Mirai-Source-Code/ - Jerry Gamblin 
2. https://github.com/lejolly/Mirai-Source-Code/ - Lejolly (Joshua Lee) --> For attack-instructions & scanner-and-loader-instructions 
3. https://github.com/brcnitk/Mirai/ - Dr. B R Chandavarkar
4. https://github.com/Glowman554/mirai/ - Glowman554 
