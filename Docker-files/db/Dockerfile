FROM mysql:8.0.33

LABEL Project="Vprofile"
LABEL Author="Razaq"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_ROOT="accounts"

ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
EXPOSE 3306