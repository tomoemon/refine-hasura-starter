This repository provides a docker-compose environment template for creating applications using hasura + refine.

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
