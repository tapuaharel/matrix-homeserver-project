# Matrix Homeserver

## Overview

Detailed documentation for the deployment of my Matrix homeserver.
This homeserver is for personal use and experimentation.
Feel free to join my homeserver at **tapuah.net**.

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

- Own a domain name.
- Set up DNS A/AAAA records to map into your public IP address.
- Set up a DHCP Reservation or configure a static IP address manually for the server.
- Port forward port 22 to the server's IP address for a SSH connection over the internet.

## Documentation

For detailed installation and configuration, refer to the following documents in the order shown:

- **[Ubuntu Server LTS](docs/UBUNTU.md)**
- **[Conduwuit](docs/CONDUWUIT.md)**
- **[Caddy](docs/CADDY.md)**
- **[Coturn](docs/COTURN.md)**
