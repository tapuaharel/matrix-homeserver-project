# Conduwuit Configuration

Conduwuit is a lightweight Matrix server implementation.

## Installation

- **Clone the Conduwuit repository:**
    ```sh
    git clone https://github.com/conduwuit/conduwuit
    cd conduwuit
    ```

## Configuration

- **Create and configure `conduwuit-config.json`:**
   Example configuration:
    ```json
    {
      "server_name": "example.com",
      "database": {
        "type": "postgres",
        "host": "localhost",
        "port": 5432,
        "name": "matrixdb",
        "user": "redacted",
        "password": "redacted"
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
