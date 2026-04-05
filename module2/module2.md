# Wi-Fi Training Program  
## Assignment Answers – Module 2  

---

### 1. Brief about Split MAC architecture and how it improves AP performance

- **Split MAC Architecture** divides MAC functions between:
  - **Access Point (AP)** → Handles time-critical tasks (beaconing, frame transmission, ACKs)
  - **Wireless LAN Controller (WLC)** → Handles non-real-time tasks (authentication, policy, management)

**Advantages:**
- Reduces processing load on AP
- Centralized management
- Better scalability
- Faster performance for real-time operations

---

### 2. CAPWAP and flow between AP and Controller

- **CAPWAP (Control And Provisioning of Wireless Access Points)** is a protocol used to manage APs via a WLC.

**Flow:**
1. AP boots up
2. Gets IP via DHCP
3. Discovers WLC (DNS/DHCP/manual)
4. Establishes CAPWAP tunnel
5. Downloads configuration
6. Starts serving clients

---

### 3. CAPWAP in OSI model and tunnels

- Works at:
  - **Layer 2 (Data Link)** and **Layer 3 (Network)**

**Two tunnels:**
1. **Control Tunnel**
   - Carries management traffic (configs, authentication)
2. **Data Tunnel**
   - Carries user data traffic

---

### 4. Difference between Lightweight APs and Cloud-based APs

| Feature              | Lightweight AP                  | Cloud-based AP              |
|---------------------|--------------------------------|-----------------------------|
| Controller          | Requires WLC                   | Managed via cloud           |
| Deployment          | On-premise                     | Internet-based              |
| Management          | Centralized (local WLC)        | Remote/cloud dashboard      |
| Scalability         | Limited by WLC                 | Highly scalable             |
| Cost                | Higher initial cost            | Subscription-based          |

---

### 5. How CAPWAP tunnel is maintained

- Uses **keepalive messages**
- Heartbeat between AP and WLC
- If no response → tunnel is dropped
- AP tries to rejoin controller

---

### 6. Difference between Sniffer mode and Monitor mode

| Feature        | Sniffer Mode                          | Monitor Mode                        |
|----------------|----------------------------------------|--------------------------------------|
| Purpose        | Packet capture                         | Network monitoring & security        |
| Traffic        | Captures specific traffic              | Scans all channels                   |
| Use Case       | Wireshark analysis                     | Rogue AP detection                   |

---

### 7. If WLC is deployed in WAN, which AP mode is best?

- **Best Mode: FlexConnect (H-REAP)**

**Reason:**
- Allows local switching of traffic
- Reduces WAN dependency
- Works even if WAN fails

---

### 8. Challenges with Autonomous APs (>50 APs)

- No centralized management
- Difficult configuration updates
- Poor scalability
- High maintenance effort
- No seamless roaming
- Inconsistent security policies

---

### 9. What happens if WLC goes down (Lightweight AP in Local mode)?

- Existing clients may continue temporarily
- New clients cannot authenticate
- No new policies/config updates
- Eventually connections drop
- Network becomes unstable

---

