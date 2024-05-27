FROM ubuntu:22.04

RUN DEBIAN_FRONTEND=noninteractive apt update && DEBIAN_FRONTEND=noninteractive apt install --no-install-recommends -y mariadb-server

COPY ./mariadb.cnf /etc/mysql/mariadb.cnf

CMD ["mysqld", "--user=mysql", "--console"]

