Generate Database initialization file:

    docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb_.sql

Run with:

    docker-compose up -d

Go to <http://localhost:8080/guacamole>, login with user/password: `guacadmin`.