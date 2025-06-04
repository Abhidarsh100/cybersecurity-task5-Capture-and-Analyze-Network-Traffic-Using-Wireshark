# 🛡️ Task 5: Network Traffic Capture and Protocol Analysis using Wireshark (Kali Linux in VirtualBox)

## 🎯 Objective

Capture and analyze live network traffic using **Wireshark** inside **Kali Linux running on Oracle VirtualBox**. Identify key network protocols such as DNS, HTTP, TCP, and ICMP to develop hands-on packet analysis skills relevant for cybersecurity.

---

## 🧰 Tools Used

| Tool             | Purpose                                      |
|------------------|----------------------------------------------|
| Kali Linux       | Penetration testing Linux distribution (VM) |
| VirtualBox       | Virtualization platform                       |
| Wireshark        | Network traffic capture and analysis         |
| curl / ping      | Generate network traffic via CLI              |
| Firefox Browser  | Generate HTTP/S and DNS traffic               |

---

## 🖥️ Environment Setup

- **Operating System**: Kali Linux (latest) inside Oracle VirtualBox
- **Wireshark**: Pre-installed on Kali
- **Active Network Interface**: `eth1` (VirtualBox virtual Ethernet adapter)
- **Network Mode**: Bridged Adapter (directly connects VM to host LAN)
- **Note**: No Wi-Fi interface is present inside the VM since VirtualBox provides virtual Ethernet interfaces.

---

## 🛠️ Steps Followed

### 1. Open Wireshark
- Start Capture on Interface eth1
- Selected interface: eth1
- Clicked "Start Capturing Packets"
- Generate Network Traffic
- Activity	Protocols Triggered
### 2. Opened firefox browser .  
- Visited http://testphp.vulnweb.com	
- Visited https://tryhackme.com	
### Open terminal. 
- Pinged 8.8.8.8	

### 🔍 Applied Wireshark Filters
| Filter                | Purpose                                   |
|-----------------------|-------------------------------------------|
| dns                   | Display DNS query and response packets    |
| http                  | Display HTTP traffic packets              |
| tcp                   | Show all TCP packets                      |
| icmp                  | Display ICMP ping requests and replies    |
| ip.addr == 8.8.8.8    | Filter traffic to/from Google DNS IP      |

📡 Protocols Identified and Explained
1. DNS (Domain Name System)
Resolves domain names to IP addresses.

Example captured packet: DNS query for tryhackme.com
![Alt text](image_path_or_URL)
2. HTTP (HyperText Transfer Protocol)
Unencrypted web requests/responses seen with vulnweb.com

3. HTTPS (TLS encrypted HTTP)
Seen when browsing tryhackme.com

Traffic encrypted, TCP handshake visible

4. TCP (Transmission Control Protocol)
Manages reliable connections with SYN, SYN-ACK, ACK handshake

5. ICMP (Internet Control Message Protocol)
Used for ping packets (request and reply)

📚 Learning Outcomes
Practical packet capturing and protocol identification

Usage of Wireshark filters to isolate traffic types

Understanding of TCP/IP protocols in real network environments

Working with Kali Linux in bridged network mode on VirtualBox
