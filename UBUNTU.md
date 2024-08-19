# Ubuntu Server LTS Installation and Configuration

This document outlines the steps to install and configure Ubuntu Server LTS on a Raspberry Pi 4 and set it up to work with your Matrix homeserver.

## Initial Setup

### Flash Ubuntu Server to SD Card

- **Download Ubuntu Server LTS:**
  Go to the [Ubuntu downloads page](https://ubuntu.com/download/raspberry-pi) and download the latest Ubuntu Server LTS image for Raspberry Pi.

- **Flash the Image:**
  Use tools like [Raspberry Pi Imager](https://www.raspberrypi.org/software/) or [Balena Etcher](https://www.balena.io/etcher/) to flash the downloaded image to the SanDisk Ultra MicroSDXC 64GB card.

- **Prepare the SD Card:**
  Insert the flashed SD card into the Raspberry Pi and connect the NVMe SSD using the Argon ONE M.2 NVMe Aluminum Case.

### Initial Boot and Configuration

- **Boot the Raspberry Pi:**
  Power on the Raspberry Pi with the SD card inserted. Connect it to your network via Ethernet or Wi-Fi.

- **Access the System:**
  Log in using SSH or directly on the Raspberry Pi:
    - Username: username
    - Password: password
  Change the password on first login.

- **Update the System:**
  Run the following commands to update package lists and upgrade all packages:

  ```sh
  sudo apt update
  sudo apt upgrade
