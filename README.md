# Traccar with PostgreSQL using Docker Compose

This repository contains a Docker Compose configuration to set up Traccar, an open-source GPS tracking system, along with PostgreSQL as the database backend. The configuration allows you to quickly deploy Traccar and connect it to a persistent PostgreSQL database.

## Prerequisites

Make sure you have Docker and Docker Compose installed on your system. You can download and install Docker Desktop from the official website: https://www.docker.com/products/docker-desktop

## Getting Started

1. Clone this repository to your local machine:

```bash
$ git clone https://github.com/example/traccar-postgresql-docker.git
$ cd traccar-postgresql-docker
```


2. Customize the configuration:

- Open the `docker-compose.yml` file in a text editor.
- Optionally, modify the environment variables under the `database` service to set the PostgreSQL username, password, and database name according to your preferences.
- If needed, you can also adjust the ports mapped to the Traccar application under the `traccar` service.

3. Prepare the Traccar configuration:

- Replace the `./conf/traccar.xml` file with your own custom Traccar configuration file, if desired. Make sure it is in the proper format and contains the necessary settings for your setup.

4. Start the containers:

Run the following command to start the Traccar and PostgreSQL containers:

```bash
$ docker-compose up -d
```


This will download the required Docker images (if not already available) and start the containers in detached mode.

5. Access Traccar:

After the containers have started successfully, you can access Traccar through a web browser:

- Open your browser and visit `http://localhost:8082` to access the Traccar web interface.
- Log in with the default credentials (username: `admin`, password: `admin`). It is recommended to change these default credentials after initial login.

6. Usage and Customization:

- Traccar is now up and running! You can configure your devices, tracks, geofences, and other settings through the Traccar web interface.
- For advanced customization and specific use cases, refer to the Traccar documentation: https://www.traccar.org/documentation/

7. Stopping the containers:

To stop the containers, run the following command:

```bash
$ docker-compose down
```


This will stop and remove the containers, but the Traccar and PostgreSQL data will be persisted in the named volume `database`.

## Troubleshooting

- If you encounter any issues during the setup or while using Traccar, refer to the Troubleshooting section in the Traccar documentation: https://www.traccar.org/documentation/troubleshooting/

- For any specific issues related to this Docker Compose configuration, feel free to open an issue in this repository.

