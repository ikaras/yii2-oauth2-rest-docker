# yii2-oauth2-rest-docker
Repository consists of two parts:
 - `/api` - [docker-compose](https://docs.docker.com/compose/) files for quick run demo of Yii2 Rest Template with OAuth2 server (https://github.com/ikaras/yii2-oauth2-rest-template)
 - `/yii2-oauth2-rest-code` - Dockerfile for docker image https://registry.hub.docker.com/u/ikaras/yii2-oauth2-rest-code/ which contain configured source code of Yii2 Rest Template

# Quick run demo of Yii2 Rest Template with OAuth2 server
1. Make sure that you have installed [Docker Compose](https://docs.docker.com/compose/), if not - go to https://docs.docker.com/compose/install/ 
2. Clone this repo.
3. Go to `cd <directory with cloned repo>/api/`
4. Run command `docker-compose up`
