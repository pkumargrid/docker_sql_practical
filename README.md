Great! Based on your setup, let's update the README accordingly:

---

# Dockerized PostgreSQL Database with Custom SQL Scripts

This repository contains a single SQL script file (`Task.sql`) containing various SQL queries for a PostgreSQL database, along with an `.env` file to configure sensitive and configurable variables. Additionally, there's a Docker Compose manifest to set up a Docker container running PostgreSQL with the custom SQL script.

## SQL Script

The `sql-scripts` directory contains a single SQL script file named `Task.sql`. This file contains various SQL queries for interacting with the PostgreSQL database. You can customize or extend this script as needed for your application.

## Environment Variables

The `.env` file contains environment variables to configure the PostgreSQL database. These variables are used by the Docker Compose manifest to set up the database container. Here's an overview of the variables:

- **`POSTGRES_USER`**: Specifies the username for accessing the PostgreSQL database.
- **`POSTGRES_PASSWORD`**: Specifies the password for the PostgreSQL user.
- **`POSTGRES_DB`**: Specifies the name of the PostgreSQL database.
- (Add any additional environment variables as needed for your application)

Ensure to set appropriate values for these variables in the `.env` file before running Docker Compose.

## Docker Compose

The `docker-compose.yml` file defines a Docker Compose manifest to set up a PostgreSQL database container and execute the SQL script during container initialization. The manifest mounts the `sql-scripts` directory into the PostgreSQL container's `/docker-entrypoint-initdb.d` directory, ensuring that the SQL script is executed when the container starts.

Here's how to use Docker Compose to create a local database with the custom SQL script:

1. **Clone this Repository**: Clone this repository to your local machine using Git:

    ```bash
    git clone <repository_url>
    ```

2. **Navigate to Repository**: Navigate to the cloned repository directory:

    ```bash
    cd <repository_directory>
    ```

3. **Set Environment Variables**: Update the `.env` file with appropriate values for the PostgreSQL database configuration.

4. **Run Docker Compose**: Start the PostgreSQL container and execute the SQL script using Docker Compose:

    ```bash
    docker-compose up -d
    ```

    This command will build the Docker image and start the container in detached mode.

5. **Verification**: Verify that the container is running and the SQL script is executed by connecting to the PostgreSQL database using a database management tool such as DBeaver or `psql`.

6. **Stopping the Container**: When you're finished, stop the PostgreSQL container using Docker Compose:

    ```bash
    docker-compose down
    ```

    This will stop and remove the container.

## Additional Information

For more information about Docker and Docker Compose, refer to the official documentation:

- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)

---

Feel free to modify and enhance this README file as needed to fit your specific project requirements.

---

This README provides clear instructions on how to set up a PostgreSQL database with custom SQL scripts using Docker Compose and environment variables. It ensures that developers can easily understand and follow the steps to create a local database environment.
