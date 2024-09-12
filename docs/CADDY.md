# Caddy

Caddy is used as a reverse proxy to manage DNS, TLS, HTTPS and forward traffic to the Matrix server.

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

- Edit the Caddy configuration file to enable reverse proxy and disable all other services.
  
  ```sh
   sudo vim /etc/caddy/Caddyfile
  ```

  ```
  tapuah.net {
                   reverse_proxy localhost:
- Create the Caddy configuration file for Conduwuit.

  ```sh
  sudo vim /etc/caddy/conf.d/conduwuit_caddyfile
  ```

  ```
  your.server.name, your.server.name:8448 {
    # TCP reverse_proxy
    127.0.0.1:6167
    # UNIX socket
    #reverse_proxy unix//run/conduwuit/conduwuit.sock
  }
    ```

    - Replace `example.com` with your domain.
    - Replace `localhost:8008` with your Conduwuit server address.

- **Start and enable Caddy:**
    ```sh
    sudo systemctl enable caddy
    sudo systemctl start caddy
    ```

## Troubleshooting

- **Check logs for errors:**
    ```sh
    sudo journalctl -u caddy
    ```
