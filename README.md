# Matrix Homeserver

## Overview

Detailed documentation for the deployment of my Matrix homeserver.
Feel free to join my homeserver at **tapuah.net**, registration token: apple

**Synatx Note:** Everything inside < > is an example and needs to be changed!!!

## Hardware

- Raspberry Pi 4 Model B 8GB RAM
- Official Raspberry Pi 4 Power Supply
- Argon ONE M.2 NVMe Aluminum Case
- Samsung 256GB M.2 2280 PCIe 3.0 x4 NVMe SSD
- SanDisk Ultra 64GB A1 C10 U1 MicroSDXC

## Software

- Ubuntu Server LTS
- Conduwuit
- Caddy
- Coturn

## Networking

- Domain Name
- DuckDNS subdomain
- DNS Alias record
- DHCP reservation/static IP Address
- DMZ
- Port Forwarding TCP <server.ip.address>:443, <server.ip.address>:8448
- Port Forwarding TCP/UDP <server.ip.address>:3478, <server.ip.address>:5349
- Port Forwarding UDP <server.ip.address>:49152-65535
- TLS Certificate (TURNS)

## Documentation

For detailed installation and configuration, refer to the following documents in the order shown:

- **Ubuntu Server LTS**
- **Conduwuit**
- **Caddy**
- **Coturn**
