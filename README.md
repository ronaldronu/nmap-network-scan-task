# nmap-network-scan-task
Cybersecurity internship task to scan local network for open ports using Nmap
# Task 1: Local Network Port Scanning

## Tools Used
- Nmap
- Wireshark (optional)
  
#NMAP                                 #WIRESHARK ANALYSIS
-----                                 -------------------
## Local IP Range                 - Captured packets during TCP SYN scan using Wireshark.
`192.168.59.2`                    - Filtered SYN packets using `tcp.flags.syn == 1 and 
                                    tcp.flags.ack == 0`
                                  - Observed open ports (SYN-ACK responses) and closed ports (RST 
                                    responses).                   

## Commands Used
```bash
nmap -sS 192.168.59.2 -oN scan_result.txt
===================================================
Wireshark - tcp.flags.syn == 1 and tcp.flags.ack == 0

