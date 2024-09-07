# Matrix Homeserver

## Overview

Detailed documentation for the deployment of my Matrix homeserver.
This homeserver is for personal use and experimentation.

## Hardware

- Raspberry Pi 4 Model B 8GB RAM
- Official Raspberry Pi 4 Power Supply
- Argon ONE M.2 NVMe Aluminum Case
- Samsung 256GB M.2 2280 PCIe 3.0 x4 NVMe SSD
- SanDisk Ultra 64GB A1 C10 U1 MicroSDXC card.

## Software

- Ubuntu Server LTS
- Conduwuit
- Caddy
- Coturn

## Networking

SOHO router

- Set up a DHCP Reservation or configure a static IP address manually for the server.
- Port forward port 22 to the server's IP address for a SSH connection over the internet.

## Documentation

For detailed installation and configuration, refer to the following documents in the order shown:

- **[Ubuntu Server LTS](UBUNTU.md)**
- **[Conduwuit](CONDUWUIT.md)**
- **[Caddy](CADDY.md)**
- **[Coturn](COTURN.md)**

## Join

Feel free to join my homeserver
