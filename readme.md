# Docker: Wordpress 6 & Redis 7 & PHP 8.1 & MariaDB 10.8 & phpMyAdmin 

## INSTALLATION

fetch docker-compose.yml file

```
curl -L https://raw.githubusercontent.com/creativeworkx/dockerpress/master/docker-compose.yml
```

start the containers

```
docker compose up -d
```

install wordpress using wordpress cli

```
docker compose exec wordpress_cli wp core install --url=localhost --title=creativeworkx_dockerpress --admin_user=admin --admin_password=password --admin_email=test@exmaple.org
```

install and activate plugins: query-monitor and redis-cache using wordpress cli

```
docker compose exec wordpress_cli wp plugin install query-monitor redis-cache --activate
```

activate wp redis integration using wordpress cli

```
docker compose exec wordpress_cli wp redis enable
```

## USAGE
Wordpress: [http://localhost/](http://localhost) -> Login at [http://localhost/wp-admin](http://localhost)

phpMyAdmin: [http://localhost:8080](http://localhost:8080) -> Already logged in

## BEWARE
Don't use in PRODUCTION