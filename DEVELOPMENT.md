# Development Guide

## Database
To use a local test database, you can use the docker-compose script:
```
$ cd ./docker-local
$ docker-compose up -d
```

It creates a MySQL 5.7x container with a volume pointing to `./var/mysql` to
store changes persistently.

### Shutting down the database
To stop the running container, you can call:
```
$ cd ./docker-local
$ docker-compose down
```

### Fresh database
If you need to purge the database content and want to start with a fresh instance,
stop the docker container, remove the volume and restart the container:
```
$ cd ./docker-local
$ docker-compose down
$ rm -rf ../var/mysql
$ docker-compose up -d
```
