# Docker / OctoberCMS
Docker for OctoberCMS *(Based on Bitnami images)*

### To begin using it
1. Copy `.env.example` to `.env`
2. Run `docker-compose up -d`
3. Run `docker-compose exec app php artisan october:install`

### To access shell of docker
```
docker-compose exec app bash
```

### To access shell as root
```
docker-compose exec -u root app bash
```
