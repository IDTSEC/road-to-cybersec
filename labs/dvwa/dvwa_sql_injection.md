# DVWA SQL Injection - test
target: DVWA  
date: 12.9.2025

### Summary
A quick SQL injection test against DVWA (sec level: low). The app accepted unsanitized input in the User ID field, which allowed injection of SQL to enumarate database rows.

### Vulnerability
SQL Injection - authentication bypass/data extraction

### Environment
- Kali Linux (local VM)
- Apache2 + PHP (with mysqli) + MariaDB
- DVWA configured with a dedicated user + database

### Steps performed
- Open DVWA: http://127.0.0.1/DVWA/login.php
- Login using default credentials: admin/password
- While in DVWA: security set to LOW
- Submit 1' OR '1'=1 (SQL Injection) -> return multiple user records

### Result?
<img width="317" height="447" alt="newsql" src="https://github.com/user-attachments/assets/fd97c375-274e-46b6-93f7-1c9df43106f7" />

## Defense
Safe coding practices needed:
- prepared statements/parameterized queries (keeping data & SQL commands separate - even if the input is malicious, it won't change the meaning of the query, basically being treated just as text)
- input validation & sanitization: checking that the user input is what we expect (letters/numbers for username), and cleaning it to remove dangerous characters
