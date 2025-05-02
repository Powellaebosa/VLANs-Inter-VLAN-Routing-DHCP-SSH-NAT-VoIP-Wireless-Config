# VLANs-Inter-VLAN-Routing-DHCP-SSH-NAT-VoIP-Wireless-Config
In this lab, I configured a full-stack enterprise-level network with secure VLAN segmentation, Layer 3 routing, DHCP services, NAT, VoIP phone integration, and wireless connectivity — all using Cisco best practices.
<b>Project Video Demo</b>https://github.com/Powellaebosa/VLANs-Inter-VLAN-Routing-DHCP-SSH-NAT-VoIP-Wireless-Config/tree/main

 Here’s what I did step-by-step in this lab:

🏛️ Core Switch Configuration (FSNA-SW1)
✔ Set hostname, clock, enable secret
✔ Configured management VLAN 100 with IP address
✔ Set up local username & encrypted passwords
✔ Applied console and VTY line access restrictions via standard ACL
✔ Enabled SSH v2, generated RSA keys, and disabled Telnet
✔ Set spanning-tree root bridge priority to 0 for VLANs 1–1024
✔ Created VLANs: MGMT (100), DATA (200), and VOICE (150)

🔁 Secondary Switch Configuration (FSNA-SW2)
✔ Configured matching VLANs
✔ Enabled SSH and disabled Telnet
✔ Set up all access ports for data and voice VLANs with QoS & portfast
✔ Enabled trunk links to FSNA-SW1
✔ Enabled MLS QoS for voice traffic optimization

🖧 Router Configuration (FSNA-RTR)
✔ Configured Router-on-a-Stick with sub-interfaces for each VLAN (100, 150, 200)
✔ Enabled IP NAT inside for all VLANs
✔ Set up DHCP pool for the DATA VLAN
✔ Configured default static route for internet access
✔ Connected router trunk port to core switch

👤 Host PC Configuration (User A & User B)
✔ Connected User A to FSNA-SW1 and User B to FSNA-SW2
✔ Verified DHCP client functionality and internet connectivity via ping tests
✔ Confirmed inter-VLAN routing by reaching default gateways and external IPs like 8.8.8.8

📞 VoIP Phones Setup
✔ Connected and registered Phone A and Phone B
✔ Configured Ephone DNs and assigned directory numbers (1001 and 1002)
✔ Verified phones were registered and able to place internal calls

📡 Wireless Access Point (WAP) & Tablet PC Setup
✔ Connected WAP to FSNA-SW1 and labeled the port
✔ Configured SSID FSNA-Lab with WPA2 PSK fsnalab1
✔ Connected Tablet PC wirelessly and ensured DHCP + internet access worked

🧠 Tools Used:

Cisco Packet Tracer

CLI (Command Line Interface)

Realistic network simulation techniques

🎓 Skills Demonstrated:

VLAN configuration and trunking

Layer 3 Inter-VLAN Routing

DHCP & NAT setup

SSH-based secure remote management

VoIP Phone provisioning

Wireless Access configuration

Access Control via ACL

Full-stack network engineering design & deployment
