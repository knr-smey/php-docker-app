# PHP Docker App

This project provides a simple PHP application running in a Docker container using Docker Compose.

## Prerequisites
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Build and Start the Containers
Open a terminal in the project directory and run:

```
docker compose up -d --build
```

- `-d` runs the containers in detached mode.
- `--build` forces a rebuild of the images.

### 2. Access the Application
By default, the app will be available at:

```
http://localhost:80
```

### 3. Stopping the Containers
To stop the running containers:

```
docker compose down
```

### 4. Viewing Logs
To view logs from the running containers:

```
docker compose logs
```

### 5. Running Commands in the Container
To run a command (e.g., `php -v`) inside the PHP container:

```
docker compose exec php php -v
```

Replace `php -v` with any PHP command you want to run.

## Project Structure
- `Dockerfile` - Docker image definition for the PHP app
- `docker-compose.yml` - Docker Compose configuration
- `src/` - Application source code

## Troubleshooting
- Make sure Docker and Docker Compose are installed and running.
- If you change dependencies or the Dockerfile, rebuild with `docker compose up -d --build`.

---

## Useful Docker Commands

Here are some additional Docker and Docker Compose commands you may find helpful:

### List Running Containers
```
docker ps
```

### List All Containers (including stopped)
```
docker ps -a
```

### Execute a Shell in the PHP Container
```
docker compose exec php sh
```
or for bash (if available):
```
docker compose exec php bash
```

### Stop All Running Containers
```
docker stop $(docker ps -q)
```

### Remove All Stopped Containers
```
docker container prune
```

### Remove All Unused Images
```
docker image prune -a
```

### Remove All Unused Volumes
```
docker volume prune
```

### Check Container Status with Compose
```
docker compose ps
```


Feel free to modify this README for your specific project needs.
