FROM ikaras/phpcode
MAINTAINER Ihor Karas <ihor@karas.in.ua>
RUN cd /var/www/html \
	&& composer global require "fxp/composer-asset-plugin:1.0.0" \
	&& composer create-project --keep-vcs --stability="dev" --prefer-source ikaras/yii2-oauth2-rest-template .
VOLUME ["/var/www/html"]
CMD	git pull \
	&& composer update -n --prefer-dist \
	&& php -r "sleep(60);" \
	&& php /var/www/html/application/api/yiic migrate --migrationPath=@yii/rbac/migrations --interactive=0 \
	&& php /var/www/html/application/api/yiic migrate --migrationPath=@vendor/filsh/yii2-oauth2-server/migrations --interactive=0 \
   	&& php /var/www/html/application/api/yiic migrate --interactive=0 \
   	&& echo "==== API READY FOR REQUESTS ====" \
	&& php -r "while(true){sleep(86400);}"
