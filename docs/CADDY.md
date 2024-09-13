# Caddy

Caddy is used to manage Reverse Proxy, TLS and HTTPS.

## Installation

- Downaload Caddy from the GitHub repository.

    ```sh
     wget -O caddy.deb https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_arm64.deb
    ```

- Install the .deb package.

  ```sh
   sudo dpkg -i caddy.deb
  ```

## Configuration

- Edit the Caddy configuration file to reverse proxy incoming traffic to Conduwuit
  
  ```sh
   sudo vim /etc/caddy/Caddyfile
  ```

  ```
  /etc/caddy/Caddyfile

  your.server.name, your.server.name:8448 {
      reverse_proxy 127.0.0.1:6167
  }
  ```

  ```sh
  sudo systemctl enable --now caddy
  sudo systemctl restart conduwuit
  ```
