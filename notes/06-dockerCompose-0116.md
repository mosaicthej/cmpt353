# Docker Compose

## Docker Compose

Docker Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application's services. Then, with a single command, you create and start all the services from your configuration.

```bash
docker-compose up
```

## Docker Compose File

```yaml
version: '3.9'
services:
  python1:
    build: ./python1
    container_name: python1
    command: flask run --host=0.0.0.0
    ports:
      - "80:5000"
    volumes:
      - ./python1:/app
    environment:
      - FLASK_APP=app.py
      - FLASK_ENV=development
```

| Option | Description |
| --- | --- |
| `version` | version of the compose file |
| `services` | list of services |
| `build` | build the image |
| `container_name` | name the container |
| `command` | command to run |
| `ports` | port mapping |
| `volumes` | volume mapping |
| `environment` | environment variables |