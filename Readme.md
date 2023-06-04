
### Run on dev env
docker compose -f docker-compose.dev.yaml up -d

docker compose -f docker-compose.dev.yaml up -d --env-file .env

#### composer for package installation

composer install --ignore-platform-reqs

composer dump-autoload

### XDEBUG
XDEBUG_MODE=debug docker compose -f docker-compose.dev.yaml up -d
