# Conduwuit

Conduwuit is a lightweight Matrix server implementation.

## Installation

- Download Conduwuit from the GitHub repository.

    ```sh
     wget -O conduwuit.deb https://github.com/girlbossceo/conduwuit/releases/download/v0.4.6/aarch64-unknown-linux-musl.deb
    ```

- Install the .deb package (make sure to read the output that generated during installation).

   ```sh
    sudo dpkg -i conduwuit.deb
   ```

## Configuration

- Create and configure the conduwuit configuration file (only included the lines that I have modified)

    ```sh
     sudo vim /etc/conduwuit/conduwuit.toml
    ```

    ```
    /etc/conduwuit/conduwuit.toml

    server_name = "<domain_name>"
    allow_registration = true
    registration_token = "<shared_secret_token>"
    ```
