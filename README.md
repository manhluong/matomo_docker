## What this docker image is for?

This is a docker image to run [Matomo](https://matomo.org/).

## How to run with docker-compose

Download Matomo code and unzip into: `local_files/matomo/`.
That folder is shared between nginx service and php service.
Please use that folder as root folder and don't use the `piwik` folder that is inside the zip file.

Set the following environment variables:
- `MYSQL_ROOT_PASSWORD`
- `MYSQL_DATABASE`
- `MYSQL_USER`
- `MYSQL_PASSWORD`

Run from the root folder:
```
docker-compose -f x86/docker-compose.yml --project-director ./local_files up
```

Open matomo via browser.
At the step to setup the databse, as server name, use `database` or whatever it is set in the `docker-compose.yml` as database service.
Check also via `phpmyadmin`.

