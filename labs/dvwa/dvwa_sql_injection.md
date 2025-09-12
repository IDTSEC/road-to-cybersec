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
<img width="466" height="471" alt="sqli" src="https://github.com/user-attachments/assets/eb7c24d8-9e0f-417a-88fd-d3a6e182bde2" />
