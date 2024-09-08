# Coturn

Coturn provides TURN services to enhance real-time communication.

## Installation

- **Install Coturn:**
    ```sh
    sudo apt install coturn
    ```

## Configuration

- **Edit the Coturn configuration file `/etc/turnserver.conf`:**
    ```ini
    listening-port=3478
    tls-listening-port=5349
    fingerprint
    use-auth-secret
    static-auth-secret=YOUR_SECRET
    realm=example.com
    server-name=example.com
    ```
    - Replace `YOUR_SECRET` with a secure secret.
    - Replace `example.com` with your domain.

- **Enable and start Coturn:**
    ```sh
    sudo systemctl enable coturn
    sudo systemctl start coturn
    ```

## Troubleshooting

- **Check logs for errors:**
    ```sh
    sudo journalctl -u coturn
    ```
