# Connect Server

Connect to the VPN.

```
cd ...../ssh_keys
ssh -i id_ed25519 ubuntu@172.27.20.150
```

Navigate to OLS folder in the server

```
cd OLS/ols4/
```

## Restart server

This operation will delete the existing data and re-read from scratch.

export OLS4_CONFIG=./dataload/configs/sanger.json

JAVA_OPTS="-Xms5G -Xmx25G"  docker compose down -v

JAVA_OPTS="-Xms5G -Xmx25G"  docker compose up


# Run OLS on Server

Run:

export OLS4_CONFIG=./dataload/configs/sanger.json

JAVA_OPTS="-Xms5G -Xmx25G"  docker compose up

http://172.27.20.150:8081/ontologies


## Configure

edit: frontend/.env


## With local Nginx 

JAVA_OPTS="-Xms5G -Xmx25G"  docker compose -f docker-compose-nginx.yml up

http://localhost/ols



recommended but not used:
docker compose up --force-recreate --build --always-recreate-deps --attach-dependencies ols4-solr ols4-neo4j ols4-backend ols4-frontend

