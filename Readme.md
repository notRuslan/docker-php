
### Run on dev env
docker compose -f docker-compose.dev.yaml up -d

docker compose -f docker-compose.dev.yaml up -d --env-file .env

docker compose -f docker-compose.dev.yaml --env-file .env.local up --build -d

docker compose -f docker-compose.dev.yaml down

#### composer for package installation

composer install --ignore-platform-reqs

composer dump-autoload

### XDEBUG
XDEBUG_MODE=debug docker compose -f docker-compose.dev.yaml up -d

### Build image 
docker build --target app -t fitter73/php-composer:1.0 -f ./php/Dockerfile .

### push image
docker push fitter73/php-composer:1.0

### multiple docker-compose
docker compose -f docker-compose.yaml -f docker-compose.dev.yaml --env-file .env.local up -d

### Work in dev mode multi file
sh ./bin/dev-mode.sh -d  // for detach 

sh ./bin/dev-mode.sh -d --build // for detach and build

XDEBUG_MODE=debug sh ./bin/dev-mode.sh -d --build // for detach and build
