# WiFi Training Program  
## Module 6 – Assignment Answers  

---

### 1. What are the pillars of Wi-Fi security?

The main pillars of Wi-Fi security are based on core principles of information security:

- **Confidentiality**: Ensures that data transmitted over the network is protected from unauthorized access, typically using encryption.
- **Integrity**: Guarantees that the data is not altered or tampered with during transmission.
- **Availability**: Ensures that authorized users can access the network and its resources when needed.
- **Authentication**: Verifies the identity of users or devices trying to connect to the network.
- **Non-repudiation** (optional but important): Prevents users from denying their actions on the network.

---

### 2. Explain the difference between authentication and encryption in WiFi security.

- **Authentication** is the process of verifying the identity of a user or device before granting access to the network. Examples include passwords, certificates, or 802.1X login methods.

- **Encryption** is the process of converting data into a secure format so that only authorized parties can read it. It protects data confidentiality during transmission (e.g., AES encryption in WPA2/WPA3).

In short:  
- Authentication = *Who are you?*  
- Encryption = *Keep your data secret.*

---

### 3. Explain the differences between WEP, WPA, WPA2, and WPA3.

- **WEP (Wired Equivalent Privacy)**:  
  The earliest Wi-Fi security protocol. Uses RC4 encryption but is weak due to poor key management and vulnerabilities.

- **WPA (Wi-Fi Protected Access)**:  
  Introduced as an improvement over WEP. Uses TKIP (Temporal Key Integrity Protocol) to dynamically change keys, but still relies on RC4.

- **WPA2**:  
  A major improvement using AES (Advanced Encryption Standard) for strong encryption. It is widely used and more secure than WPA.

- **WPA3**:  
  The latest standard with enhanced security features such as SAE (Simultaneous Authentication of Equals), improved encryption, and protection against brute-force attacks.

---

### 4. Why is WEP considered insecure compared to WPA2 or WPA3?

WEP is insecure because:

- It uses weak RC4 encryption.
- It relies on static keys that are rarely changed.
- It has vulnerabilities in its initialization vector (IV), allowing attackers to recover keys quickly.
- It lacks proper integrity protection.

Modern tools can crack WEP in minutes, making it obsolete compared to WPA2/WPA3.

---

### 5. Why was WPA2 introduced?

WPA2 was introduced to address the weaknesses of WPA and WEP by:

- Replacing TKIP with **AES encryption**, which is much stronger.
- Providing better data integrity and confidentiality.
- Complying with the IEEE 802.11i standard.

It significantly improved overall wireless security and became the industry standard.

---

### 6. What is the role of the Pairwise Master Key (PMK) in the 4-way handshake?

The **Pairwise Master Key (PMK)** is a shared secret derived from:

- A pre-shared key (PSK), or  
- Authentication via an 802.1X server.

Its role in the 4-way handshake is:

- To generate temporary session keys (PTK – Pairwise Transient Key).
- To ensure both client and access point have the same secret without transmitting it directly.
- To securely derive encryption keys used for protecting data.

---

### 7. How does the 4-way handshake ensure mutual authentication between the client and the access point?

The 4-way handshake ensures mutual authentication by:

1. The access point sends a nonce (random number) to the client.
2. The client generates its own nonce and derives a PTK using both nonces and the PMK.
3. The client sends its nonce and a message integrity code (MIC) to the access point.
4. The access point verifies the MIC and responds with its own confirmation.

Since both sides must prove knowledge of the PMK (without sending it), they authenticate each other securely.

---

### 8. What will happen if we put a wrong passphrase during a 4-way handshake?

If the passphrase is incorrect:

- The client will derive a **wrong PMK**.
- This results in incorrect PTK generation.
- The Message Integrity Code (MIC) will not match.
- The access point will reject the authentication.

As a result, the connection will fail, and the client will not be able to join the network.

---

### 9. What problem does 802.1X solve in a network?

**802.1X** solves the problem of **unauthorized access** by providing:

- Centralized authentication using a RADIUS server.
- Individual user credentials instead of a shared password.
- Dynamic key generation for each session.

This prevents unauthorized users from easily accessing the network and improves accountability.

---

### 10. How does 802.1X enhance security over wireless networks?

802.1X enhances Wi-Fi security by:

- Enabling **strong authentication methods** (e.g., certificates, EAP protocols).
- Using a centralized authentication server (RADIUS).
- Generating **unique session keys** for each user.
- Supporting mutual authentication between client and server.
- Reducing risks associated with shared passwords.

Overall, it provides enterprise-level security compared to basic WPA2-PSK networks.

---

