# yii2-oauth2-rest-docker
Repository consists of two parts:
 - `/api` - [docker-compose](https://docs.docker.com/compose/) files for quick run demo of Yii2 Rest Template with OAuth2 server (https://github.com/ikaras/yii2-oauth2-rest-template)
 - `/yii2-oauth2-rest-code` - Dockerfile for docker image https://registry.hub.docker.com/u/ikaras/yii2-oauth2-rest-code/ which contain configured source code of Yii2 Rest Template

## Quick run demo of Yii2 Rest Template with OAuth2 server
1. Make sure that you have installed [Docker Compose](https://docs.docker.com/compose/), if not - go to https://docs.docker.com/compose/install/ 
2. Clone this repo.
3. Go to `cd <directory with cloned repo>/api/`
4. Run command `docker-compose up`
5. Add to `/etc/hosts` following record `127.0.0.1 api.loc` (if you're using Boot2docker you need to replace ip with it one. `boot2docker ip` will tell you its address) 

You may get flaxibility to develop (change code in real time, saving db state between starts, replace diffent version php-fpm, apache, nginx and dbms) by reading documentation about (Docker)[https://docs.docker.com/]

ATTENTION: don't use it solution AS IS in production. It was built for quick demonstate work of Yii2 Rest Template with OAuth2 server  

## Docker image yii2-oauth2-rest-code
This image has already configured `ikaras/yii2-oauth2-rest-template` code with all needed php extensions, db connection and migration. On each running will be execute update template's and vendor's code, applying migrations
