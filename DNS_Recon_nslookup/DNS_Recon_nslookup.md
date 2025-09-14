## DNS Recon - nslookup project (SOC-style)

# Summary
This small lab demonstrates DNS reconnaissance w/ nslookup.
Target used: example.com (reversed IANA domain used for testing; safe example)

# What's the connection with SOC?
- DNS records are frequently used in phishing, C2 infra and suspicious domain investigations.
- DNS enrichment (A, MX, NS, TXT, PTR) is often performed to assess suspicious domains

# Files:
Raw DNS outputs:
- '1_a_record.txt'
- '2_mx.txt'
- '3_ns.txt'
- '4_txt.txt'
- '5_soa.txt'
- '6_aaaa.txt'  
Reverse lookups:
- 'ips.txt'  
- '7_reverse.txt'  
Authoritative queries:  
- '8_soa_via_ns.txt'  
- '9_any_via_ns.txt'  
HTTP headers for resoled IPs  
- '11_http_headers.txt'  
- 'findings_summary.txt' : readable summary  
- 'nslookup_session.txt' : terminal transcript  
- 'run_nslookup_soc.sh' : optional automation script  

## (some) commands used
'''bash
# Basic A record
nslookup example.com > 1_a_record.txt

# MX / NS / TXT / SOA / AAAA
nslookup -type=mx example.com > 2_mx.txt  
nslookup -type=ns example.com > 3_ns.txt  
nslookup -type=txt example.com > 4_txt.txt   
... etc
