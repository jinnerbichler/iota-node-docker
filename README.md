# Docker Setup

Simply run

```
 docker-compose run --rm start_iri && docker-compose up -d --build
```

in order to start the setup.

This command does the following:

1. Downloads an existing database (to achieve a fully synced state early). This might take a while.
2. Starts the IRI node
3. Starts a management dashboard ([ipm](https://github.com/akashgoswami/ipm)), which is accessible via [localhost:8080](localhost:8080)

The log output can be accessed via

```
docker-compose logs -f
```

**Dependencies**

* Docker (version 17.09.1-ce or higher)
* Docker Compose (version 3 or higher)

## Update Neigbours/Config

To update the list of neighbours simply add or remove the endpoint of the neighbor (e.g. tcp://host123:8080) to/from the config file (`./config/iota/ini`) and restart the containers via 

```docker-compose up --no-deps -d --force-recreate iri```

If you experience any problems please contact me on Slack (@jinnerbi).

DON'T forget to comment ```RESCAN_DB=true``` (change it to ```;RESCAN_DB=true```). Otherwise the startup will take ages.


**Have fun :)**