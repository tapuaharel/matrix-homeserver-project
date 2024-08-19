# Caddy Configuration

Caddy is used as a reverse proxy to manage HTTPS and forward traffic to the Matrix server.

## Installation

- **Install Caddy:**
    ```sh
    curl -fsSL https://getcaddy.com | sudo bash -s personal
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
