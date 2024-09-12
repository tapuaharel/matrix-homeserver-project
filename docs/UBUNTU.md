# Ubuntu Server LTS

Ubuntu Server LTS is the operating system that will be running on the Raspberry Pi 4.

## Installation

- Flash the Raspberry Pi OS 64bit image onto the MicroSD card using Raspberry Pi Imager.
- Insert the flashed MicroSD card into the Raspberry Pi and connect the NVMe SSD using the Argon ONE M.2 NVMe Aluminum Case.
- Boot the Raspberry Pi from the MicroSD card.
- Update package lists and upgrade all packages.

  ```sh
   sudo apt update
   sudo apt full-upgrade
  ```
  
- Install Vim (not necessary but this is what I use for text editing)

  ```sh
   sudo apt install vim
  ```

- Update the bootloader to the latest release and reboot.

  ```sh
   sudo apt install rpi-eeprom
   sudo rpi-eeprom-update -d -a
   sudo reboot
  ```

- Update the EEPROM configurtaion (select "Update" in the menu).

  ```sh
   sudo raspi-config
  ```

- Change the boot order to boot from USB in order to boot from the NVMe drive (select "Advanced Options" and then "Boot Order").

  ```sh
   sudo raspi-config
  ```

- Flash the Ubuntu Server LTS image to the NVMe drive using the Raspberry PI Imager tool and reboot.

## Configuration

- Update the system and reboot.

  ```sh
   sudo apt install
   sudo apt full-upgrade
   sudo reboot
  ```

- Add a new user to the system

  ```sh
   adduser <user_name>
  ```

- Add the user to the sudoers file.

  ```sh
   sudo adduser <user_name> sudo
  ```

- Reboot the system and login as the 'user_name'

- Find the IP address of the machine.

  ```sh
   ip a
  ```

- Set up the SSH server (for this setup I showed the password authentication method to establish connection).

  ```sh
   sudo apt install openssh-server
   sudo vim /etc/ssh/sshd_config
  ```

  ```
  /etc/ssh/sshd_config

  Match User <user_name>
  PasswordAuthentication yes
  ```
  
  ```sh
   sudo systemctl restart ssh
  ```

- Set up the SSH client (commands executed on the client)

  ```sh
   sudo apt install openssh
  ```

- Establish a SSH connection (commands executed on the client)
  
  ```sh
   ssh <user_name>@<ip_address>
  ```
