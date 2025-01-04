# Nmap - Scanning Networks
1. Discover what hosts are running on the network (IP address scan of a business domain)
     - nmap -sn 10.0.2.0/24
     - `sn`: subnet
     - touches each host in turn using ICMP ping protocol to see if it responds
     - Nmap only reports the hosts that respond, providing their `IP addresses`
<img width="290" alt="image" src="https://github.com/user-attachments/assets/0fcacbcd-4c7f-4bee-8d5f-5e6f6f2d1ff0" />

Having identified which hosts are responding, we can probe the TCP and UDP ports to check what services are being presented

2. Port scan of active hosts (those that were reported in (1))
- Check the target on 10.0.2.32 for TCP ports using `-PS` option
     - nmap -PS 10.0.2.32
     - `-Pn` option is useful to scan a live system as it skips the ping check of the host, live system does not respond to ICMP ping
     
<img width="383" alt="image" src="https://github.com/user-attachments/assets/dc2b11b5-76d9-4126-a168-e4a3aa894073" />
- nmap -PS -Pn 10.0.2.38


- Check for open UDP ports
     - sudo nmap -sU 10.0.2.32 (for linux)
     -  nmap -sU 10.0.2.32 (for windows)
 
Additional Info on Verfiying Checksums on Windows after downloading Nmap:
Navigate to the directory of the downloaded file before extracting and run these commands, verify if they match the provided checksums
- CertUtil -hashfile nmap-7.95-setup.exe MD5
- CertUtil -hashfile nmap-7.95-setup.exe SHA256
<img width="684" alt="image" src="https://github.com/user-attachments/assets/00cb7f29-f511-4439-8622-f7043059b417" />

