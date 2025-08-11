Task 5 – Wireshark Packet Analysis

Objective
---------
The goal of this task is to analyze network traffic using Wireshark on Kali Linux. This includes capturing packets, viewing protocol statistics, and identifying protocol distribution.

Tools Used
----------
- Kali Linux
- Wireshark

Steps Performed
---------------

1. Starting Wireshark
   - Open Wireshark in Kali Linux:
     wireshark &
   - Select the desired network interface (e.g., eth0 or wlan0) to capture packets.
   - Click "Start Capturing" (blue shark fin icon).

2. Capturing Packets
   - Allowed the capture to run for a few minutes to collect enough network traffic.
   - Ensured various types of network activity occurred (e.g., browsing, pings).

3. Viewing Protocol List
   - Once enough packets were captured, stopped the capture (red square icon).
   - Navigated to: Statistics → Protocol Hierarchy
   - This displayed the protocol breakdown by percentage, packet count, and bytes.

   From the capture:
   - Top Protocols Detected:
     * Ethernet
     * IPv4
     * UDP
     * TCP
     * TLS
     * HTTP
     * ARP
     * ICMP

4. Saving the Capture
   - Saved the capture file for documentation:
     File → Save As → capture_task5.pcapng

Observations
------------
- The majority of packets were UDP traffic (78.4%).
- TCP accounted for ~20.6% of packets, with notable HTTP and TLS activity.
- Minimal ARP and ICMP traffic was observed.

Conclusion
----------
Wireshark successfully captured and analyzed network packets in Kali Linux. The protocol hierarchy provided a clear view of the types of traffic present on the network and their distribution.
