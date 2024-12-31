# Nmap For bug bounty program

- nmap -A -F -T1 10.10.10.223 -v

  - `-F`: will only scan the top 100 ports
  - `T5`: fast network scanning, use for CTF, might miss some ports
  - `T1`: slow network scanning, stealthy to not get noticed as intruder
    
Expected Output:

<img width="627" alt="image" src="https://github.com/user-attachments/assets/964b8b6c-67d8-470c-b38f-4098cb239d7e" />

- Nmap tells which ports are open & what versions are running on target 

# Nmap For CTF

- nmap -A -p -Pn 10.10.223 -v
  
# Fuzzing for directories

- ffuf -w /usr/share/wordlists/dirb/common.txt -u http://tenet.htb/FUZZ -fc 403 -p 2
  - `p 2`: delay 2 seconds between requests. `p 1` means 1 second between requests
  - `fc 403`: filter out HTTP status codes from response. So for `fc 403` the response will not include the not found codes

- ffuf -w /usr/share/wordlists/dirb/common.txt -u http://tenet.htb/FUZZ -p 1
- ffuf -w /usr/share/wordlists/dirb/common.txt -u http://tenet.htb/FUZZ -p 1
