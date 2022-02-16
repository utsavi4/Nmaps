# Nmaps 
Introduction

Nmap is short for Network Mapper. It is an open-source security tool for network exploration, security scanning, and auditing. However, the Nmap command comes with lots of options that can make the utility more robust and difficult to follow for new users. The purpose of this guide is to introduce a user to the Nmap command line tool to scan a host or network to find out the possible vulnerable points in the hosts. You will also learn how to use Nmap for offensive and defensive purposes. 

Utility

 It was designed to rapidly scan large networks, although it works fine against single hosts. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running, what type of packet filters/firewalls are in use, and dozens of other characteristics. While Nmap is commonly used for security audits, many systems and network administrators find it useful for routine tasks such as network inventory, managing service upgrade schedules, and monitoring host or service uptime. It is seldom used to answer the following questions:
1. Find running computers on the local network
2. What IP addresses did you find running on the local network?
3. Discover the operating system of your target machine
4. Find out what ports are open on the machine that you just scanned?
5. See if the system is infected with malware or virus.
6. Search for unauthorized servers or network service on your network.
7. Locate and remove computers which don’t meet the organization’s minimum level of security.

Auditing the security of a device or firewall by identifying the network connections which can be made to, or through it. Identifying open ports on a target host in preparation for auditing.Network inventory, network mapping, maintenance and asset management. Auditing the security of a network by identifying new servers. Generating traffic to hosts on a network, response analysis and response time measurement. Finding and exploiting vulnerabilities in a network. DNS queries and subdomain search

Characteristics and Features 

1. Host discovery – Identifying hosts on a network. For example, listing the hosts that respond to TCP and/or ICMP requests or have a particular port open.
2. Port scanning – Enumerating the open ports on target hosts.
3. Version detection – Interrogating network services on remote devices to determine application name and version number.
4. TCP/IP stack fingerprinting – Determining the operating system and hardware characteristics of network devices based on observations of network activity of said devices.
5. Scriptable interaction with the target – using Nmap Scripting Engine(NSE) and Lua programming language.
6. Nmap can provide further information on targets, including reverse DNS names, device types, and MAC addresses.

# python3-nmap
A python 3 library which helps in using nmap port scanner. The way this tools works is by defining each nmap command into a python function making it very easy to use sophisticated nmap commands in other python scripts. Nmap is a complicated piece of software used for reconnaissance on target networks, over the years new features have been added making it more sophisticated. With this python3-nmap we make using nmap in python very easy and painless For example in nmap if you want to scan for common ports you would to something like this

$ nmap your-host.com --top-ports 10

But in this python3 script again it's very easy you just do something like this,



    import nmap3
    nmap = nmap3.Nmap()
    results = nmap.nmap_dns_brute_script("your-host.com")



And you would get your results in json


    {
        "address": "mail.your-host.com",
        "hostname": "68.65.122.10"
    },
    
    {
        "address": "www.your-host.com",
        "hostname": "5.189.129.43"
    }
   


How to use python3-nmap

Using this scripts is very easy, though it assumes you have nmap already installed, as it is the primary dependence required. Also this tools supports both windows and linux, it's cross platform so to say.







