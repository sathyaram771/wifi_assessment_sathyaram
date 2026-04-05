# Wi-Fi Training Program  
## Assignment Answers – Module 3  

---

### 1. Different 802.11 PHY layer standards and comparison

| Standard   | Band            | Max Speed        | Modulation       | Key Features |
|------------|-----------------|------------------|------------------|--------------|
| 802.11a    | 5 GHz           | 54 Mbps          | OFDM             | Less interference |
| 802.11b    | 2.4 GHz         | 11 Mbps          | DSSS             | Longer range |
| 802.11g    | 2.4 GHz         | 54 Mbps          | OFDM             | Backward compatible |
| 802.11n    | 2.4/5 GHz       | 600 Mbps         | OFDM             | MIMO support |
| 802.11ac   | 5 GHz           | ~3.5 Gbps        | OFDM             | MU-MIMO, 80/160 MHz channels |
| 802.11ax   | 2.4/5/6 GHz     | ~9.6 Gbps        | OFDMA, 1024-QAM  | High efficiency, dense environments |
| 802.11be   | 2.4/5/6 GHz     | ~46 Gbps         | 4096-QAM         | Multi-Link Operation (MLO), ultra-low latency, wider channels (320 MHz) |

---

### 2. DSSS and FHSS

- **DSSS (Direct Sequence Spread Spectrum):**
  - Spreads signal over a wide frequency band using a spreading code
  - More resistant to noise and interference
  - Used in 802.11b

- **FHSS (Frequency Hopping Spread Spectrum):**
  - Rapidly switches frequencies in a pattern
  - Avoids interference by hopping channels
  - Less commonly used in modern Wi-Fi

---

### 3. Modulation schemes in PHY layer

Common modulation techniques:
- BPSK (low data rate, robust)
- QPSK
- QAM (16-QAM, 64-QAM, 256-QAM, 1024-QAM)

**Comparison:**
- Higher-order modulation → higher speed but less robust
- Lower-order modulation → slower but more reliable

Example:
- 802.11n → up to 64-QAM  
- 802.11ac → up to 256-QAM  
- 802.11ax → up to 1024-QAM  

---

### 4. Significance of OFDM in WLAN

- Splits a channel into multiple subcarriers
- Transmits data in parallel streams

**Advantages:**
- High spectral efficiency
- Reduces interference and fading
- Supports high data rates

---

### 5. Frequency bands in Wi-Fi

- **2.4 GHz:**
  - Channels: 1–14 (only 1,6,11 non-overlapping)
  - Longer range, more interference

- **5 GHz:**
  - More channels, less interference
  - Higher speeds

- **6 GHz (Wi-Fi 6E):**
  - Even more bandwidth
  - Less congestion

---

### 6. Guard Intervals in WLAN

- Guard Interval (GI) prevents symbol overlap (Inter-Symbol Interference)

Types:
- Long GI: 800 ns
- Short GI: 400 ns

**Short GI Benefits:**
- Higher data rate (~10% improvement)
- Slightly more prone to errors in noisy environments

---

### 7. Structure of 802.11 PHY frame

Components:
1. **Preamble** → Synchronization
2. **Header (PLCP Header)** → Rate, length info
3. **Payload (PSDU)** → Actual data

---

### 8. OFDM vs OFDMA

| Feature     | OFDM                          | OFDMA                          |
|-------------|--------------------------------|--------------------------------|
| Usage       | Single user per transmission   | Multiple users simultaneously  |
| Efficiency  | Lower in dense networks        | High efficiency                |
| Used in     | 802.11a/n/ac                   | 802.11ax                       |

---

### 9. MIMO vs MU-MIMO

- **MIMO (Multiple Input Multiple Output):**
  - Multiple antennas for one device
  - Improves speed and reliability

- **MU-MIMO (Multi-User MIMO):**
  - Serves multiple devices simultaneously
  - Improves overall network capacity

---

### 10. PPDU, PLCP, PMD

- **PPDU (PLCP Protocol Data Unit):**
  - Entire transmitted frame at PHY layer

- **PLCP (Physical Layer Convergence Protocol):**
  - Prepares data for transmission
  - Adds header and preamble

- **PMD (Physical Medium Dependent):**
  - Handles actual transmission over medium (radio signals)

---

### 11. Types of PPDU

- **Legacy PPDU** → Used in older standards (a/b/g)
- **HT PPDU** → 802.11n
- **VHT PPDU** → 802.11ac
- **HE PPDU** → 802.11ax

**Structure generally includes:**
- Preamble
- Header
- Data field

Newer PPDUs support:
- Wider channels
- Higher modulation
- Multi-user support

---

### 12. How data rate is calculated

Data rate depends on:

- Channel bandwidth (20/40/80/160 MHz)
- Modulation scheme (QAM level)
- Coding rate
- Number of spatial streams (MIMO)
- Guard Interval

**Formula (simplified):**

```
Data Rate = (Subcarriers × Bits per Symbol × Coding Rate × Spatial Streams) / Symbol Duration
```

Higher values in these parameters → higher throughput.

---

