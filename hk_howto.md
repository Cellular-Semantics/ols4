export OLS4_CONFIG=./dataload/configs/sanger.json

docker compose up --force-recreate --build --always-recreate-deps --attach-dependencies ols4-solr ols4-neo4j ols4-backend ols4-frontend
