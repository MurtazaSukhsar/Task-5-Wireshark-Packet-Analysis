Task 5 – Capture and Analyze Network Traffic Using Wireshark

📌 Objective
The objective of this task was to capture live network traffic using Wireshark, identify basic protocols, and analyze the captured packets.

🛠 Tools Used
- Wireshark 4.4.7 (Network protocol analyzer)
- Kali Linux (VMware environment)

📋 Steps Performed

1️⃣ Starting Wireshark Capture
- Opened Wireshark and selected the active interface `eth0`.
- Started capturing packets (Screenshot: Screenshot_2025-08-11_03_22_19.png).

2️⃣ Capturing Live Traffic
- While capturing, visited different websites and performed ping tests to generate various types of network traffic.
- Observed a mix of TCP, ICMP, and TLS traffic.
- Notable IPs in capture:
  - 192.168.71.130 (local host in VM)
  - External IPs like 23.58.31.18, 142.250.207.174, 104.18.38.233 (servers accessed)
- Example capture in progress:
  - TCP packets with ACK, FIN, and Keep-Alive flags
  - ICMP ping requests/replies
  - TLSv1.2 and TLSv1.3 encrypted traffic
(Screenshots: Screenshot_2025-08-11_03_23_55.png, Screenshot_2025-08-11_03_24_01.png, Screenshot_2025-08-11_03_24_50.png)

3️⃣ Filtering Specific Protocols
- Applied `http` filter to isolate HTTP requests and responses.
- Observed OCSP traffic for certificate status checks and plain HTTP requests.
(Screenshot: Screenshot_2025-08-11_03_25_08.png)

4️⃣ Protocol Statistics
- Generated Protocol Hierarchy Statistics in Wireshark to view packet distribution by protocol.
- Summary from screenshot (Screenshot_2025-08-11_03_30_53.png):

| Protocol | Packets | Percent of Total | Purpose |
|----------|---------|-----------------|---------|
| Ethernet | 3790    | 100%            | Data link layer |
| IPv4     | 3790    | 100%            | Network layer |
| TCP      | 2973    | 78.4%           | Reliable communication |
| TLS      | 235     | 6.2%            | Secure web traffic |
| HTTP     | 44      | 1.2%            | Web communication |
| OCSP     | 42      | 1.1%            | Certificate status verification |
| ICMP     | 19      | 0.5%            | Network diagnostics |
| ARP      | 17      | 0.4%            | LAN address resolution |

📂 Repository Structure

Task-5-Wireshark
 ├── README.md
 
 ├── task5.pcapng    # Packet capture file
 
 ├── screenshots

 │    ├── Screenshot_2025-08-11_03_22_19.png
 
 │    ├── Screenshot_2025-08-11_03_24_01.png
 
 │    ├── Screenshot_2025-08-11_03_24_50.png
 
 │    ├── Screenshot_2025-08-11_03_25_08.png
 
 │    ├── Screenshot_2025-08-11_03_30_53.png

🎯 Outcome
- Successfully captured live traffic on eth0 interface.
- Identified multiple protocols including TCP, ICMP, HTTP, TLS, OCSP, and ARP.
- Practiced filtering in Wireshark to isolate traffic by protocol.
- Learned to use Protocol Hierarchy Statistics to summarize packet distribution.
