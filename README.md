# Matrix Homeserver

## Overview

Detailed documentation for the deployment of my Matrix homeserver.
Feel free to join my homeserver at **tapuah.net**.

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
- DNS A/AAAA records
- DHCP reservation/static IP Address
- DMZ
- Port Forwarding TCP <server.ip.address>:443 <server.ip.address>:8448
- Port Forwarding TCP/UDP <server.ip.address>:3478 <server.ip.address>:5349
- TLS Certificate (TURNS)

## Documentation

For detailed installation and configuration, refer to the following documents in the order shown:

- **[Ubuntu Server LTS](docs/UBUNTU.md)**
- **[Conduwuit](docs/CONDUWUIT.md)**
- **[Caddy](docs/CADDY.md)**
- **[Coturn](docs/COTURN.md)**
