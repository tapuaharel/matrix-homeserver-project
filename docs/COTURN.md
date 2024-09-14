# Coturn

Coturn provides TURN services to enhance real-time communication.

## Installation

- Install Coturn.

    ```sh
    sudo apt install coturn
    ```

## Configuration

- Create and edit the configuration file.

    ```sh
    sudo vim /etc/coturn.conf
    ```

    ```
    /etc/coturn.conf
    
    use-auth-secret
    static-auth-secret=<secret_key>
    realm=<domain_name>
    ```
    
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
