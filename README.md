# Moodle Docker Setup

This repository contains a Docker setup for running Moodle using `docker-compose`.

## Prerequisites

- Docker Desktop or Docker Engine for Windows or Linux
- Docker Compose

## Getting Started

PLEASE, REMEMBER WHEN YOU UPDATE THE DOCKER-COMPOSE.YML FILE, YOU NEED TO CREATE A NEW BRANCH AND RESTART THE CONTAINERS. LET'S KEEP MAIN BRANCH FOR THE ORIGINAL FILE INSTEAD SO DO NOT MERGE YOUR BRANCH TO MAIN. THIS ACTION WILL ALSO MAKE US BETTER UNDERSTAND THE CHANGES.

1. Clone or fork the repository:
    ```sh
    git clone https://github.com/yourusername/docker-moodle.git
    cd docker-moodle
    ```

2. Define your environment variables in a `docker-compose.yml' file. You need to change defaults to your own values and save the file. After you have change defaults away, you can start the containers.

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

### Environment Variables (Defaults)

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
