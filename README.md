# Task 5: Capture and Analyze Network Traffic Using Wireshark

## 🎯 Objective
Capture live network packets and identify basic protocols and traffic types.

## 🛠 Tools Used
- **Wireshark** (latest version)

---

## 🔎 Steps Performed

1. **Installed Wireshark**
   - Downloaded from [https://www.wireshark.org](https://www.wireshark.org).
   - Installed on Windows/Linux.

2. **Started Packet Capture**
   - Opened Wireshark and selected the active network interface (Wi-Fi/Ethernet).
   - Clicked **Start Capturing Packets**.

3. **Generated Traffic**
   - Opened a web browser and visited `example.com`.
   - Also tested by running:
     ```bash
     ping google.com
     ```

4. **Stopped Capture**
   - After ~1 minute, clicked the red **Stop button** in Wireshark.

5. **Applied Filters**
   - Example filters used:
     - `http` → Show HTTP traffic
     - `dns` → Show DNS queries/responses
     - `tcp` → Show TCP packets
     - `icmp` → Show ping packets

6. **Identified Protocols**
   At least 3 protocols observed in the capture:
   - **DNS** – Used for domain name resolution (queries to `8.8.8.8`).
   - **TCP** – Transport protocol for HTTP and HTTPS traffic.
   - **HTTP** – Web traffic when browsing websites.
   - **ICMP** – Ping request/reply packets.

7. **Exported Capture**
   - Saved capture as `task5_capture.pcap`.

---

## 📑 Findings & Analysis

- **DNS** packets showed queries to resolve domains like `example.com`.
- **TCP** packets established connections with three-way handshake.
- **HTTP GET requests** showed webpage fetch from a server.
- **ICMP Echo requests/replies** confirmed connectivity testing.

This shows how multiple protocols work together in networking.

---

## 📂 Repository Deliverables

- `task5_capture.pcap` → Exported packet capture file (placeholder included, replace with your generated one).
- `README.md` (this file) → Explanation of steps, findings, and protocols identified.

---

## ❓ Interview Questions & Answers

**1. What is Wireshark used for?**
Wireshark is a network protocol analyzer used to capture and inspect packets in real time for troubleshooting and analysis.

**2. What is a packet?**
A packet is the smallest unit of data transmitted over a network, containing headers (source, destination, protocol info) and payload (data).

**3. How to filter packets in Wireshark?**
Using display filters like `http`, `dns`, `tcp.port==80`, or `ip.addr==8.8.8.8`.

**4. What is the difference between TCP and UDP?**
- TCP: Connection-oriented, reliable, error-checking, slower.
- UDP: Connectionless, faster, no guaranteed delivery.

**5. What is a DNS query packet?**
It is a request sent from a client to a DNS server to resolve a domain name into an IP address.

**6. How can packet capture help in troubleshooting?**
It helps identify issues like latency, dropped packets, misconfigured devices, and malicious activity.

**7. What is a protocol?**
A set of rules that define how data is transmitted between devices on a network.

**8. Can Wireshark decrypt encrypted traffic?**
- Yes, if provided with the correct keys (e.g., SSL/TLS session keys).
- Otherwise, encrypted traffic (like HTTPS) cannot be fully read.

---

## ✅ Outcome
- Hands-on skills in packet capture and filtering.
- Identified multiple protocols (DNS, TCP, HTTP, ICMP).
- Gained awareness of how network traffic flows in real time.
