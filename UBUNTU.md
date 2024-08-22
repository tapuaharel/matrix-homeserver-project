# Ubuntu Server LTS Installation and Configuration

Ubuntu Server LTS is the operating system running on the Raspberry Pi 4.

## Installation

- Flash the Raspberry Pi OS 64bit image onto the MicroSD card using Raspberry Pi Imager.
- Insert the flashed MicroSD card into the Raspberry Pi and connect the NVMe SSD using the Argon ONE M.2 NVMe Aluminum Case.
- Boot the Raspberry Pi from the MicroSD card.
- Download the Ubuntu Server LTS ARM64 ISO file and flash it to the NVMe drive using Raspberry Pi Imager.

## Configuration

- **Boot the Raspberry Pi:**
  Power on the Raspberry Pi with the SD card inserted. Connect it to your network via Ethernet or Wi-Fi.

- **Access the System:**
  Log in using SSH or directly on the Raspberry Pi:
    - Username: "yourusername"
    - Password: "yourpassword"
  Change the password on first login.

- **Update the System:**
  Run the following commands to update package lists and upgrade all packages:

  ```sh
  sudo apt update
  sudo apt full-upgrade
