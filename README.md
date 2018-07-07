## What this docker image is for?

This is a docker image to run [Matomo](https://matomo.org/).

## How to run with docker-compose

In the docker-compose file, the following environment variables has default values:
- `MYSQL_ROOT_PASSWORD`
- `MYSQL_DATABASE`
- `MYSQL_USER`
- `MYSQL_PASSWORD`

Run from the root folder:
```
docker-compose -f x86/docker-compose.yml --project-director ./project_dir up --remove-orphans
```

The default address is [http://localhost:8080](http://localhost:8080/)

At the step to setup the database, as server name, use `matomo_database` or whatever it is set in the `docker-compose.yml` as database service.

There is also a `phpmyadmin` service to check the database at [http://localhost:9090](http://localhost:9090/)

