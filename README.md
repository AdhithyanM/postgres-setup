# Postgres Setup

This repository contains a Docker Compose setup for running PostgreSQL and pgAdmin in Docker containers. Follow the steps below to set up and run the services.

## Step-by-Step Guide

### 1. Clone the Repository

```bash
git clone https://github.com/AdhithyanM/postgres-setup.git
```

### 2. Start the Services

Open a terminal and navigate to the directory containing the `docker-compose.yml` file. Run the following command to start the services:

```bash
cd <your-repo-directory>
docker-compose -f docker-compose.yml up -d
```

### 3. Access pgAdmin

Open a web browser and go to [http://localhost:5050](http://localhost:5050).

Log in using the credentials specified in the environment variables:

- **Email**: `admin@admin.com`
- **Password**: `root`

### 4. Add PostgreSQL Server in pgAdmin

After logging in to pgAdmin, add a new server with the following details:

- **Name**: Any name you prefer.
- **Host**: `postgres` (the container name of the PostgreSQL service).
- **Port**: `5432`.
- **Username**: `root` (as specified in the `POSTGRES_USER` environment variable).
- **Password**: `root` (as specified in the `POSTGRES_PASSWORD` environment variable).

### 5. Stopping the Services

To stop the services, execute the following command from the directory containing the `docker-compose.yml`:

```bash
docker-compose down
```

## Summary

This Docker Compose setup simplifies the process of running PostgreSQL and pgAdmin as containers, allowing easy configuration and management of your PostgreSQL databases. By following this guide, you can quickly start using PostgreSQL with pgAdmin for database administration tasks.

For more information and advanced configurations, please refer to the [Docker documentation](https://docs.docker.com/compose/) and the [pgAdmin documentation](https://www.pgadmin.org/docs/).
