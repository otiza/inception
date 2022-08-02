FROM debian:buster

# ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y vim \
    && apt-get install -y wget \
    && apt-get install -y unzip \
    && apt-get install -y net-tools

RUN apt install mariadb-server -y

RUN chown -R mysql:mysql /var/lib/mysql

#COPY ./conf/wordpress.sql /

#COPY ./conf/script.sh /

#RUN chmod +x script.sh

#RUN sed -i 's/127.0.0.1/0.0.0.0/g' /etc/mysql/mariadb.conf.d/50-server.cnf

EXPOSE 3306

#CMD ["sh", "script.sh"]
ENTRYPOINT["tail -f"]