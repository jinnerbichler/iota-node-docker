# Docker Setup

Simply run

```
docker-compose up -d --build
```

in order to start the setup.

This command does the following:

1. Downloads an existing database (to achieve a fully synced state early)
2. Starts the IRI node
3. Creates a dashboard, which is accessible via `localhost:8080`

**Dependencies**

* Docker
* Docker Compose

## Add Neigbours

To add neighbours simply add the endpoint of the neighbor (e.g. tcp://host123:8080) to the config file (`./config/iota/ini`) and restart the containers via 

```docker-compose up -d --force-recreate```
