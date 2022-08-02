FROM debian:buster

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y vim \
    && apt-get install -y wget \
    && apt-get install -y unzip \
    && apt-get install -y net-tools\
    && apt-get install -y curl
RUN apt install -y php7.3-fpm php-mysql
COPY conf/script.sh  /
COPY conf/wp-config.php /
CMD [ "sh", "script.sh" ]