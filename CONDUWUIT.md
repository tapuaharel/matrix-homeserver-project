# Conduwuit

Conduwuit is a lightweight Matrix server implementation.

## Installation

- Download the aarch64 .deb package file from the repository's page.

    ```sh
    $ wget -O conduwuit.deb https://github.com/girlbossceo/conduwuit/releases/download/v0.4.6/aarch64-unknown-linux-musl.deb
    ```

- Install the .deb package (make sure to read the output that generated during installation).

   ```sh
   $ sudo dpkg -i conduwuit.deb
   ```

## Configuration

- Create and configure the conduwuit configuration file (only included the lines that I have modified)

    ```sh
    $ sudo vim /etc/conduwuit/conduwuit.toml
    ```

    ```toml

    {
      "server_name": "example.com",
      "database": {
        "type": "postgres",
        "host": "localhost",
        "port": 5432,
        "name": "matrixdb",
        "user": "yourusername",
        "password": "yourpassword"
        address = "192.168.1.1"
      }
    }
    ```

- Start the conduwuit systemd service and set it to start automatically upon system boot.

   ```sh
   $ sudo systemctl start conduwuit.service
   $ sudo systemctl enable conduwuit.service
