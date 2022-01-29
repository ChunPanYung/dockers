# Dockers On Server
contains all configurations needed for custom docker containers

## nextcloud
- need ssl private key and self-signed certificate before building
- define variables stated in `Dockerfile` and `docker-compose.yml`
- automatically read `.env` file under same directory, even using `docker-compose --file *file*`

## ubuntu
- `rsync` command installed
