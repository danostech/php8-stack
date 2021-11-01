# PHP8/Docker dev environment
A Docker and PHP 8 development environment with NGINX and MariaDB

### System Requirements
* [docker](https://docs.docker.com/get-docker/)
* [docker-compose](https://docs.docker.com/compose/)


---
### Setup
```shell
git clone git@github.com:danostech/docker-php8.git your_app_name
cd your_app_name
mkdir -p app/public
docker-compose up -d
```

### Symfony 5
```shell
git clone git@github.com:danostech/docker-php8.git your_app_name
cd your_app_name
composer create-project symfony/skeleton app
docker-compose up -d
```