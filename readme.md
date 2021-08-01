# MongoDb + Docker + seed

En este repo tenemos los archivos necesarios para levantar un contenedor Docker con:

- Un server con MongoDb
- Una collection con los datos que están en `seed/init-data.json`
- Un `volume` para que los datos no se pierdan

## Que necesito?

- Docker (y docker-compose, por lo general ya viene con docker desktop)

- [Opcional] `mongosh` o algún ~ide~ _cliente_ para corroborar la conexión

## Como lo levanto?

Después de clonar el repo:

1. Agrega lo que necesites en la DB al archivo `seed/init-data.json`, es un `json` respeta el formato 😉
2. Modifica `.env` si necesitas cambiar el nombre de la db y collection.
3. _Levanta_ el compose: `docker-compose up`
4. Listo!
