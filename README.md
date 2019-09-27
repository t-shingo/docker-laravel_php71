# docker-laravel_php71
laravel on docker
----
# environment
| app | version |
| -- |
| MySQL | 5.7 |
| php | 7.3 |
| laravel |  |

# create new laravel project
- on host server
```
cd ddocker-laravel_php71/docker-compose
docker-compose up -d

docker exec -it php /bin/bash
```

- create new laravel project on docker php-fpm
```
laravel new hogehoge
```