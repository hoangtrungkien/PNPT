# Steps to set up an FTP server on Kali
pip3 install pyftpdlib  
python -m pyftpdlib -p21 --write

# Steps to access the FTP server from a Windows machine
Assumption: Kali machine: 1.2.3.4  
Open command line  
ftp 1.2.3.4  
Name: Anonymous  
Password: \<press enter>  

# Steps to transfer file from Windows machine to FTP server on Kali
put \<file name>
