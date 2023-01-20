# Scenario
IP address of nsf server is 192.168.57.14  
server's name is dev
# Steps to enumerate nfs

In Kali terminal:  

*└─# showmount -e 192.168.57.14*  
*Export list for 192.168.57.14:*
*/srv/nfs 172.16.0.0/12,10.0.0.0/8,192.168.0.0/16*

Now we will create a dev directory in /mnt to mount the result  
*┌──(root㉿kali)-[/mnt]*  
*└─# mkdir /mnt/dev*  

*┌──(root㉿kali)-[/mnt]*  
*└─# mount -t nfs 192.168.57.14:/srv/nfs /mnt/dev/*  

*┌──(root㉿kali)-[/mnt]*  
*└─# cd /mnt/dev/*  

*┌──(root㉿kali)-[/mnt/dev]*  
*└─# ls*  
*save.zip*  
