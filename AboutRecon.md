# For bug bounty program

- nmap -A -F -T1 10.10.10.223 -v

  - `-F`: will only scan the top 100 ports
  - `T5`: fast network scanning, use for CTF, might miss some ports
  - `T1`: slow network scanning, stealthy to not get noticed as intruder
    
Expected Output:

<img width="627" alt="image" src="https://github.com/user-attachments/assets/964b8b6c-67d8-470c-b38f-4098cb239d7e" />

# For CTF

- nmap -A -p -Pn 10.10.223 -v
  
