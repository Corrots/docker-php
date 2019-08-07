### docker-compose中构建的服务:
- php-fpm
- nginx
- mysql
- redis

### php extension:
- redis
- swoole


### USAGE
#### Example for using laravel:

step1: start all  docker container with docker-compose  (php redis nginx mysql..):
```
./start
```

step2: install laravel with composer:

```bash
./bin/composer create-project --prefer-dist laravel/laravel www "5.5.*"
```

Then enjoy!
website: http://0.0.0.0

默认将docker中nginx(web服务)的80端口映射至主机的80端口，若需修改映射至主机的端口，
可修改 docker-compose.yaml 中nginx容器的配置(Line 14)

要使用laravel artisan或其他脚本指令，可在根目录执行如下指令:
```bash
./bin/php artisan
```
And you may change your mysql account item in .env file，The mysql account info sees in docker-compose.yaml
