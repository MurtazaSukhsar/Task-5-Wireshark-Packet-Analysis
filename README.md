# 📡 Task 5: Capture and Analyze Network Traffic Using Wireshark  

## 🎯 Objective  
Capture live network packets using **Wireshark**, identify basic protocols, and analyze captured traffic.  

---

## 🖥️ Environment  
- **OS**: Kali Linux (VMware)  
- **Tool**: Wireshark 4.4.7  
- **Network**: Virtual Network (NAT)  

---

## 📌 Steps Performed  

### 1️⃣ Start Wireshark Capture  
- Opened Wireshark and selected the active interface **`eth0`**.  
- Started live packet capture.  
- *(Screenshot: `Screenshot_2025-08-11_03_22_19.png`)*  

---

### 2️⃣ Generate Network Traffic  
- Browsed websites and used the `ping` command to create traffic.  
- Observed TCP, TLS, HTTP, ICMP, and ARP packets.  
- *(Screenshots: `Screenshot_2025-08-11_03_23_55.png`, `Screenshot_2025-08-11_03_24_01.png`, `Screenshot_2025-08-11_03_24_50.png`)*  

---

### 3️⃣ Apply Protocol Filters  
- Applied filters like:  
  - `http` → to see HTTP requests/responses.  
  - `tcp` → for TCP packets.  
  - `icmp` → for ping packets.  
- Observed **OCSP** queries and plain HTTP requests.  
- *(Screenshot: `Screenshot_2025-08-11_03_25_08.png`)*  

---

### 4️⃣ View Protocol Statistics  
- Opened **Statistics → Protocol Hierarchy** in Wireshark.  
- Summary:  

| Protocol | Packets | Percent of Total | Purpose |
|----------|---------|-----------------|---------|
| TCP      | 2973    | 78.4%           | Reliable communication |
| TLS      | 235     | 6.2%            | Secure web traffic |
| HTTP     | 44      | 1.2%            | Web communication |
| OCSP     | 42      | 1.1%            | Certificate status checks |
| ICMP     | 19      | 0.5%            | Network diagnostics |
| ARP      | 17      | 0.4%            | LAN address resolution |  

- *(Screenshot: `Screenshot_2025-08-11_03_30_53.png`)*  

---

## ✅ Result  
Successfully captured live network packets, identified multiple protocols, and applied filters to isolate specific traffic. Protocol hierarchy analysis provided insight into the distribution of network activity.  

---

## 📁 Folder Structure  
```
Task-5-Wireshark/
├── README.md
├── capture.pcap
└── screenshots/
    ├── Screenshot_2025-08-11_03_22_19.png
    ├── Screenshot_2025-08-11_03_23_55.png
    ├── Screenshot_2025-08-11_03_24_01.png
    ├── Screenshot_2025-08-11_03_24_50.png
    ├── Screenshot_2025-08-11_03_25_08.png
    └── Screenshot_2025-08-11_03_30_53.png
```  
