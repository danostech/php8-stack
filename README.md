# php8 develop environment w/ Docker
A Docker and PHP 8 development environment with NGINX and MariaDB.  
This is a minimal development environment. 
Take a look at the included files to learn more if you're interested.   
Quick setup instructions can be found below.

### System Requirements
* [docker](https://docs.docker.com/get-docker/)
* [docker-compose](https://docs.docker.com/compose/)

### Setup
```shell
# Clone the repo
git clone git@github.com:danostech/docker-php8.git your_app_name

# Create your public directory
cd your_app_name
mkdir -p app/public

# (optional)
# -----------
# edit docker-compose.yml
# change the names of the containers from `demo_*` to your app.
# change ports in the web and/or php containers

# edit .env
# change the  MYSQL_USER, MYSQL_PASSWORD, and MYSQL_DATABASE environment variables
# -------------------------------------------------------------------

# run docker
docker-compose up -d
```

Create an `index.php` file in `app/public`.  

Go to http://localhost:8080 in your browser.
