FROM php:7.2-fpm

#install pdo and adduser in a group
RUN docker-php-ext-install pdo_mysql &&\
	groupadd user &&\
	useradd admin --groups user

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
		apache2 \
	&& rm -rf /var/lib/apt/lists/*

	#Change documentroot give permissions and restart apache
RUN sed -i 's/#<Directory.*/<Directory /app>/g' /etc/apache2/sites-available/000-default.conf &&\
		chmod +755 /app &&\
		service apache2 restart

ENV APACHE_CONFDIR /etc/apache2
ENV APACHE_ENVVARS $APACHE_CONFDIR/envvars
ENV APACHE_RUN_USER admin
ENV APACHE_RUN_GROUP user
ENV APACHE_LOG_DIR /var/log/apache2


CMD ["/bin/sh", "-e"]
