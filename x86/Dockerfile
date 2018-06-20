############################################################
# Docker to try https://matomo.org
############################################################
FROM nginx
LABEL maintainer="Luong Bui"

RUN apt-get update && apt-get -y install vim nano wget zip php7.0 php7.0-curl php7.0-gd php7.0-cli mysql-server php7.0-mysql php-xml php7.0-mbstring

WORKDIR /usr/share/nginx/html/
RUN wget https://builds.piwik.org/piwik.zip && unzip piwik.zip

