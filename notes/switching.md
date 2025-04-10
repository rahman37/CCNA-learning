# Switching – Notes

Switching is a core function of network devices that operate at Layer 2 (Data Link layer) of the OSI model. It connects devices within the same local network and forwards frames based on **MAC addresses**.

---

## 🧱 What a Switch Does

- Learns MAC addresses of connected devices
- Builds a MAC address table (aka CAM table)
- Forwards frames only to the destination port (unicast)
- Floods unknown or broadcast frames out all ports (except incoming)
- Avoids collisions with full-duplex communication

---

## 📊 MAC Address Table

Command to view:
```bash
show mac address-table
Each entry maps:

MAC Address ↔ Port number

Helps determine where to send future frames

📚 Types of Switching
Type	Description
Store-and-Forward	Stores entire frame before forwarding; verifies CRC
Cut-Through	Starts forwarding as soon as destination MAC is read
Fragment-Free	Waits for 64 bytes (collision window) to avoid errors
📦 Frame Forwarding Behavior
Frame Type	Action on Switch
Unicast (known)	Sent directly to the correct port
Unicast (unknown)	Flooded to all ports except incoming
Broadcast	Flooded to all ports (e.g., ARP)
Multicast	Treated like broadcast (unless IGMP)
🛠️ Useful CLI Commands (Cisco)
bash
Copy
Edit
show mac address-table
show interfaces status
show running-config
🧠 Quick Reminders
Switches operate at Layer 2

Use MAC addresses to forward traffic

Can be configured with VLANs

Flood unknown MAC frames by default
