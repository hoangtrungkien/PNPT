# Enumerate samba version with Wireshark and smbver.sh
In case nmap cannot tell us the version of samba, we can use smbver.sh + Wireshark  

1. Download the smbver.sh script at: https://github.com/rewardone/OSCPRepo/blob/master/scripts/recon_enum/smbver.sh  

2. Start Wireshark - click the shark fin icon to start capture  

3. *./smbver.sh \<victim's IP address> 139 {or 445}*  

4. Back to Wireshark - stop capture, scroll to top
5. Look for the first SMB packet - right click it - Follow - TCP Stream  
6. We will see the samba version.

**Alternative:**  
You can use metasploit: *auxiliary/scanner/smb/smb_version* 