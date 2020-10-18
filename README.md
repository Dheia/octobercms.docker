# Docker / OctoberCMS
Docker for OctoberCMS *(Based on Bitnami images)*
**For usage as submodule**

### What included
1. `bitnami/php-fpm:7.4-debian-10`
2. `bitnami/apache:2.4-debian-10`
3. `djfarrelly/maildev`

### How to use
```
$ git clone https://github.com/WebCreamGroup/OctoberCMS-Docker.git ./octobercms-docker
$ cp -rf octobercms-docker/theme ./
$ cp -rf octobercms-docker/plugins ./
```

### How to setup
```
$ git clone https://github.com/WebCreamGroup/OctoberCMS-Docker.git ./
$ cp .env.example .env
$ cp docker-compose.yml.example docker-compose.yml
$ docker-compose up -d
$ docker-compose exec app php artisan october:install
```

### How to setup as submodule
```
$ git submodule add --depth 1 https://github.com/WebCreamGroup/OctoberCMS-Docker.git ./octobercms-docker
$ cd ./octobercms-docker
$ cp -rf ./theme ../
$ cp -rf ./plugins ../
$ cp .env.example .env
// Change SOURCE_ROOT_PATH=./ to SOURCE_ROOT_PATH=../
$ cp docker-compose.yml.example docker-compose.yml
$ docker-compose up -d
$ docker-compose exec app php artisan october:install
```

### Locations
- **OctoberCMS**: `http://localhost` or for **ssl** `https://localhost`
- **Maildev**: `http://localhost:1080`

### How to access shell of docker
```
docker-compose exec app bash # As main user
docker-compose exec -u root app bash # As root
```
