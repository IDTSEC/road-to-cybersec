# Nmap scan - scanme.nmap.org

## What did I scan?
I used Nmap to scan the domain 'scanme.nmap.org' -- a legal test host provided by the Nmap team for scanning practice.

## What scans did I perform?
- **Ping Scan** to check if the host was up
- **Version Detection (-sV)** to identify running services/versions
- **Aggresive Scan (-A)** for deeper OS and service detection

## What did I learn?
Nmap is a powerful tool for network reconnaisance (opens ports, identifies services and their versions, guesses the OS of a remote machine and much more)  
However:
- Nmap is to be used responsibly
- the output can be detailed and requires interpretation (some of which I'm still learning to fully understand)

## What did Nmap find?
Some of the results included:
- Detected OS: **Linux 5.0-5.14**, possibly **MicroTik RouterOS 7.2-7.5**
- Open ports like **22/tcp**(SSH), **80/tcp** (HTTP)
(since I'm still learning, I'm continuing to research how each port could be relevant from a blue-team perspective)

## Final notes  
My first scan with Nmap - I plan to repeat this and write more advanced summaries as I grow.
