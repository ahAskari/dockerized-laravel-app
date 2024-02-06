Certainly! Below is a sample README file for your Dockerized Laravel app with Nginx web server and MySQL database. Please customize it based on your specific configurations and requirements:

---

# Dockerized Laravel App with Nginx and MySQL

This repository contains a Dockerized Laravel application with Nginx as the web server and MySQL as the database. It allows you to easily set up and run your Laravel application in a containerized environment.

## Prerequisites

Make sure you have the following tools installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/ahAskari/dockerized-laravel-app
   cd dockerized-laravel-app
   ```

2. Copy the `mysql.env.example` file and rename it to `.env`. Update the necessary environment variables for MySQL configuration.

3. Build and start the Docker containers:

   ```bash
   docker compose up -d --build
   ```

   This command will download the required Docker images, build the necessary containers, and start the services in detached mode.

4. Run this command to installing laravel app
    ```bash
    docker compose run --rm composer create-project laravel/laravel .
    ```
5. Run migrations and seed the database:

   ```bash
   docker compose run artisan migrate
   ```

   This will set up the database tables and seed initial data.

6. Access your Laravel application in the browser:

   Open your web browser and navigate to [http://localhost:8000](http://localhost:8000).

## Stopping the Application

To stop the running Docker containers, use the following command:

```bash
docker compose down
```

## Configuration

- **Laravel Configuration**: You can modify the Laravel configuration in the `./src/.env` file.

- **Nginx Configuration**: Nginx configuration files are located in the `nginx` directory.

- **MySQL Configuration**: MySQL configuration is defined in the `docker compose.yml` file.

Feel free to customize the configuration files and make any necessary adjustments according to your specific requirements.