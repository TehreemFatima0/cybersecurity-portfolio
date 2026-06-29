# Lab: Local Web Application Traffic Analysis & Packet Sniffing

**Tools Used:** Wireshark, XAMPP, Apache, MySQL  
**Environment:** Localhost Sandbox Environment  

---

## Objective
Designed a local full-stack environment to analyze how data flows between a web server and a database, specifically observing how unencrypted HTTP forms expose sensitive authentication parameters in transit.

## Methodology & Infrastructure Setup
* **Environment Hosting:** Deployed a local web application utilizing **XAMPP** to run an Apache web server and a **MySQL** backend.
* **Traffic Capture:** Initialized **Wireshark** to monitor local loopback traffic (`adapter for loopback traffic` on localhost) to intercept communication between the browser client and the local server.
* **Insecure Stream Isolation:** Generated mock login traffic through an unencrypted HTTP POST form, then applied targeted Wireshark display filters to isolate the raw TCP streams payload.

## Key Outcome & Security Insight
Successfully isolated the specific network packets carrying the form submission. By parsing the unencrypted data payload, I extracted the plain-text credentials (username and password) directly from the stream. 

This self-constructed lab practically demonstrated the critical risk of clear-text data transmission on local infrastructure and highlighted the immediate necessity of implementing cryptographic layers like TLS/HTTPS, even in development environments.
