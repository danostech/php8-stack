# PHP8/Docker dev environment
A Docker and PHP 8 development environment with NGINX and MariaDB

### System Requirements
* [docker](https://docs.docker.com/get-docker/)
* [docker-compose](https://docs.docker.com/compose/)
#### Optional
* composer or (see [Creating a Composer Alias](#creating-a-composer-alias) below)
* git (optional, but you're here, so...)

---
### Setup
* [Download](https://github.com/danostech/docker-php8/archive/refs/heads/master.zip)
  or clone this repository

## Symfony 5 API with a docker development environment
1. `composer create-project symfony/skeleton api`
2. `docker-compose up -d` (you should be able to connect to localhost:8080 at this point and get the symfony welcome screen)
3. `cd app`
4. `composer require --dev phpunit/phpunit`
5. `composer require --dev symfony/maker-bundle`
6. `composer require doctrine/annotations`
7. modify `composer.json` change the php requirement to `"php": "~8.0"`,

#### Creating a Composer Alias
In .bashrc or .bash_aliases, whichever you use, add this line  
`alias composer='docker run --rm -it -v ${PWD}:/app --user $(id -u):$(id -g) composer'`
