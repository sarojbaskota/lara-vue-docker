# Vue & Laravel - Docker Repository

This repository contains a Dockerized setup for a project combining Vue.js (Quasar Framework), Laravel, and Docker.

- PHP: 8.1
- Vue.js: 3.x
- Quasar: 2.12.0
- Laravel: 10.13.5
- phpMyAdmin: 5.2.1
- MariaDB: 11.0.2

## Project Structure

The repository is structured as follows:

├── api/<br>
│ ├── Dockerfile<br>
│ └── ...<br>
│ <br>
├── admin/<br>
│ ├── Dockerfile<br>
│ └── ...<br>
│ <br>
├── docker/<br>
│ ├── mariadb/<br>
│ └── nginx/<br>
│ <br>
└── docker-compose.yml<br>


- The `api/` directory contains the Laravel api code, including the `app/` directory for Laravel application files, and a `Dockerfile` for building the api Docker image.
- The `admin/` directory contains the Vue.js admin code, including the `public/` directory and a `Dockerfile` for building the admin Docker image.
- The `docker/` directory contains subdirectories for Docker-related files, such as `mariadb/` for MariaDB configuration and `nginx/` for Nginx configuration.
- The `docker-compose.yml` file is responsible for defining and orchestrating the Docker containers.

## Getting Started

To run the project locally using Docker, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/sarojbaskota/lara-vue-docker.git
   ```
2. Change into the project directory:

   ```bash
   cd lara-vue-docker
   ```
3. Build and start the Docker containers:

   ```bash
   docker-compose up -d
   ```
4. Access the admin application in your browser:

   - Open http://localhost:8080 in your browser to view the Vue.js admin.

5. Access the api application in your browser:

   - Open http://localhost:8000 in your browser to access the Laravel api.

## Running Laravel Commands

To run Laravel commands such as migrations or artisan commands, you can access the Laravel api container using the following command:

```bash
docker exec -it laravel-api bash
```

Once inside the container, you can run Laravel commands as you would on a regular Laravel installation. For example, to run migrations, use the following command:

```bash
php artisan migrate
```
Check running container

```bash
docker ps
```




Ref: https://github.com/rikimis/vue-laravel-docker