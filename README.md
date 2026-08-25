# AtlasTech Enterprise Network

## About the project

I built this network in Cisco Packet Tracer as a practical exercise in designing and configuring a small enterprise network.

The main goal was to separate the company's departments using VLANs while still allowing them to communicate through a central router. I also configured DHCP so that client devices can automatically receive their network settings.

## Network structure

The network is divided into four VLANs:

| VLAN | Department | Network |
|------|------------|---------|
| 10 | Administration | 192.168.10.0/24 |
| 20 | Engineering | 192.168.20.0/24 |
| 30 | Sales | 192.168.30.0/24 |
| 40 | Servers | 192.168.40.0/24 |

The router acts as the gateway for each VLAN using router-on-a-stick.

## Devices

- 1 Cisco 2911 router
- 1 Cisco 3560 multilayer switch
- 3 Cisco 2960 access switches
- 6 PCs
- 1 server

## Technologies used

- VLANs
- 802.1Q trunking
- Inter-VLAN routing
- DHCP
- Static IP addressing
- Basic network troubleshooting
- Cisco Packet Tracer

## Addressing

The router provides the following gateways:

- VLAN 10 → 192.168.10.1
- VLAN 20 → 192.168.20.1
- VLAN 30 → 192.168.30.1
- VLAN 40 → 192.168.40.1

The server uses:

- IP → 192.168.40.10
- Gateway → 192.168.40.1

Client PCs receive their addresses through DHCP.

## Testing

I tested connectivity between the different VLANs using ICMP.

For example:

```text
PC1 → 192.168.20.1
PC1 → 192.168.30.1
PC1 → 192.168.40.10