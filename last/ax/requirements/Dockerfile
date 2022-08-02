FROM debian:buster

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
	&& apt-get install -y vim \
	&& apt-get install -y wget \
	&& apt-get install -y unzip
RUN apt-get -y install nginx
ADD conf/default /etc/nginx/sites-available/
ADD tools/nginx-selfsigned.crt /etc/ssl/certs/nginx-selfsigned.crt
ADD tools/nginx-selfsigned.key /etc/ssl/private/nginx-selfsigned.key
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#ENTRYPOINT /etc/init.d/nginx start -g "daemon off;";
