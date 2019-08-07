### docker-compose service:
- php-fpm
- nginx
- mysql
- redis

### php extension:
- redis
- swoole


### USAGE
#### Example for using laravel:

step1: install laravel with composer:

```bash
./bin/composer create-project --prefer-dist laravel/laravel www "5.5.*"
```

step2: start all  docker container with docker-compose  (php redis nginx mysql..):
```
./start
```

Then enjoy!
website: http://0.0.0.0

For using laravel artisan or other script just following the command:
```bash
./bin/php artisan
```
And you may change your mysql account item in .env file，The mysql account info sees in docker-compose.yaml
