# Laraver Craftable boilerplate
> CMS platform with MVC scaffolding.

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
	* [Dependencies](#dependencies)
	* [Enviroment variables](#enviroment-variables)
	* [Docker](#docker)
* [Status](#status)
* [Contact](#contact)

## General info
Based on Laravel Framework and Craftable package.

## Technologies
* [Laravel](https://laravel.com/docs/6.x) - 6.20
* [Craftable](https://www.getcraftable.com/docs/5.0/about) - 5.0
* Node - 12.20.0
* MySQL - 5.7.31

## Setup
Specifications to setup de project.

### Dependencies

* PHP 7.4. Extensions: exif gd pdo_mysql zip
* Apache 2. Modules: rewrite
* Debian Buster / Ubuntu 20.04. Libraries:
	*  git, libfreetype6-dev, libjpeg-dev, libzip-dev, unzip, zip
* MySQL 5.7.31
* npm - 6.14.8

### Enviroment variables

Copy `.env.example` to `.env` and replace enviroment variables accordingly. `DB_` and `DOCKER_` variables are mandatory.

### Docker

Run [docker-compose](https://docs.docker.com/compose/install/) to setup the enviroment. Enviroment variables in `.env` file have to be set.

```
docker-compose up -d
```

Enter `laravel-craftable` container to install PHP dependencies with composer.

```
docker exec -ti dataset bash
composer install
```

Enter `node12` container to install Node dependencies with npm and compile assets.

```
docker exec -ti node12 bash
npm install
npm run dev
npm run dev
```

Check project health status

```
http://localhost:${DOCKER_HTTP_PORT}
```

## Status

Project is: _development_

