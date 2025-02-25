# Run OLS on Server

export OLS4_CONFIG=./dataload/configs/sanger.json
JAVA_OPTS="-Xms5G -Xmx25G"  docker compose up

http://172.27.20.150:8081/ontologies


recommended but not used:
docker compose up --force-recreate --build --always-recreate-deps --attach-dependencies ols4-solr ols4-neo4j ols4-backend ols4-frontend
