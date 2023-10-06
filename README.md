![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/d2d59f3c-4908-415b-a257-a2d086e4e200)# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

## Google Hacking:
Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:
### site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/1064c96a-0216-4cb2-a9ca-b9baa681f558)
### filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/37018f7e-2e28-4b14-a1af-aa386bd33e7c)
### intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/3bc43654-c7fd-443a-b7a5-811072801cde)
### inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/ade8e3d5-f418-4a89-a0a2-e65d8e54ce6b)
### intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/c41a1516-ad6a-4396-b5ef-9e5928dd9520)

### link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/482f34dd-1a61-487d-901b-a84ff4c0b48d)

### cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/4bdcec0b-8b2e-4e72-8b16-55d9aacfe64e)
# DNS Enumeration
## DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:
![e3eh](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/7355fc54-f843-456c-b75a-dd816e8cb530)

![e3 1eh](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/a7c5233b-fef5-4290-875f-8b4a4f3e0ad6)

## dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.

![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/e657f41b-047f-402f-b4ea-330592e67806)

## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/70951f3f-aa57-429c-a91e-6f867d9de44d)
In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/7c2b1285-801e-42e2-8789-2e67293aee15)
select any username in the first column of the above file and check the same
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/618db5a1-e4b6-46ca-968f-9db99f8d4fa8)

# Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/e5da7ad5-196d-4ac2-8664-d8e88e501d76)

## Output
 ![e3 2eh](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/d808c30a-3b95-4052-be0a-7cb7af7d4abf)
## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
![image](https://github.com/Dhanashreemullaithasan/Enumeration/assets/94165415/9d79f6ad-9d38-43a2-9177-50f704f63c11)
## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

