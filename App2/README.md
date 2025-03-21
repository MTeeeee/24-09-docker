## Zugangsdaten anpassen

## Terminal im frontend Verzeichnis starten.

npm install

docker build -t frontend-2 .

docker run --name client-2 -d -p 8080:80 frontend-2

## Terminal im backend Verzeichnis starten.

npm install

docker build -t backend-2 .

docker run --name postgres_db -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=techstarter -e POSTGRES_DB=todos_db -p 5434:5432 -v pgdata:/var/lib/postgresql/data -d postgres

docker run --name server-2 --network=mynetwork --env-file .env -p 3050:3050 backend-2