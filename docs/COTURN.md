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
    sudo vim /etc/turnserver.conf
    ```

    ```
    /etc/turnserver.conf

    verbose
    syslog
    listening-port=3478
    tls-listening-port=5349
    use-auth-secret
    static-auth-secret=<turn_secret_key>
    realm=turn.<domain_name>
    cert=</path/to/fullchain.pem>
    pkey=</path/to/privkey.pem>
    no-tcp-relay
    denied-peer-ip=10.0.0.0-10.255.255.255
    denied-peer-ip=192.168.0.0-192.168.255.255
    denied-peer-ip=172.16.0.0-172.31.255.255
    no-multicast-peers
    denied-peer-ip=0.0.0.0-0.255.255.255
    denied-peer-ip=100.64.0.0-100.127.255.255
    denied-peer-ip=127.0.0.0-127.255.255.255
    denied-peer-ip=169.254.0.0-169.254.255.255
    denied-peer-ip=192.0.0.0-192.0.0.255
    denied-peer-ip=192.0.2.0-192.0.2.255
    denied-peer-ip=192.88.99.0-192.88.99.255
    denied-peer-ip=198.18.0.0-198.19.255.255
    denied-peer-ip=198.51.100.0-198.51.100.255
    denied-peer-ip=203.0.113.0-203.0.113.255
    denied-peer-ip=240.0.0.0-255.255.255.255
    allowed-peer-ip=<server.internal.ip.address>
    user-quota=12
    total-quota=1200
    ```
    
- Enable and start the Coturn service.

    ```sh
    sudo systemctl enable --now coturn
    ```

- Restart the Conduwuit service.

   ```sh
   sudo systemctl restart conduwuit
   ```
