# Network-Traffic-Analysis-With-WireShark
Used Wired Shark to analyze traffic to identify login attempts, DNS queries, and plaintext credentials.


🕵️ Wireshark Network Traffic Analysis Lab
📌 Objective

This lab demonstrates the use of Wireshark to capture and analyze network traffic. The goal is to identify DNS queries, HTTP requests, and plaintext credentials in transit.

⚙️ Tools Used

Wireshark (Packet capture & analysis)

Web Browser (to generate traffic)

🧪 Steps Performed
1. Capture Setup

Installed Wireshark on a Windows machine.

Selected the active Wi-Fi/Ethernet interface.

Began capturing live traffic.

2. Traffic Generation

Browsed multiple websites.

Conducted Google searches.

Logged into a test site using HTTP (not HTTPS) to observe plaintext traffic.

3. Packet Filtering

Applied Wireshark filters to narrow down results:

DNS Queries → dns

HTTP Traffic → http

POST Requests (logins/forms) → http.request.method == "POST"

My machine’s IP only → ip.addr == <MY_IP_ADDRESS>

4. Analysis

Identified DNS queries showing domains the system contacted.

Observed HTTP GET requests retrieving web pages.

Captured an HTTP POST request that revealed plaintext username and password fields.

5. Evidence Collected

Saved packet capture as .pcap.

Documented findings with screenshots.

📊 Findings

DNS Analysis: System queried multiple domains during browsing activity.

HTTP vs HTTPS: Credentials were visible in HTTP traffic but hidden in HTTPS sessions.

Security Risk: Use of unencrypted connections exposes sensitive user information.
