# School Network Design (Cisco Packet Tracer)

A simulated school network I designed and configured in Cisco Packet Tracer. It covers IP addressing, subnetting, routing between subnets, and core services (DNS, web and email).

## Topology

<img width="953" height="692" alt="topology png" src="https://github.com/user-attachments/assets/2a415a41-1092-48bc-9594-a90d82e4de45" />


The network has one router connecting four subnets, with 9 switches and a wireless access point. In total there are 26 end devices and servers: 15 PCs, 5 laptops, 2 printers, 1 VoIP phone and 3 servers.

## IP addressing

The network 192.16.66.0 is split into four subnets, each using the mask 255.255.255.192 (/26, 62 usable addresses). The router has one interface in each subnet, and its address is the default gateway for that subnet.

| Subnet | Address range | Gateway (router interface) | Devices |
|---|---|---|---|
| 1 | 192.16.66.0 - .63 | 192.16.66.62 | 4 PCs, 2 printers |
| 2 | 192.16.66.64 - .127 | 192.16.66.126 | 8 PCs, email, DNS and web servers |
| 3 | 192.16.66.128 - .191 | 192.16.66.190 | 5 laptops (wireless access point) |
| 4 | 192.16.66.192 - .255 | 192.16.66.254 | 3 PCs, 1 VoIP phone |

## Services configured

- **DNS server (192.16.66.75):** A records for ntic.ac.uk and ntic.com, so devices can use names instead of IP addresses.
- **Web server (192.16.66.74):** HTTP enabled, hosting a simple school homepage.
- **Email server (192.16.66.73):** SMTP and POP3 enabled for the domain ntic.ac.uk, with 9 student mailboxes.

## What I learned

- How IPv4 addresses and subnet masks divide a network into separate segments
- How a default gateway lets devices in one subnet reach another through the router
- How DNS turns domain names into IP addresses
- How web and email servers fit into a network


## Files

- exercise-prep.pkt: the Packet Tracer project file (open with Cisco Packet Tracer)
