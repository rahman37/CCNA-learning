# OSI Model – Notes

The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven distinct layers.

---

## 📶 The 7 Layers (Top to Bottom)

| Layer | Name              | Function                                 | Examples                          |
|-------|-------------------|------------------------------------------|------------------------------------|
| 7     | Application        | Interfaces directly with user apps       | HTTP, FTP, SMTP                    |
| 6     | Presentation       | Translates, encrypts, compresses data    | SSL/TLS, JPEG, MP3                 |
| 5     | Session            | Manages sessions and connections         | NetBIOS, RPC                       |
| 4     | Transport          | Ensures delivery, error recovery         | TCP, UDP                           |
| 3     | Network            | Routing, logical addressing (IP)         | IP, ICMP, OSPF                     |
| 2     | Data Link          | Frame transmission, MAC addressing       | Ethernet, PPP, VLAN                |
| 1     | Physical           | Transmits raw bits over the medium       | Cables, Hubs, Electrical Signals   |

---

## 🔄 Mnemonics

**Top-down (Layer 7 to 1):**  
> **A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing

**Bottom-up (Layer 1 to 7):**  
> **P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way

---

## 🎯 Important Notes

- **Switches** operate at Layer 2 (MAC)  
- **Routers** operate at Layer 3 (IP)  
- **TCP** is reliable (Layer 4), **UDP** is not  
- **Ping** uses ICMP (Layer 3)  
- Layer 7 protocols interact directly with the user

---

## 🧠 Quick Q&A

- Q: At what layer does encryption occur?  
  A: Layer 6 – Presentation

- Q: What layer handles IP addressing and routing?  
  A: Layer 3 – Network

- Q: Which layer segments and reassembles data?  
  A: Layer 4 – Transport
