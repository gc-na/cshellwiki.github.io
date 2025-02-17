# [English] Bash docker-compose Usage: Manage multi-container Docker applications

## Overview
The `docker-compose` command is a tool for defining and running multi-container Docker applications. It allows users to configure application services, networks, and volumes in a single YAML file, making it easier to manage complex setups.

## Usage
The basic syntax of the `docker-compose` command is as follows:

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: Starts the services defined in the `docker-compose.yml` file.
- `down`: Stops and removes the containers defined in the `docker-compose.yml` file.
- `build`: Builds or rebuilds the services defined in the `docker-compose.yml` file.
- `logs`: Displays the logs from the services.
- `exec`: Executes a command in a running container.

## Common Examples
Here are some practical examples of using the `docker-compose` command:

1. **Starting services**:
   ```bash
   docker-compose up
   ```

2. **Starting services in detached mode**:
   ```bash
   docker-compose up -d
   ```

3. **Stopping services**:
   ```bash
   docker-compose down
   ```

4. **Building services**:
   ```bash
   docker-compose build
   ```

5. **Viewing logs**:
   ```bash
   docker-compose logs
   ```

6. **Executing a command in a running container**:
   ```bash
   docker-compose exec web bash
   ```

## Tips
- Always ensure your `docker-compose.yml` file is correctly formatted to avoid errors.
- Use the `-d` option with `up` to run containers in the background, allowing you to continue using the terminal.
- Regularly check logs with `docker-compose logs` to monitor the behavior of your services.
- Utilize version control for your `docker-compose.yml` file to track changes and collaborate with others effectively.