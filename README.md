Generate Database initialization file:

    docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb_.sql

Run with:

    docker-compose up -d

Go to <http://localhost>, login with user/password: `guacadmin`.