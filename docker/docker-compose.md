## Rebuild one container
### changes inside of the original dockerfile being taken into consideration
docker-compose build <service name>

### To rebuild your Docker Compose setup based on new changes and run it
#### add --remove-orphans if you deleted one of the containers
docker-compose up --build -d

### build the container without cache
docker-compose build --no-cache <service name>

### build one service and run all services after that
docker-compose up -d --build <service name>

### build the container without cache and run it
#### --no-deps tells Docker Compose not to start linked services.
docker-compose build up -d --no-cache --no-deps <service name>

### The --force-recreate option ensures the container is recreated even if Docker Compose detects no changes in the configuration.
docker-compose up -d --force-recreate <service name>
