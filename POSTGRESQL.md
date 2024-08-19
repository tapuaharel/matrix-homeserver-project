# PostgreSQL Installation and Configuration

PostgreSQL is the database backend used for storing Matrix data.

## Installation

- **Install PostgreSQL:**
    ```sh
    sudo apt update
    sudo apt install postgresql postgresql-contrib
    ```

## Configuration

- **Set up PostgreSQL database and user:**
  - Switch to the PostgreSQL user:
    ```sh
    sudo -i -u postgres
    ```
  - Create the database and user:
    ```sh
    createdb matrixdb
    createuser --interactive
    ```
  - Grant privileges:
    ```sh
    psql
    GRANT ALL PRIVILEGES ON DATABASE matrixdb TO yourusername;
    \q
    ```

- **Configure PostgreSQL to allow connections:**
  Edit the `/etc/postgresql/12/main/pg_hba.conf` file to include the following lines (adjust version number as necessary):
    ```text
    # Allow local connections
    local   all             all                                     trust
    ```

- **Restart PostgreSQL to apply changes:**
    ```sh
    sudo systemctl restart postgresql
    ```
