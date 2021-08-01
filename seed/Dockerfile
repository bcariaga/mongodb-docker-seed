FROM mongo:bionic

COPY init-data.json /init-data.json

CMD mongoimport                                 \
    # Host (docker-compose service name)
    --host mongo-seed-db                        \
    # user and pass from .env file
    --username $MONGO_INITDB_ROOT_USERNAME      \
    --password $MONGO_INITDB_ROOT_PASSWORD      \
    --authenticationDatabase admin              \
    # initial db and collection from .env file
    --db $MONGO_INITDB_DATABASE                 \
    --collection $MONGO_INITDB_COLLECTION       \
    --type json                                 \
    --file /init-data.json                      \
    --jsonArray                                 \
    # WARNING! drop collection before run import
    --drop                                      \
    # verbose
    -v                                          \