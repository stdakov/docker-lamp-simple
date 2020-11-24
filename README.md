# docker-lamp-simple

A ready to use docker-compose configuration with php, mysql, nginx.

Containers:

- PHP 7.4
- nginx
- MySQL 5.7

## Installation

```shell
git clone https://github.com/stdakov/docker-lamp-simple.git
cd docker-lamp-simple/
git pull
docker-compose up -d
```

Wait some minutes and the containers are ready to go.

To confirm that everything is running fine go to `http://localhost:8000`.

#### Update container configuration

If you want to change some container configuration you need to rebuild the container:

```shell
docker-compose up -d --no-deps --build {service-name}
```

```shell
docker-compose up -d --no-deps --build phpmyadmin
```

```shell
docker-compose up --build -d
```

#### Connect to container:

```shell
docker-compose exec {service-name} bash
```

```shell
docker-compose exec app bash
```

```shell
docker-compose exec app ls -l
```

```shell
docker-compose exec app composer install
```

```shell
docker-compose exec app php artisan key:generate
```

```shell
docker-compose logs nginx
```

#### Restart everything:

```shell
docker-compose restart
```

#### Stop everything:

```shell
docker-compose stop
```

#### Remove everything:

```shell
docker-compose down -v
```
