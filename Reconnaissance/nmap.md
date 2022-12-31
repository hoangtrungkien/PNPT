# Scan 1 machine:
nmap -T4 -p- -A <victim's IP address>
  
If the machine does not respond to ICMP ping test -> add -Pn

If we want to show all vulnerabilities of the machine use --script vuln

Note that it may take some time (a few minutes).
