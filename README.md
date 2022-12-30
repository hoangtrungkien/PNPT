# Objective
This repository is where I store my cheat sheet for PNPT 2022 course.

# Disclaimer
All the info here is based on my personal experience and knowledge I gather from the Internet. Use it at your own risk!

## Reconnaissance

### nmap

#### Scan 1 machine:
nmap -T4 -p- -A {victim's IP address}
  
If the machine does not respond to ICMP ping test -> add -Pn

### Enumerate samba version with Wireshak and smbver.sh
In case nmap cannot tell us the version of samba (port 139 or 445), we need to use smbver.sh + Wireshark  

Download the script at: https://github.com/rewardone/OSCPRepo/blob/master/scripts/recon_enum/smbver.sh  

Start Wireshark - click the sharkfin icon to start capture  

./smbver.sh {victim's IP address} 139 {or 445}  

Back to Wireshark - stop capture, scroll to top - look for the first SMB packet - right click it - Follow - TCP Stream  
We will see the samba version.

Alternative:
You can use metasploit: auxiliary/scanner/smb/smb_version  

