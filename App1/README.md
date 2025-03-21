## Stelle sicher das du eine Datenbank mit dem richtigen Namen auf deinem PG Server hast.

## überprüfe die Zugangsdaten in der Dockerfile im Backend

## Terminal im frontend Verzeichnis starten.
npm install

npm run build

docker build -t frontend-1 .

docker run --name client-1 -d -p 8080:80 frontend-1

## Terminal im backend Verzeichnis starten.
npm install

docker build -t backend-1 .

docker run --name server-1 -p 3050:3050 backend-1