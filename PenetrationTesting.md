# Nmap - Scanning Networks
1. Discover what hosts are running on the network
     - nmap -sn 10.0.2.0/24
     - `sn`: subnet
     - touches each host in turn using ICMP ping protocol to see if it responds
     - Nmap only reports the hosts that respond, providing their `IP addresses`
<img width="290" alt="image" src="https://github.com/user-attachments/assets/0fcacbcd-4c7f-4bee-8d5f-5e6f6f2d1ff0" />

Having identified which hosts are responding, we can probe the TCP and UDP ports to check what services are being presented
