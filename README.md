# 🌐 Enterprise NAT/PAT Internet Gateway Lab

A Cisco Packet Tracer enterprise networking project that demonstrates how **NAT, PAT (NAT Overload), Static NAT, routing, and Internet gateway connectivity** can be implemented in a small enterprise network.

This project simulates an organization where multiple internal devices use private IPv4 addresses and access an external network through a single public IP address using **PAT**, while an internal server is made externally reachable using **Static NAT**.

---

## 📌 Project Overview

In an enterprise network, internal devices commonly use private IPv4 addresses such as:

- `192.168.x.x`
- `10.x.x.x`
- `172.16.x.x`

These private addresses cannot normally be routed across the public Internet.

To solve this problem, **Network Address Translation (NAT)** translates private IP addresses into public IP addresses.

This project implements:

- 🔹 PAT / NAT Overload
- 🔹 Static NAT
- 🔹 Default Routing
- 🔹 Private-to-Public Address Translation
- 🔹 Internet Gateway Simulation
- 🔹 NAT Verification
- 🔹 Network Troubleshooting
- 🔹 WAN Failure Testing

---

# 🎯 Objectives

The main objectives of this project are:

1. Configure an enterprise LAN.
2. Configure an ISP connection.
3. Configure default routing.
4. Implement PAT for multiple internal clients.
5. Implement Static NAT for an internal server.
6. Verify NAT translations.
7. Test Internet connectivity.
8. Troubleshoot NAT and routing failures.
9. Understand private and public IPv4 addressing.
10. Simulate an enterprise Internet gateway.

---

# 🏗️ Network Topology

```text
                  🌐 ISP
              Router2 (ISP)
             G0/0: 203.0.113.1
                    |
                    |
             203.0.113.0/30
                    |
                    |
          Router1 (NAT Gateway)
          G0/1: 203.0.113.2
          G0/0: 192.168.10.1
                    |
                    |
                Switch1
             /     |     |     \
           PC1    PC2   PC3   Server1
          .10     .11   .12     .100

        LAN: 192.168.10.0/24
