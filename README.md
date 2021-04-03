# Docker LEMP

|name|pulls|version|layers|image size|
|:---:|:---:|:---:|:---:|:---:|
|[idawnlight/php](https://hub.docker.com/r/idawnlight/php)|![Pulls Count](https://img.shields.io/docker/pulls/idawnlight/php.svg?style=flat-square)|![GitHub release (latest by date)](https://img.shields.io/github/v/tag/idawnlight/docker-php?style=flat-square)|![Layers](https://shields.beevelop.com/docker/image/layers/idawnlight/php/latest.svg?style=flat-square)|![image size](https://shields.beevelop.com/docker/image/image-size/idawnlight/php/latest.svg?style=flat-square)|
|[idawnlight/nginx](https://hub.docker.com/r/idawnlight/nginx)|![Pulls Count](https://img.shields.io/docker/pulls/idawnlight/nginx.svg?style=flat-square)|![GitHub release (latest by date)](https://img.shields.io/github/v/tag/idawnlight/docker-nginx?style=flat-square)|![](https://shields.beevelop.com/docker/image/layers/idawnlight/nginx/latest.svg?style=flat-square)|![](https://shields.beevelop.com/docker/image/image-size/idawnlight/nginx/latest.svg?style=flat-square)|
|[mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server)|![Pulls Count](https://img.shields.io/docker/pulls/mysql/mysql-server.svg?style=flat-square)||![](https://shields.beevelop.com/docker/image/layers/mysql/mysql-server/latest.svg?style=flat-square)|![](https://shields.beevelop.com/docker/image/image-size/mysql/mysql-server/latest.svg?style=flat-square)|
|[library/redis](https://hub.docker.com/_/redis)|![Pulls Count](https://img.shields.io/docker/pulls/library/redis.svg?style=flat-square)||![](https://shields.beevelop.com/docker/image/layers/library/redis/alpine.svg?style=flat-square)|![](https://shields.beevelop.com/docker/image/image-size/library/redis/alpine.svg?style=flat-square)|
|[phpmyadmin/phpmyadmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)|![Pulls Count](https://img.shields.io/docker/pulls/phpmyadmin/phpmyadmin.svg?style=flat-square)||![](https://shields.beevelop.com/docker/image/layers/phpmyadmin/phpmyadmin/latest.svg?style=flat-square)|![](https://shields.beevelop.com/docker/image/image-size/phpmyadmin/phpmyadmin/latest.svg?style=flat-square)|

## Requirements

Install [Docker](https://get.docker.com/) and [Compose](https://docs.docker.com/compose/install/)

## Usage

 1. Clone docker-lemp inside your project
```bash
git clone https://github.com/idawnlight/docker-lemp.git
```
 2. Enter the docker-lemp folder and rename .env.example to .env.
```bash
cd docker-lemp
cp .env.example .env
cp docker-compose.example.yml docker-compose.yml
```
 3. Open your project’s .env file and set the following:
```ini
MYSQL_ROOT_PASSWORD=your_password
```
 4. Run your containers:
```bash
docker-compose up -d
```

## Running `brotli`

 1. Add the following lines into the configuration file of your sites to enable `brotli` feature:
```nginx
brotli on;
brotli_comp_level 6;
brotli_types text/plain text/css application/json application/x-javascript text/xml application/xml application/xml+rss text/javascript application/javascript image/svg+xml;
```

## Generally Upgrade

 1. Modify project’s .env file.
```bash
vim .env
```

 2. Rebuild containers:
```bash
docker-compose up -d --no-deps --build
```

# Acknowledgement

Appreciate metowolf for this great work!