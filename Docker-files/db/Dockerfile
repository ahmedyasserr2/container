From mysql:8.0.33
Label "Project"="Vprofile"
Label "Author"="Yasser" 

ENV MYSQL_ROOT_PASSWORD="vprofilepwd"
ENV MYSQL_DATABASE="accounts"


ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql

