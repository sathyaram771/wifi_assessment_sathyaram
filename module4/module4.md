# Wi-Fi Training Program  
## Assignment Answers – MAC Layer Topics  

---

### 1. Significance of MAC Layer and Its Position in the OSI Model

The **MAC (Media Access Control) layer** is a sublayer of the **Data Link Layer (Layer 2)** in the OSI model.

### Position in OSI Model:
- Layer 2 (Data Link Layer) is divided into:
  - **LLC (Logical Link Control)**
  - **MAC (Media Access Control)**

### Significance of the MAC Layer:
- **Medium Access Control:**  
  Determines how devices share and access the wireless medium (e.g., CSMA/CA in Wi-Fi).
  
- **Frame Formatting:**  
  Encapsulates data into frames and defines the structure for transmission.

- **Addressing:**  
  Uses **MAC addresses** (unique hardware identifiers) to ensure correct delivery within a local network.

- **Error Detection:**  
  Includes mechanisms like **Frame Check Sequence (FCS)** to detect transmission errors.

- **Collision Avoidance (in Wi-Fi):**  
  Uses techniques such as **backoff timers** and acknowledgments to minimize collisions in a shared medium.

- **Reliable Delivery:**  
  Supports retransmissions and acknowledgments to improve reliability.

---

### 2. Frame Format of the 802.11 MAC Header and Purpose of Each Field

An **802.11 MAC frame** consists of three main parts:
1. MAC Header
2. Frame Body (payload)
3. FCS (Frame Check Sequence)

### 802.11 MAC Header Fields:

| Field | Size | Purpose |
|------|------|--------|
| **Frame Control** | 2 bytes | Defines frame type (data, control, management), protocol version, and control flags |
| **Duration/ID** | 2 bytes | Specifies how long the channel will be reserved (used for NAV - Network Allocation Vector) |
| **Address 1 (Receiver)** | 6 bytes | Destination MAC address |
| **Address 2 (Transmitter)** | 6 bytes | Source MAC address |
| **Address 3** | 6 bytes | Used for filtering/routing (e.g., BSSID in infrastructure networks) |
| **Sequence Control** | 2 bytes | Contains sequence number and fragment number for frame ordering and reassembly |
| **Address 4** *(optional)* | 6 bytes | Used in special cases like wireless bridging (WDS) |
| **QoS Control** *(optional)* | 2 bytes | Supports Quality of Service (traffic prioritization) |
| **HT Control** *(optional)* | 4 bytes | Used for high-throughput (802.11n/ac/ax) features |

---

### Additional Components:

#### Frame Body:
- Contains the actual payload (data being transmitted)

#### FCS (Frame Check Sequence):
- **4 bytes**
- Used for **error detection** to ensure data integrity

---

### 3. MAC layer functionalities (Management, Control, Data)

#### **1. Management Functions**
- Beacon transmission (network advertisement)
- Scanning (active/passive)
- Authentication & deauthentication
- Association & reassociation
- Synchronization (TSF timing)
- Power-saving coordination
- Roaming support

#### **2. Control Functions**
- RTS (Request to Send)
- CTS (Clear to Send)
- ACK (Acknowledgment)
- Block ACK
- NAV (Network Allocation Vector) management
- Frame control for collision avoidance

#### **3. Data Functions**
- Data frame transmission
- Frame encapsulation
- Error detection (FCS)
- Fragmentation and reassembly
- QoS handling (WMM)

---

### 4. Scanning process and its types

Scanning is used by a client to discover available Wi-Fi networks.

#### **Types:**

**1. Passive Scanning**
- AP sends beacon frames
- Client listens for beacons
- Slower but less power consumption

**2. Active Scanning**
- Client sends probe request
- AP responds with probe response
- Faster network discovery

---

### 5. Client association process

Steps:
1. **Scanning** → Discover APs  
2. **Authentication** → Open/secure authentication  
3. **Association Request** → Client requests connection  
4. **Association Response** → AP accepts/rejects  
5. **IP Assignment** → DHCP assigns IP  
6. **Data Communication begins**

---

### 6. EAPOL 4-Way Handshake

Used in WPA2/WPA3 for secure key exchange.

#### **Steps:**

1. **Message 1 (AP → Client)**
   - Sends ANonce (random number)

2. **Message 2 (Client → AP)**
   - Sends SNonce
   - Generates PTK

3. **Message 3 (AP → Client)**
   - Sends GTK (Group Key)
   - Confirms PTK

4. **Message 4 (Client → AP)**
   - Acknowledgment

#### **Keys involved:**
- **PMK (Pairwise Master Key)** → Derived from password
- **PTK (Pairwise Transient Key)** → Session key
- **GTK (Group Temporal Key)** → Broadcast traffic

---

### 7. Power saving mechanisms in MAC layer

Purpose: Reduce battery consumption

#### **Mechanisms:**

- **Legacy Power Save**
  - Client sleeps, wakes for beacon
  - Uses TIM (Traffic Indication Map)

- **U-APSD (Unscheduled Automatic Power Save Delivery)**
  - Trigger-based communication
  - Used in VoIP

- **TWT (Target Wake Time – Wi-Fi 6)**
  - Scheduled wake/sleep cycles
  - Improves efficiency

---

### 8. Medium Access Control methodologies

#### **1. CSMA/CA (Collision Avoidance)**
- Listen before transmit
- Uses backoff timer

#### **2. RTS/CTS Mechanism**
- Avoids hidden node problem
- Reserves channel before transmission

#### **3. Contention-based access**
- Devices compete for medium

#### **4. Contention-free access (PCF - rare)**
- Controlled by AP
- Not commonly used

---

### 9. Block ACK mechanism

- Allows multiple frames to be acknowledged together

#### **Working:**
1. Sender transmits multiple frames
2. Receiver sends a single Block ACK
3. Bitmap indicates received frames

#### **Advantages:**
- Reduces overhead
- Improves throughput
- Efficient for high-speed networks

---

### 10. Frame aggregation techniques

#### **Types:**

**1. A-MSDU (Aggregated MAC Service Data Unit)**
- Combines multiple MSDUs into one frame
- Same destination

**2. A-MPDU (Aggregated MAC Protocol Data Unit)**
- Combines multiple MPDUs
- Each frame has its own header

#### **Benefits:**
- Reduces overhead
- Improves efficiency
- Increases throughput

---

