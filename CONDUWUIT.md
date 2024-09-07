# Conduwuit

Conduwuit is a lightweight Matrix server implementation.

## Installation

- Download the aarch64 .deb package file from the repository's page.

    ```sh
    wget -O conduwuit.deb https://github.com/girlbossceo/conduwuit/releases/download/v0.4.6/aarch64-unknown-linux-musl.deb
    ```

- Install the .deb package (make sure to read the notes written on the screen as soon as the installation is finished).

   ```sh
   sudo dpkg -i aarch64-unknown-linux-musl.deb
   ```

## Configuration

- Create and configure the conduwuit configuration file.
   Example configuration:
    ```json
    {
      "server_name": "example.com",
      "database": {
        "type": "postgres",
        "host": "localhost",
        "port": 5432,
        "name": "matrixdb",
        "user": "yourusername",
        "password": "yourpassword"
      }
    }
    ```
    - Replace `example.com` with your domain.
    - Replace database credentials as appropriate.

- **Run Conduwuit:**
    ```sh
    deno run --allow-net --allow-read --allow-write --allow-env mod.ts
    ```

## Federation

- Ensure that federation is enabled and configured in `conduwuit-config.json`.
