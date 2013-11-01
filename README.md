dahua_dvr_auth_bypass
=====================

Dahua CCTV DVR Authentication Bypass Metasploit Scanning Module

This is a Metasploit module that scans for and exploits Dahua and Dahua rebranded CCTV DVRs.

Installation:

- git clone https://github.com/depthsecurity/dahua_dvr_auth_bypass.git
- Copy dahua_dvr_auth_bypass.rb file to Metasploit modules directory 
  (e.g. /root/.msf4/modules/auxiliary/scanner/misc/dahua_dvr_auth_bypass.rb)

Standard Functionality Includes:

- It's a scanning module so obviously it can handle one or more IP addresses to identify DVRs on large networks
- Retrieve version and serial number (Seems to only work on particular versions)
- Retrieve email settings (SMTP server, destination address, SMTP credentials)
- Retrieve DDNS settings (DDNS service, DDNS server, DDNS port, DDNS credentials)
- Retrieve NAS settings (FTP server, FTP port, FTP credentials)
- Retrieve camera channel names
- Retrieve DVR users (usernames, hashed passwords, rights, and descriptions)
- Retrieve DVR user groups

Options Include:

- Reset the password for particular user (may be version dependent)
- Clear the DVR logs (may be version dependent)

Future Functionality:

- Check for telnet and utilize known default root password to gain telnet shell
- Issue UPNP request to open telnet to public access, then get telnet shell
- Check retrieved hashes for known default hash values (888888, 666666, admin, etc)
- Identify DVR password hash mechanism for cracking in JTR
