# Docker Setup

Simply run

```
docker-compose up -d --build
```

in order to start the setup.

This command does the following:

1. Downloads an existing database (to achieve a fully synced state early)
2. Starts the IRI node
3. Starts a management dashboard ([ipm](https://github.com/akashgoswami/ipm)), which is accessible via localhost:8080

The log output can be accessed via

```
docker-compose logs -f
```

**Dependencies**

* Docker (version 17.09.1-ce or higher)
* Docker Compose (version 3 or higher)

## Update Neigbours/Config

To add neighbours simply add or remove the endpoint of the neighbor (e.g. tcp://host123:8080) to/from the config file (`./config/iota/ini`) and restart the containers via 

```docker-compose up -d --force-recreate```


**Have fun :)**