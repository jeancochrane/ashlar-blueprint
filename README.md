# Ashlar Blueprint

A reference implementation for using Ashlar to build flexible-schema web applications

# Installation

## Requirements

- Docker >= 1.13.0 (must be compatible with [Compose file v3
  syntax](https://docs.docker.com/compose/compose-file/compose-versioning/#compatibility-matrix))
- docker-compose >= 1.10.0

## Set up

Build and start the app with docker-compose:

```
docker-compose run --service-ports ashlar-server
```

The app will be accessible on `localhost:8000`
