# Docker / OctoberCMS
Docker for OctoberCMS *(Based on Bitnami images)*

### How to setup
```
$ cp .env.example .env
$ cp docker-compose.yml.example docker-compose.yml
$ docker-compose up -d
$ docker-compose exec app php artisan october:install
```

### Locations
```
http://localhost or https://localhost # The OctoberCMS
http://localhost:1080 # The Maildev
```

### How to access shell of docker
```
docker-compose exec app bash # As main user
docker-compose exec -u root app bash # As root
```
