# Caddy

Caddy is used as a reverse proxy to manage DNS, TLS, HTTPS and forward traffic to the Matrix server.

## Installation

- Downaload Caddy from the GitHub repository.

    ```sh
    $ wget -O caddy.deb https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_arm64.deb
    ```

- Install the .deb Caddy package.

  ```sh
  $ dpkg -i caddy.deb
  ```

## Configuration

- **Create a `Caddyfile` in `/etc/caddy/` with the following content:**
    ```text
    example.com {
        reverse_proxy / http://localhost:8008
        log /var/log/caddy/access.log
        file_server
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
