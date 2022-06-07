# Docker: Wordpress 6 & Redis 7 & PHP 8.1 & MariaDB 10.8 & phpmyadmin 

## Installation

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

activate wp redis integration

```
docker compose exec wordpress_cli wp redis enable
```
