# MongoDB

## Install Mongodb Docker

create ``docker-compose.yml``
```yml
version: "3.5"

services:
  mongo:
    container_name: mongodb_0027
    image: mongo:4.2
    ports:
      - 27017:27017
    command: mongod
```

execute ``docker-compose``
```bash
docker compose -f docker-compose.yml up -d
```

access mongo server using terminal
```
docker exec -it mongodb_0027 /bin/sh
mongo --host localhost --port 27017
```

Backup
```
mongodump --db <dbname>
```

Restore
```
mongorestore --db <dbname> --verbose /dump/<directory>
```
