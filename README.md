# Cybersecurity-Internship-Task-1
## Nmap Local Network Scan
## Objective
The objective of this task was to learn how to discover open ports on devices within a local network to understand potential network exposure.
Tools Used
# Nmap: A free and powerful network scanning tool used to discover hosts and services on a computer network.
## Methodology :
  Installed Nmap: I installed Nmap from its official website as per the instructions.
  Found Local IP Range: I identified the local IP range to be scanned, which was 10.197.155.0/24.
  Ran the Scan: I executed a TCP SYN scan using the command nmap -sS 10.197.155.0/24.
  Noted IP Addresses and Open Ports: I reviewed the scan results to identify the hosts, their IP addresses, and the open ports found on each device.
  Researched Common Services: I researched the common services running on the identified open ports to understand their function and potential security implications.
# Scan Results :
The Nmap scan, which completed in 41.89 seconds, identified four hosts as being "up" on the network. The following open ports and services were discovered on each host:
 # **Host: 10.197.155.2
    7000/tcp: afsj-fileserver
    8001/tcp: vcom-tunnel
    8002/tcp: teradatardbms
    8080/tcp: http-proxy
 # * Host: 10.197.155.48
    53/tcp: domain
 # * Host: 10.197.155.189
    5060/tcp: filtered zip
 # * Host: 10.197.155.224
    135/tcp: msrpc
    139/tcp: netbios-ssn
    445/tcp: microsoft-ds
    554/tcp: rtsp
    8080/tcp: http-proxy
    1521/tcp: oracle
    2869/tcp: icslap
    3306/tcp: mysql
    6881/tcp: bittorrent-tracker
    7070/tcp: realsever
    9001/tcp: tor-orport
    10243/tcp: unknown
## Potential Security Risks and Analysis
The scan revealed several services that could pose security risks if not properly configured and secured. 
# For example:
MySQL (3306/tcp): An open MySQL port could be a target for brute-force attacks or exploits if it is not protected by strong credentials or restricted to specific IP addresses.
 * Microsoft-DS (445/tcp): This port is used for file and printer sharing. If it's exposed, it can be a vulnerability for exploits like the WannaCry ransomware.
 * HTTP-Proxy (8080/tcp): An unsecured proxy can be misused to access restricted content or launch attacks from a seemingly legitimate source.
 * Bittorrent-tracker (6881/tcp): The presence of this service indicates file-sharing activity, which can consume significant bandwidth and may expose the network to malicious content.
The findings demonstrate the importance of performing port scans as a basic network reconnaissance skill to understand network service exposure and identify potential vulnerabilities. It highlights that securing open ports is a critical aspect of network security.
