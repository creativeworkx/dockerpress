# Docker & Wordpress 6 & Redis 7 & PHP 8.1 

## install

create and enter directory

```
curl -Lo sdsdsdsdsd
```

```
docker compose up -d
```

```
docker compose exec wordpress_cli wp core install --url=localhost --title=crw_wp --admin_user=admin --admin_password=password --admin_email=test@exmaple.org
```

```
docker compose exec wordpress_cli wp plugin install query-monitor redis-cache --activate
```

```
docker compose exec wordpress_cli wp redis enable
```
