# Context
This bash script is based on Heath Adams's script - as part of his PEH course.  
The objective of the script is to automate the following steps:
1. It harvests subdomains of the provided domain, using **assetfinder**
2. It only keeps alive subdomains, using **httprobe**
3. It checks the alive subdomains for possible domain takeover, using **subjack**
4. It scans the alive subdomains for 1,000 common ports, using **nmap**
5. It scraps wayback data of the alive subdomains, using **waybackurls**  
*Note: This can take a lot of time -> comment out these lines if you don't need them.*
6. It runs **gowitness** against the alive subdomains and takes screenshots of them

# Requirements
This script requires the following tools. Make sure you install them before running the script.
1. assetfinder
2. httprobe
3. subjack
4. nmap
5. waybackurls
6. gowitness

# Usage
./autorecon.sh \<domain>
  * Example: *./autorecon.sh kientrunghoang.com*  

To view the screenshots of the subdomains:  
  * *gowitness server*
  * Start Firefox, go to *http://localhost:7171/*

# Known issues
## Gowitness does not work because of nmap delay
I know it sounds weird, but it is exactly what happened to me. It took me as a layman a few hours to figure this out :).  
So if it happens to you, you have 2 choices:
1. Increase --timeout in gowitness command
2. Run gowitness out of script 
  * *gowitness file -f \<domain>/recon/httprobe/alive.txt*  
    replace \<domain> with the domain name





