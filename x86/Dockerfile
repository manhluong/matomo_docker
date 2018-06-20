############################################################
# Docker to try https://matomo.org
############################################################
FROM nginx
LABEL maintainer="Luong Bui"

RUN apt-get update && apt-get -y install vim nano wget zip systemd php7.0 php7.0-curl php7.0-gd php7.0-cli mysql-server php7.0-mysql php-xml php7.0-mbstring php-fpm

#From here: https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-ubuntu-18-04
RUN grep -q 'cgi.fix_pathinfo' "/etc/php/7.0/fpm/php.ini" && sed -i "s/^;cgi.fix_pathinfo.*/cgi.fix_pathinfo=0/g" "/etc/php/7.0/fpm/php.ini" 

COPY nginx_conf/default.conf /etc/nginx/conf.d/

WORKDIR /usr/share/nginx/html/
RUN wget https://builds.piwik.org/piwik.zip && unzip piwik.zip

