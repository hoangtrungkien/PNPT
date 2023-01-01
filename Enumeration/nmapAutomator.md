# Context
This bash script is used to automate enumeration.  
This is a summary of the main features:
1. Network : Discover all live hosts in the host's network (~15 seconds)
2. Port : Shows all open ports (~15 seconds)
3. Script : Runs a script scan on found ports (~5 minutes)
4. Full : Runs a full range port scan, then runs a thorough scan on new ports (~5-10 minutes)
5. UDP : Runs a UDP scan "requires sudo" (~5 minutes)
6. Vulns : Runs CVE scan and nmap Vulns scan on all found ports (~5-15 minutes)
7. Recon : Suggests recon commands, then prompts to automatically run them
8. All : Runs all the scans (~20-30 minutes)

# Requirements
This script requires the following tools. Make sure you install them before running the script.
1. nmap Vulners  
    * cd /usr/share/nmap/scripts  
          git clone https://github.com/vulnersCom/nmap-vulners.git  
          nmap --script-updatedb  

2. droopescan 
    * git clone https://github.com/droope/droopescan.git  
  cd droopescan  
  pip3 install -r requirements.txt

3. nikto, joomscan, odat, smtp-user-enum, ffuf
    * apt install \<packagename>


4. sslscan, wpscan, smbmap, enum4linux, dnsrecon, snmbcheck, snmpwalk, ldapsearch (installed with Kali)

# Usage
Please refer to Usage at https://github.com/21y4d/nmapAutomator
