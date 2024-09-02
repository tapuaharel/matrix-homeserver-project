# Ubuntu Server LTS

Ubuntu Server LTS is the operating system running on the Raspberry Pi 4.

## Installation

- Flash the Raspberry Pi OS 64bit image onto the MicroSD card using Raspberry Pi Imager.
- Insert the flashed MicroSD card into the Raspberry Pi and connect the NVMe SSD using the Argon ONE M.2 NVMe Aluminum Case.
- Boot the Raspberry Pi from the MicroSD card.
- Update package lists and upgrade all packages.

  ```sh
  sudo apt update
  sudo apt full-upgrade
  ```
- Update the bootloader to the latest release and reboot.

'''sh
sudo apt install rpi-eeprom
sudo rpi-eeprom-update -d -a
sudo reboot
'''

-Update the EEPROM configurtaion (select "Update" in the menu).

'''sh
sudo raspi-config
'''

- Change the boot order to boot from USB in order to boot from the NVMe drive (select "Advanced Options" and then "Boot Order").

'''sh
sudo raspi-config
'''

- Flash the Ubuntu Server LTS image to the NVMe drive using the Raspberry PI Imager tool and reboot.

## Configuration

- Update the system and reboot.

'''sh
sudo apt install
sudo apt full-upgrade
sudo reboot
'''

- Install net-tools and use ifconfig to find out the IP address of the machine.
'''sh
sudo apt install net-tools
ifconfig
'''

- Set up the SSH server (Ubuntu machine).

'''sh
sudo apt install openssh-server
sudo systemctl status ssh
cd /etc/ssh
ls -la
sudo cp ./sshd_config ./sshd_config.original
'''
- Set up an SSH connection for remote administration (the commands are executed on the machine from which you want to remotely administer the Ubuntu Server).
'''sh
ssh ubuntu@your.ip.address.here
