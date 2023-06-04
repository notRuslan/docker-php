
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
