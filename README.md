# 🧪 Wireshark - Network Traffic Analysis Lab

This project documents my hands-on experience using **Wireshark** to capture and analyze network traffic within my SOC Lab environment. The objective is to continue enhancing and improving my skills as a SOC Analyst (blue team) by inspecting packet streams and identifying abnormal patterns generated from common cyber activities.

---

##   Skills Practiced

- Deep packet inspection and analysis
- Filtering network traffic using protocol and content rules
- Reconstructing TCP sessions and analyzing packet behavior
- Identifying ARP and DHCP broadcasts
- Manual inspection of credential exposure in HTTP traffic

---

##   Observations Made

- Applied filters like `http`, `userlog`, `password`, `admin`, `cmd`, and IP addresses (e.g. `192.168.56.109`) to narrow down network activity related to attacks.
- Detected plaintext credentials moving through HTTP sessions (e.g. `admin`, `password`, `base64`).
- Captured multiple TCP flags such as [SYN], [ACK], [RST], including retransmissions and failed handshakes.
- Observed live ARP requests and DHCP transactions, which helped visualize how devices communicated locally.
- Viewed hexadecimal and ASCII content of raw payloads to understand the actual data moving through packets.

---

## 🛡️ Security Recommendations

- Enforce HTTPS to prevent sensitive credentials from being exposed in plaintext.
- Monitor and restrict traffic on uncommon or high-numbered ports (e.g. `52199`).
- Set up alerts for high volumes of TCP retransmissions, which could signal scanning, DoS attempts, or network congestion.
- Regularly inspect ARP broadcasts to detect spoofing or unusual activity.
- Avoid using basic authentication or transmitting Base64-encoded credentials without encryption.

