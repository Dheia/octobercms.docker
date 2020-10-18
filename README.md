# Docker / OctoberCMS
Docker for OctoberCMS *(Based on Bitnami images)*

### To install it
```
$ cp .env.example .env
$ cp docker-compose.yml.example docker-compose.yml
$ docker-compose up -d
$ docker-compose exec app php artisan october:install
```

### To access shell of docker
```
docker-compose exec app bash
```

### To access shell as root
```
docker-compose exec -u root app bash
```
