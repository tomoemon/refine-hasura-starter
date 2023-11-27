This repository provides a docker-compose environment template for creating applications using hasura + refine and also resolves the following pitfalls in using the hasura docker image.

- hasura console
  - hasura console and hasura cli are provided by default
- hasura postgresql client version mismatch
  - The hasura docker image uses postgresql client version 15.4 as of November 2023, but this repository uses postgresql database version 16.1. If hasura migrate command is used in this situation, an error will occur due to version mismatch
- health check
  - Appropriate dependencies and health checks are set up between services

# Setup

```
docker-compose up -d
```

- hasura ui
  - http://localhost:8080/console
- hasura console
  - http://localhost:9695/

# Develop a refine app

See [refine-app/README.md](/refine-app/README.md)

# Hasura Console

The operations performed on the hasura console are saved in the following directory: `./hasura-console/data/`

# Hasura CLI

`hasura` command can be executed inside the `hasura-console` container.

```
docker-compose exec hasura-console bash
```
