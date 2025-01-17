# Moodle Docker Setup

This repository contains a Docker setup for running Moodle using `docker-compose`.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/docker-moodle.git
    cd docker-moodle
    ```

2. Create a `.env` file in the root directory and configure the necessary environment variables. You can use the `.env.example` file as a template.

3. Start the Docker containers:
    ```sh
    docker-compose up -d
    ```

4. Access Moodle:
    Open your web browser and go to `http://localhost:PORT` (replace `PORT` with the port number specified in your `docker-compose.yml` file).

## Configuration

The `docker-compose.yml` file includes the following services:

- **moodle**: The Moodle application.
- **mariadb**: The MariaDB database server.

### Environment Variables

- `MOODLE_DB_HOST`: The database host (default: `mariadb`).
- `MOODLE_DB_NAME`: The database name (default: `moodle`).
- `MOODLE_DB_USER`: The database user (default: `moodleuser`).
- `MOODLE_DB_PASSWORD`: The database password (default: `moodlepassword`).

## Volumes

- `moodledata`: Stores Moodle data files.
- `dbdata`: Stores MariaDB data files.

## Stopping the Containers

To stop the Docker containers, run:
```sh
docker-compose down
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Troubleshooting

If you encounter any issues, please check the Docker logs:
```sh
docker-compose logs
```

For further assistance, refer to the [Moodle documentation](https://docs.moodle.org/).
